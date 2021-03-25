---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## Tehtävä 2: Laskee kolmion alan
Sivujen pituudet ovat 5,6 ja 7. 
Tehtävä sisältää kaksi "harhautusriviä" jotka eivät kuulu ohjelmaan. Kokoa ohjelman rivit alla olevaan laatikkoon. 

<div id="P2-sortableTrash" class="sortable-code"></div> 
<div id="P2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "var side1 = 5;  \\n var side2 = 6;  \\n var side3 = 7;  \\n \n" +
    "var s = (side1 + side2 + side3)/2;\n" +
    "var area =  Math.sqrt(s*((s-side1)*(s-side2)*(s-side3)));\n" +
    "console.log(area);\n" +
    "var a = (side1 + side2 + side3); #distractor\n" +
    "var b = a/2; #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



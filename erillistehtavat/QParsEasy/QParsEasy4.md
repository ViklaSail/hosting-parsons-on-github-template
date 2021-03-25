---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 4: arpoo numeron 1 ja 10 väliltä, 
pyytää käyttäjää arvaamaan mikä se oli, tulostaa arvattiinko oikein ja arvotun numeron jos arvaus ei ollut oikea. 
<div id="P4-sortableTrash" class="sortable-code"></div> 
<div id="P4-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P4-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P4-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "const num = Math.ceil(Math.random() * 10); \\n console.log(num); \\n const gnum = prompt('Arvaa numero 1 ja 10 väliltä'); \\n \n" +
    "if (gnum == num)\n" +
    "   console.log('Arvasit oikein');\n" +
    "else\n" +
    "   console.log('Väärin, numero oli '+gnum);\n" +
    "console.log(aNum); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P4-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P4-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P4-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P4-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



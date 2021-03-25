---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 5
Javascript funktio näyttää eroaako parametrina annettu luku luvusta 13 ja tulostaa erotuksen. 
jos annettu luku on suurempi kuin 13 ohjelma palauttaa eron kerrottuna kahdella.
<div id="P5-sortableTrash" class="sortable-code"></div> 
<div id="P5-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P5-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P5-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function difference(n)\n" +
    "{\n" +
    "    if (n <= 13)\n" +
    "        return 13 - n;\n" +
    "    else\n" +
    "        return (n - 13) * 2;\n" +
    "}\n" +
    "console.log(difference(32)) \\n console.log(difference(11)) \\n \n" +
    "console.log(aNum); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P5-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P5-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P5-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P5-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>




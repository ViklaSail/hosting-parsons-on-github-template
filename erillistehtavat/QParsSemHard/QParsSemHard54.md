---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 54
Järjestä koodirivit ohjelmaksi joka etsii annetusta listasta suurimman parillisen numeron.

<div id="P54-sortableTrash" class="sortable-code"></div> 
<div id="P54-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P54-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P54-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function max_even(arra) {\n" +
    "  arra.sort((x, y) => y - x);\n" +
    "  for (var i = 0; i < arra.length; i++) {\n" +
    "    if (arra[i] % 2 == 0)\n" +
    "      return arra[i];\n" +
    "  }\n" +
    "} \\n console.log(max_even([20, 40, 200])); \\n console.log(max_even([20, 40, 200, 301])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P54-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P54-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P54-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P54-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
## tehtävä 55
Järjestä koodirivit ohjelmaksi joka 


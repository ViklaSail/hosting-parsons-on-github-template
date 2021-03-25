---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 12
Järjestä koodirivit ohjelmaksi joka tarkastaa meneekö parametrina annetun luvun jako 3 tai 7 tasan.
<div id="P12-sortableTrash" class="sortable-code"></div> 
<div id="P12-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P12-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P12-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function test37(x) \n" +
    "{\n" +
    "  if (x % 3 == 0 || x % 7 == 0) \n" +
    "  {\n" +
    "    return true;\n" +
    "  } \n" +
    "  else {\n" +
    "    return false;\n" +
    "  }\n" +
    "} \\n console.log(test37(12)); \\n console.log(test37(14)); \\n console.log(test37(10)); \\n console.log(test37(11)); \\n \n" +
    "first = str.substring(0,2); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P12-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P12-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P12-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P12-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>





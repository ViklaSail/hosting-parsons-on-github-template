---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 40
Järjestä koodirivit ohjelmaksi joka tutkii saadaanko parametrina annetuista merkkijonoista samanlaiset vaihtelemalla merkkien järjestystä toisessa. 
<div id="P40-sortableTrash" class="sortable-code"></div> 
<div id="P40-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P40-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P40-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function rearrangement_characters(str1, str2) {\n" +
    "  var first_set = str1.split(''), \\n       second_set = str2.split(''), \\n       result = true; \\n \n" +
    "      \n" +
    "  first_set.sort(); \\n second_set.sort(); \\n \n" +
    "  for (var i = 0; i < Math.max(first_set.length, second_set.length); i++) {\n" +
    "    if (first_set[i] !== second_set[i]) {\n" +
    "      result = false;\n" +
    "    }\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(rearrangement_characters(\"xyz\", \"zyx\")) \\n console.log(rearrangement_characters(\"xyz\", \"zyp\")) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P40-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P40-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P40-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P40-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


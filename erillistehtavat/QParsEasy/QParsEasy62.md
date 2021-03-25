---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 62
Järjestä koodirivit ohjelmaksi. funktio saa parametrina merkkijonon ja laskee kaikkien sen sisältämien numeroiden summan
<div id="P62-sortableTrash" class="sortable-code"></div> 
<div id="P62-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P62-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P62-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sum_digits_from_string(dstr) {\n" +
    "  var dsum = 0;\n" +
    "  for (var i = 0; i < dstr.length; i++)\n" +
    "  {\n" +
    "    if (/[0-9]/.test(dstr[i])) dsum += parseInt(dstr[i])\n" +
    "  }\n" +
    "  return dsum;\n" +
    "} \\n console.log(sum_digits_from_string(\"abcd12efg9\")) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P62-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P62-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P62-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P62-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


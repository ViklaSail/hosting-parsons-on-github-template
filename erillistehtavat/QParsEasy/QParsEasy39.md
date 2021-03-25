---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 39
Järjestä koodirivit ohjelmaksi joka tutkii annetusta merkkijonosta onko isoja vai pieniä kirjaimia siinä eniten. sanan case vaihdetaan isoiksi kirjaimiksi jos isoja kirjaimia on eniten, jos pieniä kirjaimia on eniten, kaikki caset vaihdetaan pieniksi. 
<div id="P39-sortableTrash" class="sortable-code"></div> 
<div id="P39-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P39-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P39-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function change_case(new_str) {\n" +
    "  var x = 0; \\n   var y = 0; \\n \n" +
    "  for (var i = 0; i < new_str.length; i++) {\n" +
    "    if (/[A-Z]/.test(new_str[i])) {\n" +
    "      x++;\n" +
    "    } else y++;\n" +
    "  }\n" +
    "  if (y > x) return new_str.toLowerCase();\n" +
    "  return new_str.toUpperCase();\n" +
    "} \\n console.log(change_case(\"Write\")) \\n console.log(change_case(\"PHp\")) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P39-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P39-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P39-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P39-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>




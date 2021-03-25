---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 28
Järjestä koodirivit ohjelmaksi joka saa merkkijonon parametrina ja luo siitä uuden poistamalla ensimmäisen ja viimeisen merkin, jos ensimmäinen tai viimeinen merkki on 'p'. Muutoin palautetaan alkuperäinen merkkijono
<div id="P28-sortableTrash" class="sortable-code"></div> 
<div id="P28-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P28-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P28-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function nop(str) {\n" +
    "  let start_pos = 0; \\n let end_pos = str.length; \\n \n" +
    "  if (str.length > 0 && str.charAt(0) == 'P') \n" +
    "  { \n" +
    "    start_pos = 1; \n" +
    "  } \\n if (str.length > 1 && str.charAt(str.length - 1) == 'P')  \\n \n" +
    "  {\n" +
    "    end_pos--;\n" +
    "  }\n" +
    "  return str.substring(start_pos, end_pos);\n" +
    "} \\n console.log(nop(\"PythonP\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P28-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P28-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P28-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P28-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


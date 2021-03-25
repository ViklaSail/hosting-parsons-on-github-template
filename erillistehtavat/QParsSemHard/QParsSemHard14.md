---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 14
Järjestä koodirivit ohjelmaksi joka tarkastaa onko annetun merkkijonon alussa sana "java" ja siinä tapauksessa palauttaa arvon true. 
<div id="P14-sortableTrash" class="sortable-code"></div> 
<div id="P14-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P14-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P14-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function start_spec_str(str)\n" +
    "{\n" +
    "  if (str.length < 4)\n" +
    "  {\n" +
    "    return false;\n" +
    "  }\n" +
    "  front = str.substring(0, 4);\n" +
    "  if (front == 'Java') \n" +
    "  {\n" +
    "    return true;\n" +
    "  }\n" +
    "  else \n" +
    "  {\n" +
    "    return false;\n" +
    "  }\n" +
    "} \\n console.log(start_spec_str(\"JavaScript\")); \\n console.log(start_spec_str(\"Java\")); \\n console.log(start_spec_str(\"Python\")); \\n \n" +
    "back2 = str.substring(str.length-4); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P14-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P14-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P14-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P14-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


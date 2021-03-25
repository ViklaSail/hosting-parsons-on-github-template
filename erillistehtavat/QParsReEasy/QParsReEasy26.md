---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 26
Järjestä koodirivit ohjelmaksi joka muodostaa uuden merkkijonon parametriksi saadun merkkijonon 3 viimeisestä merkistä: kopioi merkkijonoon noita viimeisiä merkkejä kolme kertaa. parametriksi saadun merkkijonon pitää olla vähintään 3 merkkiä pitkä. 
<div id="P26-sortableTrash" class="sortable-code"></div> 
<div id="P26-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P26-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P26-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function newstring(str)\n" +
    "{\n" +
    "  if (str.length >= 3) {\n" +
    "    result_str = str.substring(str.length - 3);\n" +
    "    return result_str + result_str + result_str + result_str;\n" +
    "  }\n" +
    "  else\n" +
    "    return false;\n" +
    "} \\n console.log(newstring(\"Python 3.0\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P26-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P26-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P26-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P26-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



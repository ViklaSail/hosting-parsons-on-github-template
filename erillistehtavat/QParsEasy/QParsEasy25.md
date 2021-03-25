---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 25
Järjestä koodirivit ohjelmaksi joka saa parametrina lauseen ja muuttaa lauseen jokaisen sanan ensimmäisen merkin isoksi. 
<div id="P25-sortableTrash" class="sortable-code"></div> 
<div id="P25-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P25-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P25-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function capital_letter(str) \n" +
    "{\n" +
    "    str = str.split(\" \");\n" +
    "    for (var i = 0, x = str.length; i < x; i++) {\n" +
    "        str[i] = str[i][0].toUpperCase() + str[i].substr(1);\n" +
    "    }\n" +
    "    return str.join(\" \");\n" +
    "} \\n console.log(capital_letter(\"Write a JavaScript program to  \\n capitalize the first letter of each word of a given string.\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P25-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P25-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P25-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P25-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script> 





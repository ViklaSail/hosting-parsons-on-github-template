---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 10
Järjestä koodirivit ohjelmaksi, joka saa parametriksi merkkijonon ja vaihtaa viimeisen ja ensimmäisen merkin paikkoja. Merkkijonon on oltava vähintään yhden merkin pituinen 
<div id="P10-sortableTrash" class="sortable-code"></div> 
<div id="P10-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P10-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P10-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function first_last(str1) \n" +
    "{\n" +
    "  if (str1.length <= 1)\n" +
    "  {\n" +
    "    return str1;\n" +
    "  }\n" +
    "  mid_char = str1.substring(1, str1.length - 1);\n" +
    "  return (str1.charAt(str1.length - 1)) + mid_char + str1.charAt(0);\n" +
    "} \\n console.log(first_last('a')); \\n console.log(first_last('ab')); \\n console.log(first_last('abc')); \\n \n" +
    "  if (n >= 19) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P10-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P10-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P10-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P10-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


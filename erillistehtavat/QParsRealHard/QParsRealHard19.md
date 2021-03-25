---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 19
Järjestä koodirivit ohjelmaksi joka tarkastaa löytyykö annettu merkki annetussa merkkijonossa sen toisen ja neljännen merkkipositioiden välissä. Tehtävässä ei ole yhtään harhautusblokkia.


<div id="P19-sortableTrash" class="sortable-code"></div> 
<div id="P19-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P19-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P19-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check_char(str1, char)\n" +
    "{\n" +
    "  var ctr = 0;\n" +
    "  for (let i = 0; i < str1.length; i++)\n" +
    "  {\n" +
    "    if ((str1.charAt(i) == char) && (i >= 1 && i <= 3))\n" +
    "    {\n" +
    "        ctr=1;\n" +
    "        break;\n" +
    "    }\n" +
    "  }\n" +
    "  if (ctr==1) return true;\n" +
    "  return false;\n" +
    "} \\n console.log(check_char(\"Python\", \"y\")); \\n console.log(check_char(\"JavaScript\", \"a\")); \\n console.log(check_char(\"Console\", \"o\")); \\n console.log(check_char(\"Console\", \"C\")); \\n console.log(check_char(\"Console\", \"e\")); \\n console.log(check_char(\"JavaScript\", \"S\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P19-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P19-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P19-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P19-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


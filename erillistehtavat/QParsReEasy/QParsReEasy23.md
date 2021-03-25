---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 23
Järjestä koodirivit ohjelmaksi joka tarkastaa kaksi annettua kokonaislukua, että onko jonpi kumpi 8 tai onko niiden summa 8 tai onko niiden ero 8. Palauttaa totuusarvon. Tehtävässä virhe: if-lauseiden järjestyksellä väliä, jos ei mene läpi, vaihda niiden järjestystä. 
<div id="P23-sortableTrash" class="sortable-code"></div> 
<div id="P23-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P23-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P23-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check8(x, y) {\n" +
    "  if (x == 8 || y == 8) {\n" +
    "    return true;\n" +
    "  }\n" +
    "  if (x + y == 8 || Math.abs(x - y) == 8)\n" +
    "  {\n" +
    "    return true;\n" +
    "  }\n" +
    "  return false;\n" +
    "} \\n console.log(check8(7, 8)); \\n console.log(check8(16, 8)); \\n console.log(check8(24, 32)); \\n console.log(check8(17, 18)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P23-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P23-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P23-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P23-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 61
Järjestä koodirivit ohjelmaksi. funktio saa parametrina kokonaisluvun  n ja palauttaa sen perusteella komanteen potenssiin korotettujen numeroiden summan seuraavasti: 1^3 +  2^3 + 3^3 + 4^3 + .. n^3 
<div id="P61-sortableTrash" class="sortable-code"></div> 
<div id="P61-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P61-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P61-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sum_Of_Cubes(n) {\n" +
    "  let sumn = 0;\n" +
    "  for (let i = 1; i <= n; i++) {\n" +
    "    sumn += i ** 3;\n" +
    "  }\n" +
    "  return sumn;\n" +
    "} \\n console.log(sum_Of_Cubes(3)); \\n console.log(sum_Of_Cubes(4)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P61-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P61-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P61-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P61-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



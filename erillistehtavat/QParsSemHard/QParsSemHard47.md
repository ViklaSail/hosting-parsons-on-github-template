---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 47
Järjestä koodirivit ohjelmaksi joka tulostaa kahden 3-ulotteisen vektorin pistetulon. 
Huom: pistetulo on vektoreiden alkioiden tulojen summa, eli tässä tapauksessa taulukoiden 1. alkiot kerrotaan keskenään, 2. alkiot keskenään ja 3. alkiot keskenään. lopuksi kaikki summataan yhteen. Pistetulosta löytyy tietoa esim. vikipediasta. 
Tässä palapelissä sillä ei ole väliä, pystyt päättelemään rivien järjestyksen tämän lyhyen kuvauksen ja muuttujien esittelyn/käytön perusteella.
<div id="P47-sortableTrash" class="sortable-code"></div> 
<div id="P47-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P47-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P47-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function dot_product(vector1, vector2) {\n" +
    "  let result = 0;\n" +
    "  for (let i = 0; i < 3; i++) {\n" +
    "    result += vector1[i] * vector2[i];\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(dot_product([1,2,3], [1,2,3])) \\n console.log(dot_product([2,4,6], [2,4,6])) \\n console.log(dot_product([1,1,1], [0,1,-1])) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P47-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P47-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P47-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P47-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



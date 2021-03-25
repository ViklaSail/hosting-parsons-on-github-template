---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 7
Järjestä seuraavat rivit ohjelmaksi joka laskee parametrina annetun luvun absoluuttisen eron lukuun 19 ja palauttaa sen. Jos annettu luku on suurempi kuin 19, ohjelma palauttaa absoluuttisen eron kolminkertaisena. 
<div id="P7-sortableTrash" class="sortable-code"></div> 
<div id="P7-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P7-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P7-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function diff_num(n) {\n" +
    "  if (n <= 19) {\n" +
    "    return (19 - n);\n" +
    "  } else {\n" +
    "     return (n - 19) * 3;\n" +
    "  }\n" +
    "} \\n console.log(diff_num(12)); \\n console.log(diff_num(19)); \\n console.log(diff_num(22)); \\n \n" +
    "  if (n >= 19) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P7-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P7-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P7-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P7-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>




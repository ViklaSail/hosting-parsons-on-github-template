---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 6
Kokoa riveistä javascript ohjelma joka laskee kahden kokonaisluvun summan. Jos annetut luvut ovat yhtäsuuret, palautetaan niiden summa kerrottuna kolmella

<div id="P6-sortableTrash" class="sortable-code"></div> 
<div id="P6-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P6-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P6-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sumTriple (x, y) {\n" +
    "  if (x == y) {\n" +
    "    return 3 * (x + y);\n" +
    "  } else {\n" +
    "    return (x + y);\n" +
    "  }\n" +
    "} \\n console.log(sumTriple(10, 20)); \\n console.log(sumTriple(10, 10)); \\n \n" +
    "  if (x =< y) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P6-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P6-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P6-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P6-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



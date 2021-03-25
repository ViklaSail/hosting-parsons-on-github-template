---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 56
Järjestä koodirivit ohjelmaksi. Funktio saa lukuarvon parametriksi. Ohjelma laskee tuon lukuarvon parillisten numeroiden määrän ja palauttaa sen. 
<div id="P56-sortableTrash" class="sortable-code"></div> 
<div id="P56-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P56-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P56-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function even_digits(num) {\n" +
    "  var ctr = 0;\n" +
    "  while (num) {\n" +
    "    ctr += num % 2 === 0; \\n num = Math.floor(num / 10); \\n \n" +
    "  }\n" +
    "  return ctr;\n" +
    "} \\n console.log(even_digits(123)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P56-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P56-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P56-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P56-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


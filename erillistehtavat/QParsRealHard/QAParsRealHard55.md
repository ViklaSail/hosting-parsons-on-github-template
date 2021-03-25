---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 55
Järjestä koodirivit ohjelmaksi. Tämä ohjelma saa parametriksi numeron ja antaa vastaukseksi ensimmäisen annettua numeroa suuremman alkuluvun. 
<div id="P55-sortableTrash" class="sortable-code"></div> 
<div id="P55-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P55-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P55-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function next_Prime_num(num) {\n" +
    "    for (var i = num + 1;; i++) {\n" +
    "        var isPrime = true;\n" +
    "        for (var d = 2; d * d <= i; d++) {\n" +
    "            if (i % d === 0) {\n" +
    "                isPrime = false;\n" +
    "                break;\n" +
    "            }\n" +
    "        }\n" +
    "        if (isPrime) {\n" +
    "            return i;\n" +
    "        }\n" +
    "    }\n" +
    "} \\n console.log(next_Prime_num(3)); \\n console.log(next_Prime_num(17)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P55-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P55-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P55-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P55-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



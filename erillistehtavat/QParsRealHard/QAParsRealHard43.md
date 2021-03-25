---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 43
Järjestä koodirivit ohjelmaksi joka poistaa parametrista annetusta numerosta yhden merkin/luvun. Tämä tehdään niin että muodostunut uusi numero on suurin mahdollinen, vaikka yksi numero onkin sen sisältä poistettu. 
<div id="P43-sortableTrash" class="sortable-code"></div> 
<div id="P43-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P43-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P43-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function digit_delete(num) {\n" +
    "    var result = 0, num_digits = [];\n" +
    "    while (num) {\n" +
    "        num_digits.push(num % 10); \\n num = Math.floor(num / 10); \\n \n" +
    "    }\n" +
    "    for (var index_num = 0; index_num < num_digits.length; index_num++) {\n" +
    "        var n = 0;\n" +
    "        for (var i = num_digits.length - 1; i >= 0; i--) {\n" +
    "            if (i !== index_num) {\n" +
    "                n = n * 10 + num_digits[i];\n" +
    "            }\n" +
    "        }\n" +
    "        result = Math.max(n, result);\n" +
    "    }\n" +
    "    return result;\n" +
    "} \\n console.log(digit_delete(100)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P43-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P43-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P43-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P43-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



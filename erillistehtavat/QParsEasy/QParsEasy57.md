---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 57
Järjestä koodirivit ohjelmaksi. funktio poistaa kaikki merkit jotka esiintyvät useammin kuin kerran parametrina annetussa merkkijonossa. Palauttaa uuden merkkijonon. TEHTÄVÄSSÄ VIRHE. for lauseen lopetussulje pitää sisentää askelen liikaa, sitten menee "läpi" (if-tasolle)
<div id="P57-sortableTrash" class="sortable-code"></div> 
<div id="P57-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P57-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P57-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function remove_duplicate_cchars(str) {\n" +
    "  var arr_char = str.split(\"\"); \\n var result_arr = []; \\n \n" +
    "  for (var i = 0; i < arr_char.length; i++) {\n" +
    "    if (str.indexOf(arr_char[i]) === str.lastIndexOf(arr_char[i]))\n" +
    "      result_arr.push(arr_char[i]);\n" +
    "    }\n" +
    "  return result_arr.join(\"\");\n" +
    "} \\n console.log(remove_duplicate_cchars(\"abcdabc\")); \\n console.log(remove_duplicate_cchars(\"python\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P57-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P57-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P57-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P57-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script> 


---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 50
Järjestä koodirivit ohjelmaksi joka tarkastaa annetusta lukuarvosta, että onko jokainen yksittäinen numero pienempi kuin seuraava numero, eli onko lukuarvon yksittäiset numerot kasvavassa järjestyksessä. 

<div id="P50-sortableTrash" class="sortable-code"></div> 
<div id="P50-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P50-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P50-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function is_increasing_digits_Sequence(num) {\n" +
    "  var arr_num = ('' + num).split('');\n" +
    "  for (var i = 0; i < arr_num.length - 1; i++) {\n" +
    "    if (parseInt(arr_num[i]) >= parseInt(arr_num[i + 1]))\n" +
    "      return false;\n" +
    "  }\n" +
    "  return true;\n" +
    "} \\n console.log(is_increasing_digits_Sequence(123)); \\n console.log(is_increasing_digits_Sequence(1223)); \\n console.log(is_increasing_digits_Sequence(45677)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P50-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P50-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P50-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P50-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



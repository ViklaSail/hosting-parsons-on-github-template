---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 32
Järjestä koodirivit ohjelmaksi jolle annetaan parametriksi taulukko ja integer luku kuvaamaan monenneksiko suurinta alkiota taulukosta haetaan. Ohjelma hakee palauttaa tuon alkion. 
<div id="P32-sortableTrash" class="sortable-code"></div> 
<div id="P32-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P32-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P32-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function Kth_greatest_in_array(arr, k) {\n" +
    "  for (var i = 0; i < k; i++) {\n" +
    "    var max_index = i, tmp = arr[i];\n" +
    "    for (var j = i + 1; j < arr.length; j++) {\n" +
    "      if (arr[j] > arr[max_index]) {\n" +
    "        max_index = j;\n" +
    "      }\n" +
    "    }\n" +
    "    arr[i] = arr[max_index];\n" +
    "    arr[max_index] = tmp;\n" +
    "  }\n" +
    "  return arr[k - 1];\n" +
    "} \\n console.log(Kth_greatest_in_array([1,2,6,4,5], 3)) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P32-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P32-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P32-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P32-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>





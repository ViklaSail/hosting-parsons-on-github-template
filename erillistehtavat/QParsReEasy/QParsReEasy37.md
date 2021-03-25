---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 37
Järjestä koodirivit ohjelmaksi joka laskee parametrina saadun taulukon vierekkäisten alkioiden erot. Sitten se laskee nuo erot yhteen ja palauttaa summan. 
<div id="P37-sortableTrash" class="sortable-code"></div> 
<div id="P37-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P37-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P37-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sum_adjacent_difference(arr) {\n" +
    "	var result = 0;\n" +
    "	for (var i = 1; i < arr.length; i++) {\n" +
    "		result += Math.abs(arr[i] - arr[i - 1]);\n" +
    "	}\n" +
    "	return result;\n" +
    "} \\n console.log(sum_adjacent_difference([1, 2, 3, 2, -5])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P37-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P37-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P37-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P37-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


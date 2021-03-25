---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)



## tehtävä 41
Järjestä koodirivit ohjelmaksi joka tarkastaa kahdesta taulukosta onko niissä ainakin yksi yhteinen elementti. 
<div id="P41-sortableTrash" class="sortable-code"></div> 
<div id="P41-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P41-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P41-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check_common_element(arra1, arra2) {\n" +
    "  for (var i = 0; i < arra1.length; i++)\n" +
    "  {\n" +
    "    if (arra2.indexOf(arra1[i]) != -1) \n" +
    "      return true;\n" +
    "  }\n" +
    "  return false;\n" +
    "} \\n console.log(check_common_element([1,2,3], [3,4,5]));  \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P41-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P41-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P41-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P41-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


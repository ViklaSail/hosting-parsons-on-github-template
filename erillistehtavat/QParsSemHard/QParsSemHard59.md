---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)



## tehtävä 59
Järjestä koodirivit ohjelmaksi. Funktio saa parametriksi kaksi taulukkoa ja laskee kuinka monta taulukon elementtiä löytyy molemmista taulukoista. 
<div id="P59-sortableTrash" class="sortable-code"></div> 
<div id="P59-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P59-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P59-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function test_same_elements_both_arrays(arra1, arra2) {\n" +
    "  let result = 0;\n" +
    "  for(let i = 0; i < arra1.length; i++) {\n" +
    "    for(let j = 0; j < arra2.length; j++){\n" +
    "      if(arra1[i] === arra2[j])\n" +
    "      {\n" +
    "        result++;\n" +
    "      }\n" +
    "    }\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(test_same_elements_both_arrays([1,2,3,4], [1,2,3,4])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P59-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P59-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P59-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P59-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

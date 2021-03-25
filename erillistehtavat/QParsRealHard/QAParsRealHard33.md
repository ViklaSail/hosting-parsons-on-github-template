---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 33
Järjestä koodirivit ohjelmaksi joka saa parametriksi taulukon ja integer-numeron kuvaamaan montako peräkkäistä alkiota halutaan summata. Ohjelma hakee suurinta mahdollista peräkkäisten lukujen summaa ja palauttaa sen. 
liian vaikea? 
<div id="P33-sortableTrash" class="sortable-code"></div> 
<div id="P33-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P33-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P33-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function array_max_consecutive_sum(nums, k) {\n" +
    "  let result = 0; \\n let temp_sum = 0; \\n \n" +
    "  for (var i = 0; i < k - 1; i++) {\n" +
    "    temp_sum += nums[i];\n" +
    "  }\n" +
    "  for (var i = k - 1; i < nums.length; i++) {\n" +
    "    temp_sum += nums[i];\n" +
    "    if (temp_sum > result) {\n" +
    "      result = temp_sum;\n" +
    "    }\n" +
    "    temp_sum -= nums[i - k + 1];\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(array_max_consecutive_sum([1, 2, 3, 14, 5], 2)) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P33-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P33-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P33-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P33-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


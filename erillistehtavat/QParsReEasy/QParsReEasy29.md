---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)



## tehtävä 29
Järjestä koodirivit ohjelmaksi joka saa parametriksi listan numeroita. Ohjelma vertaa listan ensimmäistä ja viimeistä numeroa ja palauttaa true jos ne ovat samat. listassa pitäisi siis olla vähintään kaksi numeroa.

<div id="P29-sortableTrash" class="sortable-code"></div> 
<div id="P29-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P29-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P29-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function first_last_same(nums)\n" +
    "{\n" +
    "    var end = nums.length - 1;\n" +
    "    if (nums.length >= 1){\n" +
    "       return nums[0] == nums[end];\n" +
    "    } else {return false;}\n" +
    "} \\n console.log(first_last_same([10, 20, 30]));  \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P29-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P29-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P29-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P29-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

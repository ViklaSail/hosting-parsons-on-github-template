---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 31
Järjestä koodirivit ohjelmaksi joka saa parametriksi 3 alkioisen taulukon ja muodostaa uuden taulukon parametritaulukon ensimmäisesta ja viimeisestä alkiosta. Lopuksi uusi taulukko palautetaan. 
<div id="P31-sortableTrash" class="sortable-code"></div> 
<div id="P31-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P31-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P31-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function started(nums) {\n" +
    "     var array1 = [];\n" +
    "     array1.push(nums[0], nums[nums.length - 1]);\n" +
    "     return array1;\n" +
    "} \\n console.log(started([20, 20, 30])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P31-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P31-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P31-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P31-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



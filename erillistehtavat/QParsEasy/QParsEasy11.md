---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 11
Järjestä koodirivit ohjelmaksi, joka saa parametrina merkkijonon, lisää merkkijonon ensimmäisen kirjaimen sen alkuun ja loppuun sekä palauttaa uuden merkkijonon. 
<div id="P11-sortableTrash" class="sortable-code"></div> 
<div id="P11-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P11-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P11-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function front_back(str)\n" +
    "{\n" +
    "  first = str.substring(0,1);\n" +
    "  return first + str + first;\n" +
    "} \\n console.log(front_back('a')); \\n console.log(front_back('ab')); \\n console.log(front_back('abc')); \\n \n" +
    "first = str.substring(0,2); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P11-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P11-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P11-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P11-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


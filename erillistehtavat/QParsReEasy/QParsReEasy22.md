---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 22
Järjestä koodirivit erikoislaskimeksi joka laskee kaksi lukua yhteen ja palauttaa 65 jos summa on 50 ja 80 välillä. Muutoin palautetaan 80
<div id="P22-sortableTrash" class="sortable-code"></div> 
<div id="P22-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P22-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P22-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sortaSum(x, y) \n" +
    "{\n" +
    "  const sum_nums = x + y;\n" +
    "  if (sum_nums >= 50 && sum_nums <= 80) {\n" +
    "    return 65;\n" +
    "  }\n" +
    "  return 80;\n" +
    "} \\n console.log(sortaSum(30,20)); \\n console.log(sortaSum(90,80)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P22-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P22-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P22-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P22-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



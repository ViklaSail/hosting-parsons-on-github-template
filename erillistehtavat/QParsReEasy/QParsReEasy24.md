---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 24
Järjestä koodirivit ohjelmaksi joka saa 3 numeroa. jos kaikki 3 numeroa ovat samoja palautetaan 30, muutoin palautetaan 20. Jos kaksi ensin annettua numeroa ovat samoja, palautetaan 40. 
Check three given numbers, if the three numbers are same return 30 otherwise return 20 and if two numbers are same return 40 
<div id="P24-sortableTrash" class="sortable-code"></div> 
<div id="P24-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P24-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P24-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function three_numbers(x, y, z) {\n" +
    "  if (x == y && y == z) {\n" +
    "    return 30;\n" +
    "  } \\n if (x == y || y == z || z == x) { \\n \n" +
    "    return 40;\n" +
    "  }\n" +
    "  return 20;\n" +
    "} \\n console.log(three_numbers(8, 8, 8)); \\n console.log(three_numbers(8, 8, 18)); \\n console.log(three_numbers(8, 7, 18)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P24-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P24-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P24-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P24-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



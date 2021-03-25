---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 15
Järjestä koodirivit ohjelmaksi joka tarkastaa että kaksi annettua lukua on arvoalueella 50..99. Jos jonpi kumpi annetuista luvuista on mainitulla arvo-alueella, palautetaan true. 

<div id="P15-sortableTrash" class="sortable-code"></div> 
<div id="P15-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P15-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P15-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check_numbers(x, y) \n" +
    "{\n" +
    "  if ((x >= 50 && x <= 99) || (y >= 50 && y <= 99))\n" +
    "  {\n" +
    "    return true;\n" +
    "  } \n" +
    "  else \n" +
    "  {\n" +
    "    return false;\n" +
    "  }\n" +
    "} \\n console.log(check_numbers(12, 101)); \\n console.log(check_numbers(52, 80)); \\n console.log(check_numbers(15, 99)); \\n \n" +
    "if ((x <= 50 && x <= 99) || (y >= 50 && y <= 99)) #distractor\n" +
    "if ((x >= 50 && x >= 99) || (y <= 50 && y >= 99)) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P15-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P15-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P15-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P15-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>




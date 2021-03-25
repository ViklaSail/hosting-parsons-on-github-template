---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 16
Järjestä koodirivit ohjelmaksi joka palauttaa annetuista kolmesta luvusta suurimman. käytä kaikki sulkeet. max_val = 0 asetuksesta puuttuu var tai let alusta, älä välitä siitä. Pari harhautusblokkia.

<div id="P16-sortableTrash" class="sortable-code"></div> 
<div id="P16-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P16-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P16-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function max_of_three(x, y, z) \n" +
    "{\n" +
    "  max_val = 0;\n" +
    "  if (x > y)\n" +
    "  {\n" +
    "    max_val = x;\n" +
    "  } else\n" +
    "  {\n" +
    "    max_val = y;\n" +
    "  }\n" +
    "  if (z > max_val) \n" +
    "  {\n" +
    "    max_val = z;\n" +
    "  }\n" +
    "  return max_val;\n" +
    "} \\n console.log(max_of_three(1,0,1)); \\n console.log(max_of_three(0,-10,-20)); \\n console.log(max_of_three(1000,510,440)); \\n \n" +
    "if ((x <= 50 && x <= 99) || (y >= 50 && y <= 99)) #distractor\n" +
    "if ((x >= 50 && x >= 99) || (y <= 50 && y >= 99)) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P16-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P16-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P16-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P16-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 45
Järjestä koodirivit ohjelmaksi joka saa parametrina jaettavan numeron ja jakajan. 
Jos jakaja on 1, palautetaan jaettava numero. 
Muussa tapauksessa Ohjelma jakaa jaettavan jakajalla niin monta kertaa kuin jako menee tasan ja tallentaa tuloksen uudelleen jaettavaksi. 
Kun jako ei enää mene tasan, palautetaan tulos. Jakojäännöksen saa % operaattorilla. 


<div id="P45-sortableTrash" class="sortable-code"></div> 
<div id="P45-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P45-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P45-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function divide_digit(num, d) {\n" +
    "  if (d==1)\n" +
    "    return num;\n" +
    "  else {\n" +
    "    while (num % d === 0) {\n" +
    "      num = num / d;\n" +
    "    }\n" +
    "    return num;\n" +
    "  }\n" +
    "} \\n console.log(divide_digit(-12, 2)) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P45-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P45-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P45-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P45-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



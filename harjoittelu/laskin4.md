---
layout: default
title: Harjoittelutehtävä
---
### Laskimen osa 4
Kysyy prompt-ikkunassa luvun. TArkistaa onko kyseessä luku ja kysyy uutta lukua kunnes käyttäjä antaa oikeasti luvun. 
<div id="pre3-sortableTrash" class="sortable-code"></div> 
<div id="pre3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="pre3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="pre3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function kysyLuku(valitulos,operaattori){\n" +
    "   var luku = prompt(&quot;anna luku &quot;+valitulos+operaattori);\n" +
    "   var tulos = konvertoiNumeroksi(luku);\n" +
    "   while(isNaN(tulos))\n" +
    "   {\n" +
    "       luku = prompt(&quot;Ei ollut luku, anna luku &quot;+valitulos+operaattori);\n" +
    "       tulos = konvertoiNumeroksi(luku);\n" +
    "   }\n" +
    "   return tulos;\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "pre3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#pre3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#pre3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

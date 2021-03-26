---
layout: default
title: Harjoittelutehtävä
---

## LASKIMEN OSA 5
Kysy operaattori-funktio kysyy nelilaskimen laskutoimitusta kunnes käyttäjä antaa "laillisen" laskutoimituksen. 

<div id="pre4-sortableTrash" class="sortable-code"></div> 
<div id="pre4-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="pre4-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="pre4-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function kysyOperaattori(operandi){\n" +
    "   var operaattori = prompt(&quot;anna laskutoimitus &quot;+operandi);\n" +
    "   var validi = tarkastaLaskutoimitus(operaattori);\n" +
    "   while(!validi){\n" +
    "     operaattori = prompt(&quot;Virheellinen syöte, anna laskutoimitus &bsol;n &quot;+operandi);\n" +
    "     validi = tarkastaLaskutoimitus(operaattori);\n" +
    "   }\n" +
    "   return operaattori\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "pre4-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#pre4-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#pre4-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


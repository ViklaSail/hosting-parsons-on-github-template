---
layout: default
title: Harjoittelutehtävä
---
### laskimen osa 3
Muuttaa merkkijonon numeroksi. Jos se ei onnistu palauttaa merkkijonon NaN. 
<div id="pre2-sortableTrash" class="sortable-code"></div> 
<div id="pre2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="pre2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="pre2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function konvertoiNumeroksi(luku){\n" +
    "    var result = NaN;\n" +
    "    if(isNaN(luku)){\n" +
    "        result = NaN;\n" +
    "    } else {\n" +
    "        result = parseInt(luku);\n" +
    "    }\n" +
    "    return result\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "pre2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#pre2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#pre2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

---
layout: default
title: Harjoittelutehtävä
---
### laskimen osa 2
Saa parametrina laskutoimituksen ja tarkistaa sopiiko se nelilaskimen sallittuihin operaatioihin. Palauttaa totuusarvon. 

<div id="pre1-sortableTrash" class="sortable-code"></div> 
<div id="pre1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="pre1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="pre1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function tarkastaLaskutoimitus(operaattori){\n" +
    "    var operators = [&quot;+&quot;, &quot;-&quot;, &quot;*&quot;, &quot;/&quot;,&quot;L&quot;];\n" +
    "    var isValid = operators.includes(operaattori);\n" +
    "    return isValid\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "pre1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#pre1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#pre1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
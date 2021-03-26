
---
layout: default
title: Harjoittelutehtävä
---

# Parsons laskin 1
Laskin kysyy luvun (operandi1) ja operaation (operaattori) kunnes saa operaattoriksi lopetusmerkin "L".
Laskin käyttää edellisen laskutoimituksen tulosta seuraavan laskemiseen. Välitulos talletetaan operandi1-muuttujaan. 
Lopuksi tulostetaan lopullinen tulos konsoliin.     
Tässä tehtävässä on yksi virhe: muuttuja

<div id="pekka1-sortableTrash" class="sortable-code"></div> 
<div id="pekka1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="pekka1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="pekka1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function laskin(){\n    var operaattori = &quot;&quot;;\n" +
    "    var operandi1 = kysyLuku(&quot;0&quot;,operaattori);\n" +
    "    while (operaattori != &quot;L&quot;) {\n" +
    "        operaattori = kysyOperaattori(operandi1);\n" +
    "        if (operaattori != &quot;L&quot;){\n" +
    "          operandi2 = kysyLuku(operandi1,operaattori);\n" +
    "          operandi1 = laske(operandi1,operaattori,operandi2)\n" +
    "        }\n" +
    "    }\n" +
    "    return operandi1;\n" +
    "}\n" +
    "console.log(laskin());";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "pekka1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#pekka1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#pekka1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

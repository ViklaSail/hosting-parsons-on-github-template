---


layout: default
title: Harjoittelutehtäviä
---
# Parsons oma kokeilu
Laskin kysyy luvun (operandi1) ja operaation (operaattori) kunnes saa operaattoriksi lopetusmerkin "L".
Laskin käyttää edellisen laskutoimituksen tulosta seuraavan laskemiseen. Välitulos talletetaan operandi1-muuttujaan. 
Lopuksi tulostetaan lopullinen tulos konsoliin.

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

### laskimen osa 1
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

### laskimen osa 2
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

### Laskimen osa 3
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

## LASKIMEN OSA 4
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

# PARSONS PUZZLE BLOKKIKOKEILU
Ei ruksia html-kohdassa pre5. LISÄKSI UUSI KOODI. kaikki js-osoitteet vaihdettu
<div id="pre5-sortableTrash" class="sortable-code"></div> 
<div id="pre5-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="pre5-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="pre5-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "var aika = new Date();\nvar paiva = aika.getDate();\n" +
    "document.write(&quot;Nyt on &quot; + paiva + &quot;.&quot; + kuukausi + &quot;.&quot; + vuosi + &quot; ja kello on &quot; + tunnit + &quot;:&quot; + minuutit + &quot;:&quot; + sekunnit + &quot;.&quot;);";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "pre5-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#pre5-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#pre5-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
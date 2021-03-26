---


layout: default
title: Harjoittelutehtäviä
---






# PARSONS PUZZLE kokeilu
Laita rivit järkevään järjestykseen

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
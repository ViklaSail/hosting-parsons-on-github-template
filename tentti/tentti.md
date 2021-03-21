---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons puzle tentti

# konvertoi celcius-asteet fahrenheiteiksi

<div id="P1-sortableTrash" class="sortable-code"></div> 
<div id="P1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function cToF(celsius) \n" +
    "{\n" +
    "  var cTemp = celsius;\n" +
    "  var cToFahr = cTemp * 9 / 5 + 32;\n" +
    "  var message = cTemp+'\xB0C is ' + cToFahr + ' \xB0F.';\n" +
    "  console.log(message);\n" +
    "} \\n cToF(60); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
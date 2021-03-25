---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 64
Järjestä koodirivit ohjelmaksi. Funktio saa parametrina merkkijonon ja vaihtaa siitä isot kirjamet pieniksi sekä pienet isoiksi. 

<div id="P64-sortableTrash" class="sortable-code"></div> 
<div id="P64-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P64-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P64-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function change_case(txt) {\n" +
    "    var str1 = \"\";\n" +
    "    for (var i = 0; i < txt.length; i++) {\n" +
    "        if (/[A-Z]/.test(txt[i])) str1 += txt[i].toLowerCase();\n" +
    "        else str1 += txt[i].toUpperCase();\n" +
    "    }\n" +
    "    return str1;\n" +
    "} \\n console.log(change_case(\"testiMERKKI\")); \\n console.log(change_case(\"Germany\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P64-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P64-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P64-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P64-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>






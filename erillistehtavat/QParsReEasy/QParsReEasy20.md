---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 20
Järjestä koodirivit ohjelmaksi joka luo parametrina saadusta merkkijonosta uuden niin että kolme ensimmäistä merkkiä on pienillä kirjaimilla. Jos saadun merkkijonon pituus on vähemmän kuin 3 merkkiä, muuta kaikki kirjaimet isoiksi. 
<div id="P20-sortableTrash" class="sortable-code"></div> 
<div id="P20-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P20-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P20-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function upper_lower(str) {\n" +
    "  if (str.length < 3) {\n" +
    "    return str.toUpperCase();\n" +
    "  }\n" +
    "  front_part = (str.substring(0, 3)).toLowerCase(); \\n back_part = str.substring(3, str.length);   \\n \n" +
    "  return front_part + back_part;\n" +
    "} \\n console.log(upper_lower(\"Python\")); \\n console.log(upper_lower(\"Py\")); \\n console.log(upper_lower(\"JAVAScript\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P20-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P20-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P20-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P20-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 8
Järjestä koodirivit ohjelmaksi jolle annetaan parametrina merkkijono ja joka muodostaa siitä uuden merkkijonon lisäämällä alkuun "Py" merkkijonon. Jos merkkijono jo alkoin kirjaimilla "Py" palautetaan alkuperäinen merkkijono. 
 program to create a new string adding "Py" in front of a given string. If the given string begins with "Py" then return the original string.
<div id="P8-sortableTrash" class="sortable-code"></div> 
<div id="P8-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P8-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P8-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function string_check(str1) {\n" +
    "  if (str1 === null || str1 === undefined || str1.substring(0, 2) === 'Py') \n" +
    "  {\n" +
    "    return str1;\n" +
    "  }\n" +
    "  return \"Py\"+str1;\n" +
    "} \\n console.log(string_check(\"Python\")); \\n console.log(string_check(\"thon\")); \\n \n" +
    "  if (n >= 19) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P8-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P8-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P8-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P8-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



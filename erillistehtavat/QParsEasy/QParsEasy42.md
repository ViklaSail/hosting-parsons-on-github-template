---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 42
Järjestä koodirivit ohjelmaksi joka laskee lukuja sisältävän taulukon inversioiden määrän. Inversio tarkoittaa tilannetta jossa listan luvut eivät ole luonnollisessa suuruusjärjestyksessä. (ohje: älä mieti käsitettä inversio, mieti vain missä järjestyksessä koodin on oltava muuttujien esittelyn ja käytön perusteella)
<div id="P42-sortableTrash" class="sortable-code"></div> 
<div id="P42-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P42-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P42-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function number_of_InversionsNaive(arr) {\n" +
    "    var ctr = 0;\n" +
    "    for (var i = 0; i < arr.length; i++) {\n" +
    "        for (var j = i + 1; j < arr.length; j++) {\n" +
    "            if (arr[i] > arr[j]) \n" +
    "              ctr++;\n" +
    "        }\n" +
    "    }\n" +
    "    return ctr;\n" +
    "} \\n console.log(number_of_InversionsNaive([0, 3, 2, 5, 9]));    \\n console.log(number_of_InversionsNaive([1, 5, 4, 3]));    \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P42-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P42-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P42-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P42-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>





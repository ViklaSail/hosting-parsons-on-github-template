---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 3: Päivittelyä
Seuraava ohjelma tarkasta onko tammikuun ensimmäinen päivä sunnuntai vuosien 2014 ja 2050 väliltä, ja tulostaa lokiin päivän jos näin on. 


<div id="P3-sortableTrash" class="sortable-code"></div> 
<div id="P3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for (var year = 2014; year <= 2050; year++)\n" +
    "{\n" +
    "    var d = new Date(year, 0, 1);\n" +
    "    if ( d.getDay() === 0 )\n" +
    "        console.log(\"1st January is being a Sunday  \"+year);\n" +
    "}\n" +
    "var a = new Date(year, 0, 1); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P3-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


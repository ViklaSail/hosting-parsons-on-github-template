---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 21
Järjestä koodirivit ohjelmaksi joka tarkistaa saako opiskelija arvosanan A+. Opiskelija saa A+ arvosanan kun kokeen pisteet ovat välillä 89-100, silloin kun on kyse tavallisesta tehtävästä. Jos kyse on "loppukokeesta, A+ raja on tiukempi, ja opiskelijan pitää saada vähintään 90 pistettä saadakseen A+. Ohjelmalle annetaan pisteet ja tieto siitä onko kyse loppukokeesta ja ohjelma palauttaa totuusarvon true mikäli opiskelija on saamassa A+ 

<div id="P21-sortableTrash" class="sortable-code"></div> 
<div id="P21-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P21-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P21-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function exam_status(totmarks,is_exam)\n" +
    "{\n" +
    "  if (is_exam) {\n" +
    "    return totmarks >= 90;\n" +
    "  }\n" +
    "  return (totmarks >= 89 && totmarks <= 100);\n" +
    "} \\n console.log(exam_status(\"78\", \" \")); \\n console.log(exam_status(\"89\", \"true \")); \\n console.log(exam_status(\"99\", \"true \")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P21-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P21-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P21-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P21-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



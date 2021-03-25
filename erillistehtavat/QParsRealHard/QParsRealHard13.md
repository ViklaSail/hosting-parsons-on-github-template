---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 13
Järjestä koodirivit ohjelmaksi joka lisää annetun merkkijonon 3 viimeistä merkkiä annetun mekkijonon alkuun ja loppuun. Annetun merkkijonon pituuden on oltava suurempi kuin kolme. 
Ratkaisussa on virhe, str_len pitää laittaa if-lauseen alkuun, vaikkei sitä käytetäkkään. 

<div id="P13-sortableTrash" class="sortable-code"></div> 
<div id="P13-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P13-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P13-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function front_back3(str)\n" +
    "{\n" +
    "  if (str.length>=3)\n" +
    "  {\n" +
    "    str_len = 3;\n" +
    "    back = str.substring(str.length-3);\n" +
    "    return back + str + back;\n" +
    "  } else\n" +
    "    return false;\n" +
    "} \\n console.log(front_back3(\"abc\")); \\n console.log(front_back3(\"ab\")); \\n console.log(front_back3(\"abcd\")); \\n \n" +
    "back2 = str.substring(str.length-4); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P13-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P13-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P13-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P13-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>




---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 27
Järjestä koodirivit ohjelmaksi joka saa parametriksi merkkijonon. Jos merkkijonon pituus on pariton luku ja suurempi kuin 3, luodaan uusi merkkijono ottamalla kolme keskimmäistä merkkiä parametrina saadusta merkkijonosta. Muussa tapauksessa palautetaan alkuperäinen merkkijono. 

<div id="P27-sortableTrash" class="sortable-code"></div> 
<div id="P27-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P27-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P27-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function middle_three(str) {\n" +
    "  if (str.length % 2!= 0) {\n" +
    "    mid = (str.length + 1)/2;\n" +
    "    return str.slice(mid - 2, mid + 1);\n" +
    "  }\n" +
    "  return str;\n" +
    "} \\n console.log(middle_three('abcdefg')); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P27-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P27-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P27-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P27-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>




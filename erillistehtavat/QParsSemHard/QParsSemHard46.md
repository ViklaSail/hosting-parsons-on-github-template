---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)



## tehtävä 46
Järjestä koodirivit ohjelmaksi joka saa parametriksi listan numeroita ja muodostaa listan numeroista jakava-jaettava-pareja joissa jako menee tasan. Muodostetaan niin monta paria kuin mahdollista. Palautetaan muodostettujen parien lukumäärä. 
<div id="P46-sortableTrash" class="sortable-code"></div> 
<div id="P46-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P46-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P46-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function arr_pairs(arr) {\n" +
    "    var result = 0;\n" +
    "    for (var i = 0; i < arr.length; i++)\n" +
    "    {\n" +
    "      for (var j = i + 1; j < arr.length; j++)\n" +
    "      {\n" +
    "         if (arr[i] % arr[j] === 0 || arr[j] % arr[i] === 0)\n" +
    "         {\n" +
    "           result++;\n" +
    "         }\n" +
    "      }\n" +
    "    }\n" +
    "    return result;\n" +
    "} \\n console.log(arr_pairs([1,2,3]))// tulostaa 2   \\n console.log(arr_pairs([2,4,6]))// tulostaa 2 \\n console.log(arr_pairs([2,4,16]))// tulostaa 3  \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P46-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P46-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P46-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P46-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 36
Järjestä koodirivit ohjelmaksi joka etsii kokonaislukutaulukosta parametrina annettua lukua ja korvaa sen toisella parametrina annetulla luvulla. 

<div id="P36-sortableTrash" class="sortable-code"></div> 
<div id="P36-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P36-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P36-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function array_element_replace(arr, old_value, new_value) {\n" +
    "  for (var i = 0; i < arr.length; i++) {\n" +
    "    if (arr[i] === old_value) {\n" +
    "      arr[i] = new_value;\n" +
    "    }\n" +
    "  }\n" +
    "  return arr;\n" +
    "}\n" +
    "num = [1, 2, 3, 2, 2, 8, 1, 9];\n" +
    "console.log(\"Original Array: \"+num); \\n console.log(array_element_replace(num, 2, 5)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P36-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P36-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P36-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P36-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


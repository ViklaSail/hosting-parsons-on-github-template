---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 44
Järjestä koodirivit ohjelmaksi joka etsii parametrina annetusta numerolistasta sellaisen numeroparin joiden absoluuttinen ero ei ole suurempi kuin toisena parametrina annettu lukuarvo mutta samanaikaisesti ero on mahdollisimman lähellä sitä toisena parametrina annettua lukuarvoa. 

<div id="P44-sortableTrash" class="sortable-code"></div> 
<div id="P44-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P44-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P44-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function different_values(ara, n) {\n" +
    "    var max_val = -1;\n" +
    "    for (var i = 0; i < ara.length; i++) {\n" +
    "        for (var j = i + 1; j < ara.length; j++) {\n" +
    "            var x = Math.abs(ara[i] - ara[j]);\n" +
    "            if (x <= n) {\n" +
    "                max_val = Math.max(max_val, x)\n" +
    "            }\n" +
    "        }\n" +
    "    }\n" +
    "    return max_val\n" +
    "} \\n console.log(different_values([12, 10, 33, 34], 10)); \\n console.log(different_values([12, 10, 33, 34], 24)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P44-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P44-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P44-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P44-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


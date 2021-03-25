---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 30
Järjestä koodirivit ohjelmaksi joka saa parametriksi kaksi kolmen alkion pituista taulukkoa ja tekee uuden taulukon ottamalla keskimmäiset alkioit parametritaulukoista ja lisäämällä ne uuden taulukon alkioiksi
<div id="P30-sortableTrash" class="sortable-code"></div> 
<div id="P30-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P30-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P30-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function middle_elements(a, b) \n" +
    "{\n" +
    "  var new_array = []\n" +
    "  new_array.push(a[1], b[1]);\n" +
    "  return new_array;\n" +
    "} \\n console.log(middle_elements([1, 2, 3], [1, 5, 6]));   \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P30-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P30-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P30-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P30-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



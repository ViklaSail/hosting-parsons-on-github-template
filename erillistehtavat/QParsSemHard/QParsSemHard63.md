---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)


## tehtävä 63
Järjestä koodirivit ohjelmaksi. Funktio saa taulukon jossa on numeroita. jos taulukon pituus  on parillinen luku, esim 4, funktio vaihtaa taulukon alkupään ja loppypään paikkaa. Jos taulukko on [1,2,3,4], siitä tulee [3,4,1,2]. jos taulukon pituus on pariton luku, esim 5, palautetaan false. 
<div id="P63-sortableTrash" class="sortable-code"></div> 
<div id="P63-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P63-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P63-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function halv_array_swap(iarra) {\n" +
    "  if (((iarra.length)%2)!=0)\n" +
    "  {\n" +
    "    return false;\n" +
    "  }\n" +
    "  for (var i = 0; i < iarra.length / 2; i++) {\n" +
    "    var tmp = iarra[i];\n" +
    "    iarra[i] = iarra[i + iarra.length / 2];\n" +
    "    iarra[i + iarra.length / 2] = tmp;\n" +
    "  }\n" +
    "  return iarra;\n" +
    "} \\n console.log(halv_array_swap([1,2,3,4,5,6])) \\n console.log(halv_array_swap([1,2,3,4,5,6,7])) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P63-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P63-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P63-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P63-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


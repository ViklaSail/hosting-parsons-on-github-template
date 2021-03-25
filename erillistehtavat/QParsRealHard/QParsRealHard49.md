---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## tehtävä 49
Järjestä koodirivit ohjelmaksi jolle annetaan parametriksi lista numeroita ja numero. Ohjelma laskee montako parillista numeroa listalla on ennen toisena parametrina ennettua numeroa. Jos parametriksi annetaan tyhjä lista, ohjelma palauttaa -1.  
esimerkki-lista: [1,2,3,4,5,6,7,8]    
annettu numero: 5   
palautettu lukumäärä: 2    

<div id="P49-sortableTrash" class="sortable-code"></div> 
<div id="P49-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P49-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P49-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function find_numbers(arr_num, num) {\n" +
    "    var result = 0;\n" +
    "    for (var i = 0; i < arr_num.length; i++)\n" +
    "    {\n" +
    "        if (arr_num[i] % 2 === 0 && arr_num[i] !== num) {\n" +
    "            result++;\n" +
    "        } \\n if (arr_num[i] === num) \\n { \\n     return result; \\n } \\n \n" +
    "    }\n" +
    "    return -1;\n" +
    "} \\n console.log(find_numbers([1,2,3,4,5,6,7,8], 5)) \\n console.log(find_numbers([1,3,5,6,7,8], 6)) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P49-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P49-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P49-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P49-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>




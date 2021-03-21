---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons puzle tentti

## Tehtävä 1: konvertoi celcius-asteet fahrenheiteiksi

<div id="P1-sortableTrash" class="sortable-code"></div> 
<div id="P1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function cToF(celsius) \n" +
    "{\n" +
    "  var cTemp = celsius;\n" +
    "  var cToFahr = cTemp * 9 / 5 + 32;\n" +
    "  var message = cTemp+'\xB0C is ' + cToFahr + ' \xB0F.';\n" +
    "  console.log(message);\n" +
    "} \\n cToF(60); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Tehtävä 2: Laskee kolmion alan
Sivujen pituudet ovat 5,6 ja 7. 
Tehtävä sisältää kaksi "harhautusriviä" jotka eivät kuulu ohjelmaan. Kokoa ohjelman rivit alla olevaan laatikkoon. 

<div id="P2-sortableTrash" class="sortable-code"></div> 
<div id="P2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "var side1 = 5;  \\n var side2 = 6;  \\n var side3 = 7;  \\n \n" +
    "var s = (side1 + side2 + side3)/2;\n" +
    "var area =  Math.sqrt(s*((s-side1)*(s-side2)*(s-side3)));\n" +
    "console.log(area);\n" +
    "var a = (side1 + side2 + side3); #distractor\n" +
    "var b = a/2; #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 3: Päivittelyä
Seuraava ohjelma tarkasta onko tammikuun ensimmäinen päivä sunnuntai vuosien 2014 ja 2050 väliltä, ja tulostaa päivän jos näin on. 


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

## tehtävä 4: arpoo numeron 1 ja 10 väliltä, 
pyytää käyttäjää arvaamaan mikä se oli, tulostaa arvattiinko oikein ja arvotun numeron jos arvaus ei ollut oikea. 
<div id="P4-sortableTrash" class="sortable-code"></div> 
<div id="P4-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P4-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P4-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "const num = Math.ceil(Math.random() * 10); \\n console.log(num); \\n const gnum = prompt('Arvaa numero 1 ja 10 väliltä'); \\n \n" +
    "if (gnum == num)\n" +
    "   console.log('Arvasit oikein');\n" +
    "else\n" +
    "   console.log('Väärin, numero oli '+gnum);\n" +
    "console.log(aNum); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P4-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P4-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P4-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P4-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 5
Javascript funktio näyttää eroaako parametrina annettu luku luvusta 13 ja tulostaa erotuksen. 
jos annettu luku on suurempi kuin 13 ohjelma palauttaa eron kerrottuna kahdella.
<div id="P5-sortableTrash" class="sortable-code"></div> 
<div id="P5-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P5-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P5-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function difference(n)\n" +
    "{\n" +
    "    if (n <= 13)\n" +
    "        return 13 - n;\n" +
    "    else\n" +
    "        return (n - 13) * 2;\n" +
    "}\n" +
    "console.log(difference(32)) \\n console.log(difference(11)) \\n \n" +
    "console.log(aNum); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P5-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P5-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P5-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P5-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 6
Kokoa riveistä javascript ohjelma joka laskee kahden kokonaisluvun summan. Jos annetut luvut ovat yhtäsuuret, palautetaan niiden summa kerrottuna kolmella

<div id="P6-sortableTrash" class="sortable-code"></div> 
<div id="P6-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P6-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P6-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sumTriple (x, y) {\n" +
    "  if (x == y) {\n" +
    "    return 3 * (x + y);\n" +
    "  } else {\n" +
    "    return (x + y);\n" +
    "  }\n" +
    "} \\n console.log(sumTriple(10, 20)); \\n console.log(sumTriple(10, 10)); \\n \n" +
    "  if (x =< y) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P6-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P6-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P6-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P6-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 7
Järjestä seuraavat rivit ohjelmaksi joka laskee parametrina annetun luvun absoluuttisen eron lukuun 19 ja palauttaa sen. Jos annettu luku on suurempi kuin 19, ohjelma palauttaa absoluuttisen eron kolminkertaisena. 
<div id="P7-sortableTrash" class="sortable-code"></div> 
<div id="P7-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P7-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P7-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function diff_num(n) {\n" +
    "  if (n <= 19) {\n" +
    "    return (19 - n);\n" +
    "  } else {\n" +
    "     return (n - 19) * 3;\n" +
    "  }\n" +
    "} \\n console.log(diff_num(12)); \\n console.log(diff_num(19)); \\n console.log(diff_num(22)); \\n \n" +
    "  if (n >= 19) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P7-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P7-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P7-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P7-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 8
Järjestä koodirivit ohjelmaksi jolle annetaan parametrina merkkijono ja joka muodostaa siitä uuden merkkijonon lisäämällä alkuun "Py" merkkijonon. Jos merkkijono jo alkoin kirjaimilla "Py" palautetaan alkuperäinen merkkijono. 
 program to create a new string adding "Py" in front of a given string. If the given string begins with "Py" then return the original string.
<div id="P8-sortableTrash" class="sortable-code"></div> 
<div id="P8-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P8-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P8-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function string_check(str1) {\n" +
    "  if (str1 === null || str1 === undefined || str1.substring(0, 2) === 'Py') \n" +
    "  {\n" +
    "    return str1;\n" +
    "  }\n" +
    "  return \"Py\"+str1;\n" +
    "} \\n console.log(string_check(\"Python\")); \\n console.log(string_check(\"thon\")); \\n \n" +
    "  if (n >= 19) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P8-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P8-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P8-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P8-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 9
Järjestä koodirivit ohjelmaksi joka poistaa parametrina annetusta merkkijonosta toisena parametrina annetusta sijainnista yhden merkin. 
(Tästä voisi tehdä jatkotehtävän, enemmän parametreja, monimutkaisempaa toimintaa)
<div id="P9-sortableTrash" class="sortable-code"></div> 
<div id="P9-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P9-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P9-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function remove_character(str, char_pos) \n" +
    "{\n" +
    "  part1 = str.substring(0, char_pos); \\n part2 = str.substring(char_pos + 1, str.length); \\n \n" +
    "  return (part1 + part2);\n" +
    "} \\n console.log(remove_character(\"Python\",0)); \\n console.log(remove_character(\"Python\",3)); \\n console.log(remove_character(\"Python\",5)); \\n \n" +
    "  if (n >= 19) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P9-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P9-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P9-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P9-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 10
Järjestä koodirivit ohjelmaksi, joka saa parametriksi merkkijonon ja vaihtaa viimeisen ja ensimmäisen merkin paikkoja. Merkkijonon on oltava vähintään yhden merkin pituinen 
<div id="P10-sortableTrash" class="sortable-code"></div> 
<div id="P10-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P10-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P10-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function first_last(str1) \n" +
    "{\n" +
    "  if (str1.length <= 1)\n" +
    "  {\n" +
    "    return str1;\n" +
    "  }\n" +
    "  mid_char = str1.substring(1, str1.length - 1);\n" +
    "  return (str1.charAt(str1.length - 1)) + mid_char + str1.charAt(0);\n" +
    "} \\n console.log(first_last('a')); \\n console.log(first_last('ab')); \\n console.log(first_last('abc')); \\n \n" +
    "  if (n >= 19) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P10-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P10-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P10-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P10-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 11
Järjestä koodirivit ohjelmaksi, joka saa parametrina merkkijonon, lisää merkkijonon ensimmäisen kirjaimen sen alkuun ja loppuun sekä palauttaa uuden merkkijonon. 
<div id="P11-sortableTrash" class="sortable-code"></div> 
<div id="P11-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P11-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P11-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function front_back(str)\n" +
    "{\n" +
    "  first = str.substring(0,1);\n" +
    "  return first + str + first;\n" +
    "} \\n console.log(front_back('a')); \\n console.log(front_back('ab')); \\n console.log(front_back('abc')); \\n \n" +
    "first = str.substring(0,2); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P11-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P11-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P11-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P11-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 12
Järjestä koodirivit ohjelmaksi joka tarkastaa meneekö parametrina annetun luvun jako 3 tai 7 tasan.
<div id="P12-sortableTrash" class="sortable-code"></div> 
<div id="P12-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P12-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P12-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function test37(x) \n" +
    "{\n" +
    "  if (x % 3 == 0 || x % 7 == 0) \n" +
    "  {\n" +
    "    return true;\n" +
    "  } \n" +
    "  else {\n" +
    "    return false;\n" +
    "  }\n" +
    "} \\n console.log(test37(12)); \\n console.log(test37(14)); \\n console.log(test37(10)); \\n console.log(test37(11)); \\n \n" +
    "first = str.substring(0,2); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P12-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P12-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P12-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P12-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



## tehtävä 13
Järjestä koodirivit ohjelmaksi joka lisää annetun merkkijonon 3 viimeistä merkkiä annetun mekkijonon alkuun ja loppuun. Annetun merkkijonon pituuden on oltava suurempi kuin kolme. 

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
## tehtävä 14
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 14
Järjestä koodirivit ohjelmaksi joka tarkastaa onko annetun merkkijonon alussa sana "java" ja siinä tapauksessa palauttaa arvon true. 
<div id="P14-sortableTrash" class="sortable-code"></div> 
<div id="P14-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P14-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P14-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function start_spec_str(str)\n" +
    "{\n" +
    "  if (str.length < 4)\n" +
    "  {\n" +
    "    return false;\n" +
    "  }\n" +
    "  front = str.substring(0, 4);\n" +
    "  if (front == 'Java') \n" +
    "  {\n" +
    "    return true;\n" +
    "  }\n" +
    "  else \n" +
    "  {\n" +
    "    return false;\n" +
    "  }\n" +
    "} \\n console.log(start_spec_str(\"JavaScript\")); \\n console.log(start_spec_str(\"Java\")); \\n console.log(start_spec_str(\"Python\")); \\n \n" +
    "back2 = str.substring(str.length-4); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P14-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P14-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P14-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P14-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 15
Järjestä koodirivit ohjelmaksi joka tarkastaa että kaksi annettua lukua on arvoalueella 50..99. Jos jonpi kumpi annetuista luvuista on mainitulla arvo-alueella, palautetaan true. 

<div id="P15-sortableTrash" class="sortable-code"></div> 
<div id="P15-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P15-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P15-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check_numbers(x, y) \n" +
    "{\n" +
    "  if ((x >= 50 && x <= 99) || (y >= 50 && y <= 99))\n" +
    "  {\n" +
    "    return true;\n" +
    "  } \n" +
    "  else \n" +
    "  {\n" +
    "    return false;\n" +
    "  }\n" +
    "} \\n console.log(check_numbers(12, 101)); \\n console.log(check_numbers(52, 80)); \\n console.log(check_numbers(15, 99)); \\n \n" +
    "if ((x <= 50 && x <= 99) || (y >= 50 && y <= 99)) #distractor\n" +
    "if ((x >= 50 && x >= 99) || (y <= 50 && y >= 99)) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P15-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P15-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P15-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P15-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
## tehtävä 16
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 16
Järjestä koodirivit ohjelmaksi joka palauttaa annetuista kolmesta luvusta suurimman

<div id="P16-sortableTrash" class="sortable-code"></div> 
<div id="P16-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P16-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P16-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function max_of_three(x, y, z) \n" +
    "{\n" +
    "  max_val = 0;\n" +
    "  if (x > y)\n" +
    "  {\n" +
    "    max_val = x;\n" +
    "  } else\n" +
    "  {\n" +
    "    max_val = y;\n" +
    "  }\n" +
    "  if (z > max_val) \n" +
    "  {\n" +
    "    max_val = z;\n" +
    "  }\n" +
    "  return max_val;\n" +
    "} \\n console.log(max_of_three(1,0,1)); \\n console.log(max_of_three(0,-10,-20)); \\n console.log(max_of_three(1000,510,440)); \\n \n" +
    "if ((x <= 50 && x <= 99) || (y >= 50 && y <= 99)) #distractor\n" +
    "if ((x >= 50 && x >= 99) || (y <= 50 && y >= 99)) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P16-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P16-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P16-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P16-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 17
Järjestä koodirivit ohjelmaksi joka palauttaa kahdesta annetusta luvusta sen joka on lähinnä numeroa 100. Jos annetut luvut ovat samansuuruisia, palautetaan false.
<div id="P17-sortableTrash" class="sortable-code"></div> 
<div id="P17-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P17-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P17-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function near_100(x, y) {\n" +
    "  if (x != y)\n" +
    "  {\n" +
    "    x1 = Math.abs(x - 100);\n" +
    "    y1 = Math.abs(y - 100);\n" +
    "    if (x1 < y1)\n" +
    "    {\n" +
    "      return x;\n" +
    "    }\n" +
    "    if (y1 < x1)\n" +
    "    {\n" +
    "      return y;\n" +
    "    }\n" +
    "    return 0;\n" +
    "  }\n" +
    "  else\n" +
    "    return false;\n" +
    "} \\n console.log(near_100(90, 89)); \\n console.log(near_100(-90, -89)); \\n console.log(near_100(90, 90)); \\n \n" +
    "if ((x <= 50 && x <= 99) || (y >= 50 && y <= 99)) #distractor\n" +
    "if ((x >= 50 && x >= 99) || (y <= 50 && y >= 99)) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P17-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P17-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P17-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P17-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 18
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 19
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 20
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 21
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 22
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 23
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 24
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 25
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 26
Järjestä koodirivit ohjelmaksi joka 


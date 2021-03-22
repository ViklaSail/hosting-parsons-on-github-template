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
Järjestä koodirivit ohjelmaksi joka  palauttaa suuremman kahdesta numerosta. Lisäksi ohjelma varmistaa että luvut ovat 40 ja 60 välillä eiväkä ole samat. 

<div id="P18-sortableTrash" class="sortable-code"></div> 
<div id="P18-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P18-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P18-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function max_townums_range(x, y){	\n" +
    "  if( (x >= 40) && (x <= 60) && (y >= 40 && y <= 60) ){\n" +
    "    if(x === y){\n" +
    "      return \"Numbers are the same\";\n" +
    "    }else if (x > y){\n" +
    "      return x;\n" +
    "    }else{\n" +
    "      return y;\n" +
    "    }\n" +
    "  } else {\n" +
    "    return \"Numbers don't fit in range\"; \n" +
    "  }\n" +
    "} \\n console.log(max_townums_range(45, 60)); \\n console.log(max_townums_range(25, 60)); \\n console.log(max_townums_range(45, 80)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P18-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P18-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P18-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P18-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 19
Järjestä koodirivit ohjelmaksi joka tarkastaa löytyykö annettu merkki annetussa merkkijonossa sen toisen ja neljännen merkkipositioiden välissä. 


<div id="P19-sortableTrash" class="sortable-code"></div> 
<div id="P19-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P19-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P19-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check_char(str1, char)\n" +
    "{\n" +
    "  var ctr = 0;\n" +
    "  for (let i = 0; i < str1.length; i++)\n" +
    "  {\n" +
    "    if ((str1.charAt(i) == char) && (i >= 1 && i <= 3))\n" +
    "    {\n" +
    "        ctr=1;\n" +
    "        break;\n" +
    "    }\n" +
    "  }\n" +
    "  if (ctr==1) return true;\n" +
    "  return false;\n" +
    "} \\n console.log(check_char(\"Python\", \"y\")); \\n console.log(check_char(\"JavaScript\", \"a\")); \\n console.log(check_char(\"Console\", \"o\")); \\n console.log(check_char(\"Console\", \"C\")); \\n console.log(check_char(\"Console\", \"e\")); \\n console.log(check_char(\"JavaScript\", \"S\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P19-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P19-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P19-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P19-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 20
Järjestä koodirivit ohjelmaksi joka luo parametrina saadusta merkkijonosta uuden niin että kolme ensimmäistä merkkiä on pienillä kirjaimilla. Jos saadun merkkijonon pituus on vähemmän kuin 3 merkkiä, muuta kaikki kirjaimet isoiksi. 
<div id="P20-sortableTrash" class="sortable-code"></div> 
<div id="P20-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P20-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P20-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function upper_lower(str) {\n" +
    "  if (str.length < 3) {\n" +
    "    return str.toUpperCase();\n" +
    "  }\n" +
    "  front_part = (str.substring(0, 3)).toLowerCase(); \\n back_part = str.substring(3, str.length);   \\n \n" +
    "  return front_part + back_part;\n" +
    "} \\n console.log(upper_lower(\"Python\")); \\n console.log(upper_lower(\"Py\")); \\n console.log(upper_lower(\"JAVAScript\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P20-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P20-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P20-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P20-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

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


## tehtävä 22
Järjestä koodirivit erikoislaskimeksi joka laskee kaksi lukua yhteen ja palauttaa 65 jos summa on 50 ja 80 välillä. Muutoin palautetaan 80
<div id="P22-sortableTrash" class="sortable-code"></div> 
<div id="P22-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P22-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P22-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sortaSum(x, y) \n" +
    "{\n" +
    "  const sum_nums = x + y;\n" +
    "  if (sum_nums >= 50 && sum_nums <= 80) {\n" +
    "    return 65;\n" +
    "  }\n" +
    "  return 80;\n" +
    "} \\n console.log(sortaSum(30,20)); \\n console.log(sortaSum(90,80)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P22-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P22-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P22-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P22-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 23
Järjestä koodirivit ohjelmaksi joka tarkastaa kaksi annettua kokonaislukua, että onko jonpi kumpi 8 tai onko niiden summa 8 tai onko niiden ero 8. Palauttaa totuusarvon
<div id="P23-sortableTrash" class="sortable-code"></div> 
<div id="P23-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P23-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P23-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check8(x, y) {\n" +
    "  if (x == 8 || y == 8) {\n" +
    "    return true;\n" +
    "  }\n" +
    "  if (x + y == 8 || Math.abs(x - y) == 8)\n" +
    "  {\n" +
    "    return true;\n" +
    "  }\n" +
    "  return false;\n" +
    "} \\n console.log(check8(7, 8)); \\n console.log(check8(16, 8)); \\n console.log(check8(24, 32)); \\n console.log(check8(17, 18)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P23-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P23-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P23-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P23-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 24
Järjestä koodirivit ohjelmaksi joka saa 3 numeroa. jos kaikki 3 numeroa ovat samoja palautetaan 30, muutoin palautetaan 20. Jos kaksi ensin annettua numeroa ovat samoja, palautetaan 40. 
Check three given numbers, if the three numbers are same return 30 otherwise return 20 and if two numbers are same return 40 
<div id="P24-sortableTrash" class="sortable-code"></div> 
<div id="P24-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P24-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P24-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function three_numbers(x, y, z) {\n" +
    "  if (x == y && y == z) {\n" +
    "    return 30;\n" +
    "  } \\n if (x == y || y == z || z == x) { \\n \n" +
    "    return 40;\n" +
    "  }\n" +
    "  return 20;\n" +
    "} \\n console.log(three_numbers(8, 8, 8)); \\n console.log(three_numbers(8, 8, 18)); \\n console.log(three_numbers(8, 7, 18)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P24-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P24-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P24-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P24-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 25
Järjestä koodirivit ohjelmaksi joka saa parametrina lauseen ja muuttaa lauseen jokaisen sanan ensimmäisen merkin isoksi. 
<div id="P25-sortableTrash" class="sortable-code"></div> 
<div id="P25-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P25-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P25-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function capital_letter(str) \n" +
    "{\n" +
    "    str = str.split(\" \");\n" +
    "    for (var i = 0, x = str.length; i < x; i++) {\n" +
    "        str[i] = str[i][0].toUpperCase() + str[i].substr(1);\n" +
    "    }\n" +
    "    return str.join(\" \");\n" +
    "} \\n console.log(capital_letter(\"Write a JavaScript program to  \\n capitalize the first letter of each word of a given string.\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P25-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P25-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P25-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P25-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script> 



## tehtävä 26
Järjestä koodirivit ohjelmaksi joka muodostaa uuden merkkijonon parametriksi saadun merkkijonon 3 viimeisestä merkistä: kopioi merkkijonoon noita viimeisiä merkkejä kolme kertaa. parametriksi saadun merkkijonon pitää olla vähintään 3 merkkiä pitkä. 
<div id="P26-sortableTrash" class="sortable-code"></div> 
<div id="P26-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P26-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P26-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function newstring(str)\n" +
    "{\n" +
    "  if (str.length >= 3) {\n" +
    "    result_str = str.substring(str.length - 3);\n" +
    "    return result_str + result_str + result_str + result_str;\n" +
    "  }\n" +
    "  else\n" +
    "    return false;\n" +
    "} \\n console.log(newstring(\"Python 3.0\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P26-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P26-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P26-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P26-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 27
Järjestä koodirivit ohjelmaksi joka saa parametriksi merkkijonon. Jos merkkijonon pituus on pariton luku ja suurempi kuin 3, luodaan uusi merkkijono ottamalla kolme keskimmäistä merkkiä parametrina saadusta merkkijonosta. 
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



## tehtävä 28
Järjestä koodirivit ohjelmaksi joka saa merkkijonon parametrina ja luo siitä uuden poistamalla ensimmäisen ja viimeisen merkin, jos ensimmäinen tai viimeinen merkki on 'p'. Muutoin palautetaan alkuperäinen merkkijono
<div id="P28-sortableTrash" class="sortable-code"></div> 
<div id="P28-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P28-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P28-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function nop(str) {\n" +
    "  let start_pos = 0; \\n let end_pos = str.length; \\n \n" +
    "  if (str.length > 0 && str.charAt(0) == 'P') \n" +
    "  { \n" +
    "    start_pos = 1; \n" +
    "  } \\n if (str.length > 1 && str.charAt(str.length - 1) == 'P')  \\n \n" +
    "  {\n" +
    "    end_pos--;\n" +
    "  }\n" +
    "  return str.substring(start_pos, end_pos);\n" +
    "} \\n console.log(nop(\"PythonP\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P28-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P28-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P28-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P28-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 29
Järjestä koodirivit ohjelmaksi joka saa parametriksi listan numeroita. Ohjelma vertaa listan ensimmäistä ja viimeistä numeroa ja palauttaa true jos ne ovat samat. listassa pitäisi siis olla vähintään kaksi numeroa.

<div id="P29-sortableTrash" class="sortable-code"></div> 
<div id="P29-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P29-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P29-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function first_last_same(nums)\n" +
    "{\n" +
    "    var end = nums.length - 1;\n" +
    "    if (nums.length >= 1){\n" +
    "       return nums[0] == nums[end];\n" +
    "    } else {return false;}\n" +
    "} \\n console.log(first_last_same([10, 20, 30]));  \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P29-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P29-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P29-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P29-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

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


## tehtävä 31
Järjestä koodirivit ohjelmaksi joka saa parametriksi 3 alkioisen taulukon ja muodostaa uuden taulukon parametritaulukon ensimmäisesta ja viimeisestä alkiosta. Lopuksi uusi taulukko palautetaan. 
<div id="P31-sortableTrash" class="sortable-code"></div> 
<div id="P31-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P31-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P31-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function started(nums) {\n" +
    "     var array1 = [];\n" +
    "     array1.push(nums[0], nums[nums.length - 1]);\n" +
    "     return array1;\n" +
    "} \\n console.log(started([20, 20, 30])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P31-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P31-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P31-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P31-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 32
Järjestä koodirivit ohjelmaksi jolle annetaan parametriksi taulukko ja integer luku kuvaamaan monenneksiko suurinta alkiota taulukosta haetaan. Ohjelma hakee palauttaa tuon alkion. 
<div id="P32-sortableTrash" class="sortable-code"></div> 
<div id="P32-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P32-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P32-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function Kth_greatest_in_array(arr, k) {\n" +
    "  for (var i = 0; i < k; i++) {\n" +
    "    var max_index = i, tmp = arr[i];\n" +
    "    for (var j = i + 1; j < arr.length; j++) {\n" +
    "      if (arr[j] > arr[max_index]) {\n" +
    "        max_index = j;\n" +
    "      }\n" +
    "    }\n" +
    "    arr[i] = arr[max_index];\n" +
    "    arr[max_index] = tmp;\n" +
    "  }\n" +
    "  return arr[k - 1];\n" +
    "} \\n console.log(Kth_greatest_in_array([1,2,6,4,5], 3)) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P32-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P32-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P32-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P32-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



## tehtävä 33
Järjestä koodirivit ohjelmaksi joka saa parametriksi taulukon ja integer-numeron kuvaamaan montako peräkkäistä alkiota halutaan summata. Ohjelma hakee suurinta mahdollista peräkkäisten lukujen summaa ja palauttaa sen. 
liian vaikea? 
<div id="P33-sortableTrash" class="sortable-code"></div> 
<div id="P33-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P33-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P33-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function array_max_consecutive_sum(nums, k) {\n" +
    "  let result = 0; \\n let temp_sum = 0; \\n \n" +
    "  for (var i = 0; i < k - 1; i++) {\n" +
    "    temp_sum += nums[i];\n" +
    "  }\n" +
    "  for (var i = k - 1; i < nums.length; i++) {\n" +
    "    temp_sum += nums[i];\n" +
    "    if (temp_sum > result) {\n" +
    "      result = temp_sum;\n" +
    "    }\n" +
    "    temp_sum -= nums[i - k + 1];\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(array_max_consecutive_sum([1, 2, 3, 14, 5], 2)) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P33-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P33-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P33-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P33-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 34
Järjestä koodirivit ohjelmaksi, joka saa parametriksi taulukon. Ohjelma etsii kaikista mahdollisista alkiopareista eniten toisistaan eroavan parin ja palauttaa lasketun eron.  


<div id="P34-sortableTrash" class="sortable-code"></div> 
<div id="P34-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P34-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P34-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function array_max_diff(arr) {\n" +
    "    var max_result = 0;\n" +
    "    for(var i=0;i<arr.length;i++)\n" +
    "       {\n" +
    "        for(var k=0; k!=i && k<arr.length; k++)\n" +
    "        {\n" +
    "            var diff = Math.abs(arr[i]-arr[k]);\n" +
    "            max_result = Math.max(max_result, diff);\n" +
    "        }\n" +
    "    }\n" +
    "    return max_result;\n" +
    "} \\n console.log(array_max_diff([1, 2, 3, 8, 9])) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P34-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P34-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P34-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P34-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 35
Järjestä koodirivit ohjelmaksi joka etsii annetusta integertaulukosta sen numeron joka esiintyy lukumääräisesti eniten 
<div id="P35-sortableTrash" class="sortable-code"></div> 
<div id="P35-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P35-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P35-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function array_element_mode(arr) {\n" +
    "  var ctr = [], ans = 0;\n" +
    "  for(var i = 0; i < 10; i++) {\n" +
    "    ctr.push(0);\n" +
    "  }\n" +
    "  for(var i = 0; i < arr.length; i++) {\n" +
    "    ctr[arr[i] - 1]++;\n" +
    "    if(ctr[arr[i] - 1] > ctr[ans]) {\n" +
    "      ans = arr[i] - 1;\n" +
    "    }\n" +
    "  }\n" +
    "  return ans + 1;  \n" +
    "} \\n console.log(array_element_mode([1, 2, 3, 2, 2, 8, 1, 9])) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P35-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P35-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P35-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P35-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

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

## tehtävä 37
Järjestä koodirivit ohjelmaksi joka laskee parametrina saadun taulukon vierekkäisten alkioiden erot. Sitten se laskee nuo erot yhteen ja palauttaa summan. 
<div id="P37-sortableTrash" class="sortable-code"></div> 
<div id="P37-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P37-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P37-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sum_adjacent_difference(arr) {\n" +
    "	var result = 0;\n" +
    "	for (var i = 1; i < arr.length; i++) {\n" +
    "		result += Math.abs(arr[i] - arr[i - 1]);\n" +
    "	}\n" +
    "	return result;\n" +
    "} \\n console.log(sum_adjacent_difference([1, 2, 3, 2, -5])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P37-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P37-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P37-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P37-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 38
Järjestä koodirivit ohjelmaksi joka saa merkkijonon ja muodostaa siitä lyhimmän mahdollisen merkkijonon joka sisältää alkuperäisen merkkijonon ja  on palidromi
<div id="P38-sortableTrash" class="sortable-code"></div> 
<div id="P38-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P38-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P38-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function build_Palindrome(new_str) {\n" +
    "  var flag;\n" +
    "  for (var i = new_str.length;; i++) {\n" +
    "    flag = true;\n" +
    "    for (var j = 0; j < i - j - 1; j++) {\n" +
    "      if (i - j - 1 < new_str.length && new_str[j] != new_str[i - j - 1]) {\n" +
    "        flag = false;\n" +
    "        break;\n" +
    "      }\n" +
    "    }\n" +
    "    if (flag) {\n" +
    "      for (var j = new_str.length; j < i; j++) {\n" +
    "        new_str += new_str[i - j - 1];\n" +
    "      }\n" +
    "      return new_str;\n" +
    "    }\n" +
    "  }\n" +
    "} \\n console.log(build_Palindrome(\"abcddc\")) \\n console.log(build_Palindrome(\"122\")) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P38-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P38-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P38-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P38-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 39
Järjestä koodirivit ohjelmaksi joka tutkii annetusta merkkijonosta onko isoja vai pieniä kirjaimia siinä eniten. sanan case vaihdetaan isoiksi kirjaimiksi jos isoja kirjaimia on eniten, jos pieniä kirjaimia on eniten, kaikki caset vaihdetaan pieniksi. 
<div id="P39-sortableTrash" class="sortable-code"></div> 
<div id="P39-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P39-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P39-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function change_case(new_str) {\n" +
    "  var x = 0; \\n   var y = 0; \\n \n" +
    "  for (var i = 0; i < new_str.length; i++) {\n" +
    "    if (/[A-Z]/.test(new_str[i])) {\n" +
    "      x++;\n" +
    "    } else y++;\n" +
    "  }\n" +
    "  if (y > x) return new_str.toLowerCase();\n" +
    "  return new_str.toUpperCase();\n" +
    "} \\n console.log(change_case(\"Write\")) \\n console.log(change_case(\"PHp\")) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P39-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P39-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P39-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P39-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 40
Järjestä koodirivit ohjelmaksi joka tutkii saadaanko parametrina annetuista merkkijonoista samanlaiset vaihtelemalla merkkien järjestystä toisessa. 
<div id="P40-sortableTrash" class="sortable-code"></div> 
<div id="P40-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P40-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P40-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function rearrangement_characters(str1, str2) {\n" +
    "  var first_set = str1.split(''), \\n       second_set = str2.split(''), \\n       result = true; \\n \n" +
    "      \n" +
    "  first_set.sort(); \\n second_set.sort(); \\n \n" +
    "  for (var i = 0; i < Math.max(first_set.length, second_set.length); i++) {\n" +
    "    if (first_set[i] !== second_set[i]) {\n" +
    "      result = false;\n" +
    "    }\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(rearrangement_characters(\"xyz\", \"zyx\")) \\n console.log(rearrangement_characters(\"xyz\", \"zyp\")) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P40-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P40-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P40-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P40-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 41
Järjestä koodirivit ohjelmaksi joka tarkastaa kahdesta taulukosta onko niissä ainakin yksi yhteinen elementti. 
<div id="P41-sortableTrash" class="sortable-code"></div> 
<div id="P41-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P41-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P41-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check_common_element(arra1, arra2) {\n" +
    "  for (var i = 0; i < arra1.length; i++)\n" +
    "  {\n" +
    "    if (arra2.indexOf(arra1[i]) != -1) \n" +
    "      return true;\n" +
    "  }\n" +
    "  return false;\n" +
    "} \\n console.log(check_common_element([1,2,3], [3,4,5]));  \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P41-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P41-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P41-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P41-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 42
Järjestä koodirivit ohjelmaksi joka laskee lukuja sisältävän taulukon inversioiden määrän. Inversio tarkoittaa tilannetta jossa listan luvut eivät ole luonnollisessa suuruusjärjestyksessä. (ohje: älä mieti käsitettä inversio, mieti vain missä järjestyksessä koodin on oltava muuttujien esittelyn ja käytön perusteella)
<div id="P42-sortableTrash" class="sortable-code"></div> 
<div id="P42-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P42-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P42-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function number_of_InversionsNaive(arr) {\n" +
    "    var ctr = 0;\n" +
    "    for (var i = 0; i < arr.length; i++) {\n" +
    "        for (var j = i + 1; j < arr.length; j++) {\n" +
    "            if (arr[i] > arr[j]) \n" +
    "              ctr++;\n" +
    "        }\n" +
    "    }\n" +
    "    return ctr;\n" +
    "} \\n console.log(number_of_InversionsNaive([0, 3, 2, 5, 9]));    \\n console.log(number_of_InversionsNaive([1, 5, 4, 3]));    \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P42-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P42-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P42-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P42-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



## tehtävä 43
Järjestä koodirivit ohjelmaksi joka poistaa parametrista annetusta numerosta yhden merkin/luvun. Tämä tehdään niin että muodostunut uusi numero on suurin mahdollinen, vaikka yksi numero onkin sen sisältä poistettu. 
<div id="P43-sortableTrash" class="sortable-code"></div> 
<div id="P43-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P43-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P43-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function digit_delete(num) {\n" +
    "    var result = 0, num_digits = [];\n" +
    "    while (num) {\n" +
    "        num_digits.push(num % 10); \\n num = Math.floor(num / 10); \\n \n" +
    "    }\n" +
    "    for (var index_num = 0; index_num < num_digits.length; index_num++) {\n" +
    "        var n = 0;\n" +
    "        for (var i = num_digits.length - 1; i >= 0; i--) {\n" +
    "            if (i !== index_num) {\n" +
    "                n = n * 10 + num_digits[i];\n" +
    "            }\n" +
    "        }\n" +
    "        result = Math.max(n, result);\n" +
    "    }\n" +
    "    return result;\n" +
    "} \\n console.log(digit_delete(100)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P43-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P43-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P43-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P43-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

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

## tehtävä 45
Järjestä koodirivit ohjelmaksi joka saa parametrina jaettavan numeron ja jakajan. Ohjelma jakaa jaettavan niin monta kertaa kuin jako menee tasan ja tallentaa tuloksen uudelleen jaettavaksi. Lopullinen jakolaskun tulos palautetaan. 
<div id="P45-sortableTrash" class="sortable-code"></div> 
<div id="P45-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P45-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P45-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function divide_digit(num, d) {\n" +
    "  if (d==1)\n" +
    "    return num;\n" +
    "  else {\n" +
    "    while (num % d === 0) {\n" +
    "      num = num / d;\n" +
    "    }\n" +
    "    return num;\n" +
    "  }\n" +
    "} \\n console.log(divide_digit(-12, 2)) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P45-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P45-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P45-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P45-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


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

## tehtävä 47
Järjestä koodirivit ohjelmaksi joka tulostaa kahden 3-ulotteisen vektorin pistetulon. 
Huom: pistetulo on vektoreiden alkioiden tulojen summa, eli tässä tapauksessa taulukoiden 1. alkiot kerrotaan keskenään, 2. alkiot keskenään ja 3. alkiot keskenään. lopuksi kaikki summataan yhteen. Pistetulosta löytyy tietoa esim. vikipediasta. 
Tässä palapelissä sillä ei ole väliä, pystyt päättelemään rivien järjestyksen tämän lyhyen kuvauksen ja muuttujien esittelyn/käytön perusteella.
<div id="P47-sortableTrash" class="sortable-code"></div> 
<div id="P47-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P47-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P47-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function dot_product(vector1, vector2) {\n" +
    "  let result = 0;\n" +
    "  for (let i = 0; i < 3; i++) {\n" +
    "    result += vector1[i] * vector2[i];\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(dot_product([1,2,3], [1,2,3])) \\n console.log(dot_product([2,4,6], [2,4,6])) \\n console.log(dot_product([1,1,1], [0,1,-1])) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P47-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P47-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P47-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P47-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 48
Järjestä koodirivit ohjelmaksi joka tulostaa alkuluvut parametrina annettuun lukuun asti. Alkuluku on luku joka on jaollinen vain yhdellä ja itsellään. Tässä yksi mahdollinen ratkaisu.
<div id="P48-sortableTrash" class="sortable-code"></div> 
<div id="P48-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P48-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P48-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sort_prime(num) {\n" +
    "  var prime_num1 = [], prime_num2 = [];\n" +
    "  for (var i = 0; i <= num; i++) { \\n     prime_num2.push(true); \\n } \\n \n" +
    "  for (var i = 2; i <= num; i++) {\n" +
    "    if (prime_num2[i]) {\n" +
    "      prime_num1.push(i);\n" +
    "      for (var j = 1; i * j <= num; j++) {\n" +
    "        prime_num2[i * j] = false;\n" +
    "      }\n" +
    "    }\n" +
    "  }\n" +
    "  return prime_num1;\n" +
    "} \\n console.log(sort_prime(5)) \\n console.log(sort_prime(11)) \\n console.log(sort_prime(19)) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P48-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P48-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P48-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P48-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


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


## tehtävä 50
Järjestä koodirivit ohjelmaksi joka tarkastaa annetusta lukuarvosta, että onko jokainen yksittäinen numero pienempi kuin seuraava numero, eli onko lukuarvon yksittäiset numerot kasvavassa järjestyksessä. 

<div id="P50-sortableTrash" class="sortable-code"></div> 
<div id="P50-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P50-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P50-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function is_increasing_digits_Sequence(num) {\n" +
    "  var arr_num = ('' + num).split('');\n" +
    "  for (var i = 0; i < arr_num.length - 1; i++) {\n" +
    "    if (parseInt(arr_num[i]) >= parseInt(arr_num[i + 1]))\n" +
    "      return false;\n" +
    "  }\n" +
    "  return true;\n" +
    "} \\n console.log(is_increasing_digits_Sequence(123)); \\n console.log(is_increasing_digits_Sequence(1223)); \\n console.log(is_increasing_digits_Sequence(45677)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P50-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P50-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P50-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P50-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 51
Järjestä koodirivit ohjelmaksi. Ohjelma saa parametreina ympyrän keskipisteen koordinaatit, ympyrän säteen ja koordinaattipisteen. 
Ohjelma tarkastaa onko annettu koordinaattipiste ympyrän sisällä. Ohjelma palauttaa totuusarvon. 
syötteet: 
Ympyrän keskipiste: (x, y)
ympyrän säde: r
ympyrän sisällä (oletettavasti, tätä testataan) oleva piste: (a, b)
yksi mahdollinen ratkaisu: 
<div id="P51-sortableTrash" class="sortable-code"></div> 
<div id="P51-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P51-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P51-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function check_a_point(a, b, x, y, r) {\n" +
    "    var dist_points = (a - x) * (a - x) + (b - y) * (b - y);\n" +
    "    r *= r;\n" +
    "    if (dist_points < r) { \\n         return true; \\n \n" +
    "    }\n" +
    "    return false;\n" +
    "} \\n console.log(check_a_point(0, 0, 2, 4, 6)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P51-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P51-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P51-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P51-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 52
Järjestä koodirivit ohjelmaksi. Ohjelman funktio saa listan numeroita ja tarkastaa, ovatko listalla olevat numerot joko laskevassa tai nousevassa järjestyksessä. Yhden numeron merkkijonon tapauksessa palautetaan true. 

<div id="P52-sortableTrash" class="sortable-code"></div> 
<div id="P52-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P52-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P52-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function is_monotonous(num) {\n" +
    "    if (num.length === 1) {\n" +
    "        return true;\n" +
    "    }\n" +
    "    var num_direction = num[1] - num[0];\n" +
    "    for (var i = 0; i < num.length - 1; i++) {\n" +
    "        if (num_direction * (num[i + 1] - num[i]) <= 0) {\n" +
    "            return false;\n" +
    "        }\n" +
    "    }\n" +
    "    return true;\n" +
    "} \\n console.log(is_monotonous([1, 2, 3])); \\n console.log(is_monotonous([1, 2, 2])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P52-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P52-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P52-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P52-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>



## tehtävä 53
Järjestä koodirivit ohjelmaksi. Toteutetaan funktio joka saa parametriksi merkkijonoja listassa ja palauttaa listan pisimmän merkkijonon. 

<div id="P53-sortableTrash" class="sortable-code"></div> 
<div id="P53-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P53-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P53-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function longest_str_in_array(arra)\n" +
    "{\n" +
    "    var max_str = arra[0].length; \\n var ans = arra[0]; \\n \n" +
    "    for (var i = 1; i < arra.length; i++) {\n" +
    "        var maxi = arra[i].length;\n" +
    "        if (maxi > max_str) {\n" +
    "            ans = arra[i]; \\n max_str = maxi; \\n \n" +
    "        }\n" +
    "    }\n" +
    "    return ans;\n" +
    "} \\n console.log(longest_str_in_array([\"ab\", \"a\", \"abcd\"])); \\n console.log(longest_str_in_array([\"ab\", \"ab\", \"ab\"])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P53-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P53-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P53-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P53-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 54
Järjestä koodirivit ohjelmaksi joka etsii annetusta listasta suurimman parillisen numeron.

<div id="P54-sortableTrash" class="sortable-code"></div> 
<div id="P54-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P54-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P54-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function max_even(arra) {\n" +
    "  arra.sort((x, y) => y - x);\n" +
    "  for (var i = 0; i < arra.length; i++) {\n" +
    "    if (arra[i] % 2 == 0)\n" +
    "      return arra[i];\n" +
    "  }\n" +
    "} \\n console.log(max_even([20, 40, 200])); \\n console.log(max_even([20, 40, 200, 301])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P54-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P54-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P54-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P54-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
## tehtävä 55
Järjestä koodirivit ohjelmaksi joka 

## tehtävä 55
Järjestä koodirivit ohjelmaksi. Tämä ohjelma saa parametriksi numeron ja antaa vastaukseksi ensimmäisen annettua numeroa suuremman alkuluvun. 
<div id="P55-sortableTrash" class="sortable-code"></div> 
<div id="P55-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P55-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P55-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function next_Prime_num(num) {\n" +
    "    for (var i = num + 1;; i++) {\n" +
    "        var isPrime = true;\n" +
    "        for (var d = 2; d * d <= i; d++) {\n" +
    "            if (i % d === 0) {\n" +
    "                isPrime = false;\n" +
    "                break;\n" +
    "            }\n" +
    "        }\n" +
    "        if (isPrime) {\n" +
    "            return i;\n" +
    "        }\n" +
    "    }\n" +
    "} \\n console.log(next_Prime_num(3)); \\n console.log(next_Prime_num(17)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P55-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P55-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P55-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P55-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 56
Järjestä koodirivit ohjelmaksi. Funktio saa lukuarvon parametriksi. Ohjelma laskee tuon lukuarvon parillisten numeroiden määrän ja palauttaa sen. 
<div id="P56-sortableTrash" class="sortable-code"></div> 
<div id="P56-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P56-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P56-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function even_digits(num) {\n" +
    "  var ctr = 0;\n" +
    "  while (num) {\n" +
    "    ctr += num % 2 === 0; \\n num = Math.floor(num / 10); \\n \n" +
    "  }\n" +
    "  return ctr;\n" +
    "} \\n console.log(even_digits(123)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P56-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P56-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P56-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P56-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 57
Järjestä koodirivit ohjelmaksi. funktio poistaa kaikki merkit jotka esiintyvät useammin kuin kerran parametrina annetussa merkkijonossa. Palauttaa uuden merkkijonon. 
<div id="P57-sortableTrash" class="sortable-code"></div> 
<div id="P57-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P57-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P57-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function remove_duplicate_cchars(str) {\n" +
    "  var arr_char = str.split(\"\"); \\n var result_arr = []; \\n \n" +
    "  for (var i = 0; i < arr_char.length; i++) {\n" +
    "    if (str.indexOf(arr_char[i]) === str.lastIndexOf(arr_char[i]))\n" +
    "      result_arr.push(arr_char[i]);\n" +
    "    }\n" +
    "  return result_arr.join(\"\");\n" +
    "} \\n console.log(remove_duplicate_cchars(\"abcdabc\")); \\n console.log(remove_duplicate_cchars(\"python\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P57-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P57-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P57-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P57-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script> 

## tehtävä 58
Järjestä koodirivit ohjelmaksi. Ohjelma tarkastaa annetun lukuarvon numeroista ovatko ne samoja vai eivät. jos kaikki lukuarvon numerot ovat sama numero, palautetaan tosi.  

<div id="P58-sortableTrash" class="sortable-code"></div> 
<div id="P58-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P58-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P58-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function test_same_digit(num) {\n" +
    "  const first = num % 10;\n" +
    "  while (num) {\n" +
    "    if (num % 10 !== first) return false;\n" +
    "       num = Math.floor(num / 10);\n" +
    "  }\n" +
    "  return true\n" +
    "} \\n console.log(test_same_digit(1234)); \\n console.log(test_same_digit(1111)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P58-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P58-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P58-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P58-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 59
Järjestä koodirivit ohjelmaksi. Funktio saa parametriksi kaksi taulukkoa ja laskee kuinka monta taulukon elementtiä löytyy molemmista taulukoista. 
<div id="P59-sortableTrash" class="sortable-code"></div> 
<div id="P59-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P59-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P59-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function test_same_elements_both_arrays(arra1, arra2) {\n" +
    "  let result = 0;\n" +
    "  for(let i = 0; i < arra1.length; i++) {\n" +
    "    for(let j = 0; j < arra2.length; j++){\n" +
    "      if(arra1[i] === arra2[j])\n" +
    "      {\n" +
    "        result++;\n" +
    "      }\n" +
    "    }\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(test_same_elements_both_arrays([1,2,3,4], [1,2,3,4])); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P59-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P59-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P59-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P59-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## tehtävä 60
Järjestä koodirivit ohjelmaksi. Funktiolle annetaan parametrina täysin toimiva suhteellisia polkuelementtejä sisältävä unix-hakemisto. Funktio poistaa tarpeettomat elementit polusta siten, että se edelleen osoittaa samaan paikkaan kuin alkuperäinen polku. 
huom: continue-lause hyppäyttää kontrollin silmukan alkuun, jolloin sen jälkeen tulevat rivit jäävät suorittamatta. Tässä ratkaisussa hyödynnetään continue-lausetta for-silmukan sisässä. Muutoin rivien järjestys on pitkälti pääteltävissä siitä, miten muuttujia esitellään ja käytetään.

<div id="P60-sortableTrash" class="sortable-code"></div> 
<div id="P60-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P60-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P60-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function simplify_path(main_path) {\n" +
    "  var parts = main_path.split('/'), \\n       new_path = [], \\n       length = 0; \\n \n" +
    "  for (var i = 0; i < parts.length; i++) {\n" +
    "    var part = parts[i];\n" +
    "    if (part === '.' || part === '' || part === '..') {\n" +
    "      if (part === '..' && length > 0) {\n" +
    "        length--;\n" +
    "      }\n" +
    "      continue;\n" +
    "    }\n" +
    "    new_path[length++] = part;\n" +
    "  }\n" +
    "  if (length === 0) {\n" +
    "    return '/';\n" +
    "  }\n" +
    "  var result = '';\n" +
    "  for (var i = 0; i < length; i++) {\n" +
    "    result +=  '/'+new_path[i] ;\n" +
    "  }\n" +
    "  return result;\n" +
    "} \\n console.log(simplify_path(\"/home/var/./www/../html//sql/\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P60-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P60-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P60-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P60-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 61
Järjestä koodirivit ohjelmaksi. funktio saa parametrina kokonaisluvun  n ja palauttaa sen perusteella komanteen potenssiin korotettujen numeroiden summan seuraavasti: 1^3 +  2^3 + 3^3 + 4^3 + .. n^3 
<div id="P61-sortableTrash" class="sortable-code"></div> 
<div id="P61-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P61-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P61-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sum_Of_Cubes(n) {\n" +
    "  let sumn = 0;\n" +
    "  for (let i = 1; i <= n; i++) {\n" +
    "    sumn += i ** 3;\n" +
    "  }\n" +
    "  return sumn;\n" +
    "} \\n console.log(sum_Of_Cubes(3)); \\n console.log(sum_Of_Cubes(4)); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P61-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P61-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P61-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P61-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## tehtävä 62
Järjestä koodirivit ohjelmaksi. funktio saa parametrina merkkijonon ja laskee kaikkien sen sisältämien numeroiden summan
<div id="P62-sortableTrash" class="sortable-code"></div> 
<div id="P62-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P62-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P62-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function sum_digits_from_string(dstr) {\n" +
    "  var dsum = 0;\n" +
    "  for (var i = 0; i < dstr.length; i++)\n" +
    "  {\n" +
    "    if (/[0-9]/.test(dstr[i])) dsum += parseInt(dstr[i])\n" +
    "  }\n" +
    "  return dsum;\n" +
    "} \\n console.log(sum_digits_from_string(\"abcd12efg9\")) \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P62-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P62-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P62-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P62-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

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

## tehtävä 64
Järjestä koodirivit ohjelmaksi. Funktio saa parametrina merkkijonon ja vaihtaa siitä isot kirjamet pieniksi sekä pienet isoiksi. 

<div id="P64-sortableTrash" class="sortable-code"></div> 
<div id="P64-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="P64-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="P64-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "function change_case(txt) {\n" +
    "    var str1 = \"\";\n" +
    "    for (var i = 0; i < txt.length; i++) {\n" +
    "        if (/[A-Z]/.test(txt[i])) str1 += txt[i].toLowerCase();\n" +
    "        else str1 += txt[i].toUpperCase();\n" +
    "    }\n" +
    "    return str1;\n" +
    "} \\n console.log(change_case(\"testiMERKKI\")); \\n console.log(change_case(\"Germany\")); \\n ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "P64-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "P64-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#P64-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#P64-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>





# OHJELMOINTI-TEHTÄVIÄ
## tehtävä 1 VAIKEA
Tee ohjelma, joka saa parametriksi merkkijonon ja palauttaa totuusarvon.  Ohjelma tarkastaa onko annetussa merkkijonossa vain kirjaimia ja lisäksi tarkastaa että merkkijonossa ei ole vierekkäin kahta isoa tai kahta pientä kirjainta. Eli joka toinen kirjain on iso ja joka toinen pieni. 
Käytä funktioita. skandeja ei tarvitse huomioida. pienet kirjaimet merkistössä ovat yhdessä jonossa joten voit vertaila: A<= kirjain <= Z on varmasti iso kirjain. käytä parillisuuden päättelyyn % operaattoria, testaa esim seuraavaa printtiä: console.log(2%2); console.log(5%2);

Pseudo-koodi joka ehkä auttaa jäsentelemään ohjelmaa
FUNCTION tarkastaMerkkijono
  tarkasta onko merkkijonossa vain kirjaimia
    FOR merkkejä riittää
    IF merkin järjestysnumero on parillinen THEN
        IF 1. merkki pienellä JA merkki on pienellä THEN
           merkkijonossa on rinnaiset pienet merkit
        IF 1. merkki on ISOLLA JA merkki on ISOLLA THEN
           merkkijonossa rinnakkaiset ISOT merkit
    ELSE 
        IF 1. merkki pienellä JA merkki EI ole pienellä THEN
           merkkijonossa on rinnaiset pienet merkit
        IF 1. merkki on ISOLLA JA merkki EI ole ISOLLA THEN
           merkkijonossa rinnakkaiset ISOT merkit
    END FOR
END FUNCTION
## tehtävä 2 VAIKEA
Tee seuraavankaltainen funktio:
Funktiolle annetaan kokonaislukuja sisältävä matriisi (listana joka sisältää listoja). 
funktio tarkastaa onko kyseess ns. lävistäjä matriisi, eli vain matriisin vasemmasta ylänurkasta oikeaan alanurkkaan sijaitsevilla paikoilla on numero, muuten arvot ovat nollia. kts wikipedia https://fi.wikipedia.org/wiki/L%C3%A4vist%C3%A4j%C3%A4matriisi. Jos matriisi on lävistäjämatriisi, palautetaan totuusarvo. 

## tehtävä 3 helppo
Kirjoita ohjelma joka tarkastaa onko annettu numero annetulla välillä. 
Esimerkiksi annat ohjelmalle alarajan 4 ja ylärajan 10 sekä numeron 3. Ohjelman pitää palauttaa false, koska 3 ei ole annetulla välillä. 

## tehtävä 4 vaikeahko
Ohjelma saa parametreina ympyrän keskipisteen koordinaatit, ympyrän säteen ja koordinaattipisteen. 
Ohjelma tarkastaa onko annettu koordinaattipiste ympyrän sisällä. Ohjelman palauttaa totuusarvon. 
syötteet: 
Ympyrän keskipiste: (x, y)
ympyrän säde: r
ympyrän sisällä (oletettavasti, tätä testataan) oleva piste: (a, b)
## tehtävä 5
Tee funktio joka saa kaksi totuusarvoa ja toteuttaa niiden välille NOR operaattorin. Käytä normaaleja and ja or sekä not operaatioita. Tämän pystyy tekemään yhdellä lauseella/rivillä. 
NOR selitettynä: 
(p NOR q) lause on tosi tarkalleen silloin kun sekä p että q ovat epätosia. Eli kun p ja q ovat false = p NOR q = true. 
testaa tuotosta: anna parametreiksi
true true  
true false  
false true  
false false  

Viimeisen parametrikaksikon pitäisi palauttaa true. 

## tehtävä 6
Kirjoita parseint ja numeron toString(2) funktioita käyttäen ohjelma, joka saa parametrinä kymmenjärjestelmän (eli desimaalijärjestelmän) luvun, muuttaa sen binääriseksi, vaihtaa binäärisen luvun bittien järjestyksen käänteiseksi ja muuntaa takasin desimaalijärjestelmän luvuksi joka palautetaan
esim. 

56 -> 111000 bittien kääntämisen jälkeen 7 -> 111
234 -> 11101010 bittien kääntämisen jälkeen 87 -> 1010111

## tehtävä 7 

Tee funktio, joka saa parametrina listan numeroita. Jos listan pituus on pariton numero, palautetaan false. Muussa tapauksessa vaidetaan vierekkäiset alkiot toistensa kesken ja palautetaan uusi lista. 
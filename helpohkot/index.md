layout: default
title: Tenttitehtävä
---

## Parsons puzzle-tenttitehtävä 
[Ohjeita, avaa uuteen välilehteen](../ohjeet.md)

## Tehtävä 1
Write a JavaScript program that accept two integers and display the larger.

<div id="1-sortableTrash" class="sortable-code"></div> 
<div id="1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "var num1, num2;\n" +
    "num1 = window.prompt(\"Input the First integer\", \"0\"); \\n num2 = window.prompt(\"Input the second integer\", \"0\"); \\n \n" +
    "                                                 \n" +
    "if(parseInt(num1, 10) > parseInt(num2, 10)) { \n" +
    "  console.log(\"The larger of \"+ num1+ \" and \"+ num2+ \" is \"+ num1+ \".\");\n" +
    "} else \\n   if(parseInt(num2, 10) > parseInt(num1, 10)) { \\n \n" +
    "    console.log(\"The larger of \"+ num1+\" and \"+ num2+ \" is \"+ num2+ \".\");\n" +
    "  } else {\n" +
    "    console.log(\"The values \"+ num1+ \" and \"+num2+ \" are equal.\");\n" +
    "  }\n" +
    "  ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

# tehtävä 2
Write a JavaScript for loop that will iterate from 0 to 15. For each iteration, it will check if the current number is odd or even, and display a message to the screen.


<div id="2-sortableTrash" class="sortable-code"></div> 
<div id="2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for (var x=0; x<=15; x++) {\n" +
    "        if (x === 0) {\n" +
    "                console.log(x +  \" is even\");\n" +
    "        }\n" +
    "        else if (x % 2 === 0) {\n" +
    "                console.log(x + \" is even\");   \n" +
    "        }\n" +
    "        else {\n" +
    "                console.log(x + \" is odd\");\n" +
    "        }\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

# tehtävä 3
Write a JavaScript program which iterates the integers from 1 to 100. But for multiples of three print "Fizz" instead of the number and for the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz"


<div id="3-sortableTrash" class="sortable-code"></div> 
<div id="3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for ( var i = 1; i <= 100; i++ )\n" +
    "{\n" +
    "  if ( i%3 === 0 && i%5 === 0 )\n" +
    "  {\n" +
    "    console.log( i + \" FizzBuzz\" );\n" +
    "  }\n" +
    "  else if ( i%3 === 0 ) \n" +
    "  {\n" +
    "    console.log(i+ \" Fizz\" );\n" +
    "  }\n" +
    "  else if ( i%5 === 0 ) \n" +
    "  {\n" +
    "    console.log(i+ \" Buzz\" );\n" +
    "  }\n" +
    "  else\n" +
    "  {\n" +
    "    console.log(i);\n" +
    "  }\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

# tehtävä 4
```
Write a JavaScript program to construct the following pattern, using a nested for loop. Go to the editor

*  
* *  
* * *  
* * * *  
* * * * *  

```
<div id="4-sortableTrash" class="sortable-code"></div> 
<div id="4-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="4-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="4-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "var x,y,chr;\n" +
    "for(x=1; x <=6; x++)\n" +
    "{\n" +
    "   for (y=1; y < x; y++)\n" +
    "   {\n" +
    "      chr=chr+(\"*\");        \n" +
    "   }\n" +
    "   console.log(chr);\n" +
    "   chr='';    \n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "4-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#4-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#4-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


# tehtävä 5

Write a JavaScript program to sum the multiples of 3 and 5 under 1000.

<div id="5-sortableTrash" class="sortable-code"></div> 
<div id="5-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="5-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="5-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "var sum = 0;\n" +
    "for (var x = 0; x < 1000; x++)\n" +
    "{\n" +
    "    if (x % 3 === 0 || x % 5 === 0)\n" +
    "    {\n" +
    "       sum += x;\n" +
    "    }\n" +
    "}\n" +
    "console.log(sum);";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "5-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#5-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#5-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


# tehtävä 6

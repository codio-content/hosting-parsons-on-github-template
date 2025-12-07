---
layout: default
title: "Square & Rectangle Measurement"
---

<p class="task-description">
An algorithm is used to either calculate the area or perimeter of a rectangle. The user enters the length of two sides of the rectangle (as separate inputs), and
then if they want to calculate the area or perimeter or area. The desired result is shown
</p> 
<p class="task-instructions">
Drag or shuffle the blocks of code in the practice problems below.
Remember to indent where appropriate by dragging blocks to the right.
To check your work, press the "Get Feedback" button.
To start over, press the "Reset Problem" button.
</p> 
<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "length1 = float(input(&quot;Please enter the length of 1 side in cm &quot;)) \n" +
    "length2 = float(input(&quot;Please enter the length of 2 side in cm &quot;))\n" +
    "measure = input(&quot;Please enter A for area, and P for permieter&quot;)\n" +
    "\n" +
    "if measure == &quot;A&quot;:\n" +
    "  print(length1*length2)\n" +
    "else:\n" +
    "  print(length1+length1+length2+length2)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
---
layout: default
title: "Number Guessing Challenge"
---

<p class="task-description">
Create an algorithm which asks a user to guess a randomly generated number until they get it correct. Every time they guess, it should tell them how far away from the actual number they are.
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

<script type="text/javascript"> 
(function(){
  var initial =
    "import random\n" +
    "target = random.randint(1, 100)\n" +
    "\n" +
    "guess = int(input(&quot;Guess the number (1–100): &quot;))\n" +
    "\n" +
    "while guess != target:\n" +
    "  difference = abs(target - guess)\n" +
    "  print(&quot;You are &quot; + str(difference) + &quot; away from the actual number.&quot;)\n" +
    "  guess = int(input(&quot;Guess again: &quot;))\n" +
    "\n" +
    "print(&quot;Correct! The number was &quot; + str(target))";

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

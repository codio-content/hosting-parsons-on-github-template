---
layout: default
title: "Petrol Station Easy"
---

<p class="task-description">
 An algorithm at a petrol station to work out how much to charge customers. Petrol is £1.34 a litre and Diesel is £1.43. Create an algorithm which asks the user for
the type of fuel and the amount of fuel and output the total amount.
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
    "total = 0\n" +
    "amount = int(input(&quot;How much fuel? &quot;))\n" +
    "fuel = input(&quot;Which type of fuel? &quot;)\n" +
    "\n" +
    "if fuel == &quot;petrol&quot;:\n" +
    "  total = amount * 1.34\n" +
    "else:\n" +
    "  total = amount * 1.43\n" +
    "\n" +
    "print(&quot;£&quot; + str(round(total, 2)))";

  var parsonsPuzzle = new ParsonsWidget({
    sortableId: "sortable",
    max_wrong_lines: 10,
    grader: ParsonsWidget._graders.LineBasedGrader,
    exec_limit: 2500,
    can_indent: true,
    x_indent: 50,
    lang: "en",
    show_feedback: true
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

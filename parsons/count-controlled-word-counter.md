---
layout: default
title: "Word Counter (Count Controlled)"
---

<p class="task-description">
An algorithm stores a list of words. The user enters a word and the algorithm will display how many times that word appears
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
  var initial = "words = [&quot;button&quot;, &quot;steak&quot;, &quot;dog&quot; ,&quot;steak&quot;, &quot;house&quot;]\n" +
    "find = input(&quot;Which word are you looking for? &quot;)\n" +
    "total = 0\n" +
    "for item in words:\n" +
    "  if item == find:\n" +
    "    total = total + 1\n" +
    "\n" +
    "print(&quot;The word &quot; + find + &quot; appears &quot; + str(total) + &quot; in the list&quot;)";
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
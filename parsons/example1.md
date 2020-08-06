---
layout: default
title: Page 2 Example (Variable Check Grader)
---

Construct a program that swaps the values of variables <code>x</code> and <code>y</code> using the helper variable <code>tmp</code>. You can change the names of the variables (<span class="jsparson-toggle"></span>) by clicking them.

<div id="question1-sortableTrash" class="sortable-code"></div> 
<div id="question1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="question1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="question1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "main(){\n" +
    "	System.out.println(Hello World);\n" +
    "}\n" +
    "class HelloWorld #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "question1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#question1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#question1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

[Next](./example2.html)

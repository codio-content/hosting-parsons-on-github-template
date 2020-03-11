---
layout: default
title: Page 2 Example (Variable Check Grader)
---

Construct a program that swaps the values of variables <code>x</code> and <code>y</code> using the helper variable <code>tmp</code>. You can change the names of the variables (<span class="jsparson-toggle"></span>) by clicking them.

<div id="2-sortableTrash" class="sortable-code"></div> 
<div id="2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript">
function(){
  var initial = "$$toggle::x::y::tmp$$ = $$toggle::x::y::tmp$$\n" +
    "$$toggle::x::y::tmp$$ = $$toggle::x::y::tmp$$\n" +
    "$$toggle::x::y::tmp$$ = $$toggle::x::y::tmp$$";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.VariableCheckGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "sortableTrash",
    "vartests": [
        {
            "message": "Testing with initial variable values x = 3 and y = 4",
            "initcode": "x = 3\ny = 4",
            "code": "",
            "variables": {}
        },
        {
            "message": "Testing with initial variable values x = 0 and y = 2",
            "initcode": "x = 0\ny = 2",
            "code": "",
            "variables": {}
        }
    ]
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
 });</script>
    
[Next](./example2.html)

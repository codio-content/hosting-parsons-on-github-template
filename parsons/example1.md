---
layout: page
title: Example 1
---
<div id="sortableTrash" class="sortable-code"></div>
<div id="sortable" class="sortable-code"></div>
<div style="clear:both;"></div>

<p>
    <input id="feedbackLink" value="Get Feedback" type="button" />
    <input id="newInstanceLink" value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
var initial = "function () {\n" +
    "	\n" +
    "}";
var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
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
</script>
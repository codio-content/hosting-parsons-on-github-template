---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---
# Parsons Practice

## Parsons 1

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

## Parsons 2

<div id="sortableTrash2" class="sortable-code"></div>
<div id="sortable2" class="sortable-code"></div>
<div style="clear:both;"></div>

<p>
    <input id="feedbackLink2" value="Get Feedback" type="button" />
    <input id="newInstanceLink2" value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
var initial = "1\n" +
    "2\n" +
    "3\n" +
    "4\n" +
    "5";
var parsonsPuzzle2 = new ParsonsWidget({
    "sortableId": "sortable2",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
});
parsonsPuzzle2.init(initial);
parsonsPuzzle2.shuffleLines();
$("#newInstanceLink2").click(function(event){
    event.preventDefault();
    parsonsPuzzle2.shuffleLines();
});
$("#feedbackLink2").click(function(event){
    event.preventDefault();
    parsonsPuzzle2.getFeedback();
});
</script>

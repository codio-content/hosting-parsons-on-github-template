---
layout: post
title:  "My example"
date:   2020-03-03 11:10:59 +0000
categories: update example
---
# first parsons example

<div id="sortableTrash" class="sortable-code"></div>
<div id="sortable" class="sortable-code"></div>
<div style="clear:both;"></div>

<p>
    <input id="newInstanceLink" value="New instance" type="button" />
    <input id="feedbackLink" value="Get feedback" type="button" />
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
</script>

<div id="sortableTrash" class="sortable-code"></div>
<div id="sortable2" class="sortable-code"></div>
<div style="clear:both;"></div>

<p>
    <input id="newInstanceLink" value="New instance" type="button" />
    <input id="feedbackLink" value="Get feedback" type="button" />
</p>

<script type="text/javascript">
var initial = "function () {\n" +
    "	\n" +
    "}";
var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable2",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
});
parsonsPuzzle.init(initial);
parsonsPuzzle.shuffleLines();
</script>

# Uncommon HTML Bug: innerHTML Security Risk

This repository demonstrates a subtle yet significant bug related to using `innerHTML` to inject script tags into an HTML document. While using `innerHTML` to update parts of the page is a common practice, doing so with user-supplied data or dynamically-generated scripts introduces substantial security risks. 

The `bug.html` file shows the vulnerability: a script is appended to the DOM using `innerHTML`, creating a cross-site scripting (XSS) vulnerability if the content of the innerHTML is not properly sanitized. 

The `bugSolution.html` shows the safer way to update DOM elements with scripts, which is to create elements separately and then append them to the page, avoiding the risks of using `innerHTML` directly.
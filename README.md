# Uncommon HTML Error: Premature DOM Access

This repository demonstrates a subtle error that can occur in HTML/JavaScript when attempting to access and manipulate a DOM element before the browser has fully rendered it.  The core issue is a race condition where the script executes before the element exists.

## The Bug (bug.html)
The `bug.html` file shows the problem: the JavaScript tries to add content to a `<div>` before the browser has created the element.  This results in an error or no visible changes.

## The Solution (bugSolution.html)
The `bugSolution.html` file presents a solution. By explicitly creating the element in the JavaScript and appending it to the DOM *before* trying to add content, this error can be avoided.
# Uncommon HTML Bug: Asynchronous Script Execution

This repository demonstrates an uncommon bug in HTML related to asynchronous JavaScript execution and DOM element access.  The bug arises when a script attempts to manipulate a DOM element before the element has been fully loaded and rendered by the browser.

## Bug Description
The `bug.html` file contains a script that tries to change the display style of a `div` element. However, because of asynchronous loading, the script executes *before* the `div` element is fully added to the DOM, resulting in an error (though not always a visible error; it might just silently fail).

## Solution
The `bugSolution.html` file demonstrates a solution using the `DOMContentLoaded` event listener to ensure that the script executes only after the DOM is fully parsed and ready.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser.  Observe the behavior (the text might or might not disappear; the script may fail silently).
3. Open `bugSolution.html` in a web browser. The text should disappear correctly.

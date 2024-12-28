# HTML Input Number Value Update Bug

This repository demonstrates an uncommon bug related to the &lt;input type="number"&gt; element in HTML and how JavaScript interacts with its value.  The core problem involves unexpected behavior when updating the input's value via JavaScript and then immediately attempting to use that updated value for calculation or further updates.

The `bug.html` file showcases the bug in action.  The `bugSolution.html` file presents a solution to reliably retrieve and use the updated value of the number input.

## Bug Description:

The issue stems from the asynchronous nature of JavaScript and how browsers handle DOM updates.  Changing the `value` property of the number input doesn't instantly update the underlying value used by Javascript.  Therefore, simply calling `element.value` directly after updating it can return the old value.
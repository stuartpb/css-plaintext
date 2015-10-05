# CSS Plain-Text Conversion Explainer

## What is this?

For years, browsers have [their own functionality for converting HTML to plain text][kangax-post], for creating a value for the `innerText` property of HTML elements, as well as generating plain-text values for selected/copied content, but its behavior has been [non-standard and fiddly, with many differences between different browsers][kangax-table]. Attempts have been made to define a simple standard algorithm for converting a tree of DOM elements to plain text, but they have fallen short due to not taking into account all the types of content that are often encountered on the Web, which uses CSS layout to give vastly different effective content from the actual text content of a DOM tree. (For this reason, the value of `innerText` can be drastically different from `textContent`.)

This spec stands to define a single, extensible algorithm for determining the plain-text representation of an HTML selection, with extensible CSS properties for controlling aspects of the output such as what kind of whitespace characters to insert between different types of elements.

[kangax-post]: http://perfectionkills.com/the-poor-misunderstood-innerText/
[kangax-table]: http://perfectionkills.com/the-poor-misunderstood-innerText/#diff-with-textContent

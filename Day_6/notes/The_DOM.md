# The DOM
The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.

In the HTML DOM (Document Object Model), everything is a node:
The document itself is a document node
All HTML elements are element nodes
All HTML attributes are attribute nodes
Text inside HTML elements are text nodes
Comments are comment nodes

### Connecting with the DOM
The document object is the root node of all the othe HTML document and the "owner" of all other nodes.

When selecting nodes in javascript you select the document node

e.g.
```
document.getElementById()
document.getElementsByClassName()
document.getElementsByTagName()
```

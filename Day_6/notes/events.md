#Events

HTML events are "things" that happen to HTML elements.
An HTML event can be something the browser does (such as finish loading the page), or something the user has done (such as scrolling or clicking a button).

In CSS you can react to an event and change the elements styles by pseudo classes such as `:hover` and `:active`.

JavaScript has access to many more events than CSS and also unlike CSS they aren't limited to just changing styles. JavaScript let's you execute code when an event happens.

There are two ways to evoke code when an event happens:
- Event handler attributes
- Event listeners(most common)

**HTML events**
 In HTML they even have an event handler attributes, with inline JavaScript code. These are most common in tutorials or small snippets of code.

e.g.
```
<button onclick="alert('Hello world!')">click me!</button>
```

You can also call functions in your inline JS

e.g.

```
<button onclick="callAlert()">click me!</button>
```

**Common Events**
- onchange: an HTML element has changed
- onclick: an HTML element has been clicked
- onmouseover: an HTMl element has been hovered with a mouse
- onmouseout: the mouse has moved away from an HTMl element
- onkeydown: a key on the keyboard has been processed
- onload: the browser has finished loading the page


**Event Listeners**
Event listeners are attached to an element and take in what kind of event to listen for and what to do once that event has happened.

e.g.
```
document.getElementById('example').addEventListener('click', function() {
  console.log('hello world!');
  })
```

Events aren't just for elements. They can also be applied to the Window Object(the viewport).

e.g.
```
window.addEventListener("resize", function(){
    console.log('hello world!');
});
```

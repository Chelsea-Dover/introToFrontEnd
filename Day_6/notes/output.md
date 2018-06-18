# Output
Javascript(or JS) can be "display" data in multiple different ways:
- innerHTML: writes into the HTML element
- document.write(): writes into the HTML output
- window.alert(): writes into an alter box
- console.log(): writes into the browser console

**innerHTML**
`innerHTML` will write into a specified HTML element. To gain access to an HTMl element you must first select it (There are many methods for selecting elements, the two most used are `document.getElementsByClassName("elementClassName")` and `document.getElementById("elementId")`, in this example we will be using `document.getElementById("")`). Once we've selected the element we can use `innerHTML` to define the content.

e.g.

```
<!-- HTMl section -->
<div id="example">Hey</div>

<!-- JS section -->
document.getElementById('example').innerHTML = 'Hello world!'
```

result:

  Hello world!

**document.write()**
The `document.write()` method should only be used for testing. When using `document.write()` after an HTMl document if completely loaded it will delete all existing HTML.

e.g.
```
document.write('Hello world!');
```

**window.alert()(or just "alert()")**
`window.alert()`(or the shorthand which is just `alert()`) will make an alert box open containing the information you specified.

e.g.
```
window.alert('Hello world!');
alert('Hey world!');
```

**console.log()**
`console.log()` is the preferred method for debugging. It will output your specified data in the inspector console.

e.g.
```
console.log('Hello world!');
```

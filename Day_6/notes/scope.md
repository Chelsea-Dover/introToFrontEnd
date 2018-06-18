# Javascript scope
In JavaScript, scope is the set of variables, objects, and functions you have access to.

**Local Variables**
Variables declared within a JavaScript function, become `local` to the function.

Local variables have `local scope`. Meaning that they can only be accessed within that function.

e.g.
```
// code here cannot get access to x

function myFunction() {
  var x = "hello"

  // code here can get access to x
}
```

**Global Variables**
Variables declared outside a function, become `global`.

Global variables have `global scope`. Meaning all functions can access it.

e.g.
```
var x = "hello"

// code here cannot get access to x

function myFunction() {


  // code here can get access to x
}
``

# Variables
Variables are used to store data values.

The syntax for creating a variable is by starting with the keyword `var`. Once you've defined the variable you can then assign a value to it by using the equal sign.

e.g.
```
var x = 1;
```

In JavaScript you don't need to assign a value to your variable the same time you define it. As long as the variable is defined before you try to assign a value it and it's in scope everything will work.

e.g.
```
var x;

x = 1;
```

JavaScript is a loosely typed or a dynamic language. That means you don't have to declare the type of a variable ahead of time. The type will get determined automatically while the program is being processed. That also means that you can have the same variable as different types.

e.g.
```
var  myVar = “this is a string”;
myVar = 2;
myVar = document.getElementById(“myElement”);
```

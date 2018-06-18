# Debugging
  Errors can (will) happen, every time you write some new computer code.

JavaScript is very forgiving and will try it's darnedest to work with what you give it and just silently break. The reason for that is because if it completely broke when something wasn't valid like some other programming languages every time something was wrong on your site your users would be able to see it and that would not be good.

**Debuggers**
Built-in debuggers can be turned on and off, forcing errors to be reported to the user.

With a debugger, you can also set breakpoints (places where code execution can be stopped), and examine variables while the code is executing.

Normally, otherwise follow the steps at the bottom of this page, you activate debugging in your browser with the F12 key, and select "Console" in the debugger menu.

**Browser Console and Logging**
The console in the inspector displays JavaScript errors and logging in the browser.

You can log data in the browser by using `console.log()`.

e.g.
```
var x, y, z;
x = 1;
y = 2;
z = x + y;

console.log(z)
```

**Breakpoints**
In the debugger window, you can set breakpoints in the JavaScript code.

At each breakpoint, JavaScript will stop executing, and let you examine JavaScript values.

After examining values, you can resume the execution of code (typically with a play button).

**Debugger Keyword**
The debugger keyword stops the execution of JavaScript, and calls (if available) the debugging function.

This has the same function as setting a breakpoint in the debugger.

With the debugger turned on, this code will stop executing before it executes the third line.

e.g.
```
var x = 15 * 5;
debugger;
document.getElementById("demo").innerHTML = x;
```

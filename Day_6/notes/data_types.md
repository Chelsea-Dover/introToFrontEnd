# Data types
Data types are a very important concept in programming. They allows the computer to know how the programmer intends to use the data.

For example, let's say we have this:
`var x = "1" + "2";`

Without data types, how would a computer know whether to combine both of the above so the output would be `12` or to add up the values so the output would be `3`?

Another example. Without data types, a computer cannot safely solve this:

`var x = 1 + "hello";`

What will that output? Will it produce an error?
JavaScript will treat the example above as below because when adding a number and a string, JavaScript will treat the number as a string:

`var x = "1" + "hello"`

JavaScript evaluates expressions from left to right. Different sequences can produce different results:

e.g.

```
var x = 1 + 2 + 'hello';

/* the above will result in 3hello */

var x = 'hello' + 1 + 2;

/* the above will result in hello12 */
```
In the first example, JavaScript treats 16 and 4 as numbers, until it reaches "Volvo".
In the second example, since the first operand is a string, all operands are treated as strings.

JavaScript is a loosely typed or a dynamic language. That means you don't have to declare the type of a variable ahead of time. The type will get determined automatically while the program is being processed. That also means that you can have the same variable as different types.

**Data Types**
In JavaScript, almost "everything" is an object.
- Booleans can be objects (if defined with the new keyword)
- Numbers can be objects (if defined with the new keyword)
- Strings can be objects (if defined with the new keyword)
- Dates are always objects
- Maths are always objects
- Regular expressions are always objects
- Arrays are always objects
- Functions are always objects
- Objects are always object

The concept of objects in JavaScript can be understood with real life, tangible objects.

In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup for example. A cup has a color, a design. weight, a material it's made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.

*methods*
Methods are actions that can be applied to objects. A JavaScript Method is a property containing a function definition.

All JavaScript values, except primitives, are objects.

Syntax to access an object method:
	objectsName.methodName()

If you access the method, without `()`, it will return the function definition.

A primitive value is a value that has no properties or methods. A primitive data type is data that has a primitive value.

The six data types that are primitive are:
  - Boolean type: possible values are `true` or `false`
  - Null type: an assignment value. It can be assigned to a variable as a representation of no value.
  - Undefined: undefined means a variable has been declared but has not yet been assigned a value. This is similar to null but they are different
  - Number: integer such as `100` or `1.00`
  - String: a section of text such as `'hello'` or `"10"`
  - Symbol: a unique and immutable data type and may be used as an identifier for object properties. The symbol object is an implicit object wrapper for the symbol primitive data type.

Primitive values are immutable (they are hard coded and therefore cannot be changed).

_if x = 3.14, you can change the value of x. But you cannot change the value of 3.14._

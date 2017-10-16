# CSS selectors
Using more unique selectors is a very sleek way to keep you selectors in CSS short.

The three main selectors are:
- tag selectors
- class selectors
- id selectors

## Tag selectors
 Tag selectors are the most common selectors used. The syntax of a tag selector is the tag name of the element you want and that's it!

So if we had an paragraph HTML element like so:
 `<p>hello!</p>`
and we want to select it in the CSS to add style we can do that by doing the following:

```
p {
  background:red;
}
```

## Class selectors
Class selectors are very useful as you can add the same class to multiple elements of all different kinds and then add the same styles to them all in one spot.

So If we want to get elements with the class `class-selector`

e.g.
```
<p class="class-selector">hello!</p>
<div class="class-selector">hey!</div>
```

We can do that by putting the below in the CSS
```
.class-selector {
  background:red;
}
```
## Id selectors
Id selectors are mostly used in Javascript. They are unique selectors so once you add an id to an element you cannot add it to another one.

So if we have an element with an id such as: `<p id="id-selector">hello!</p>` and we want to select it in CSS we can do that by adding the following CSS:

```
#id-selector {
  background:red;
}
```
## Universal selector
The universal selector will choose all nodes. The syntax is `*`.

So if we wanted add sty to every element, we can do that by doing the following:
```
* {
  background:red;
}
```

## Attribute selectors
Attribute selectors will select elements based on the value of one of it's attribute.

#### [attribute] Selector
The [attribute] selector will select elements with a certain attribute. For example `a[target]` will select all anchor tags with the attribute target

e.g.
```
<a href="link.com" target="_blank">hello!</a> <!-- style will be applied to this element -->

<a href="link.com">hey!</a> <!-- style will not be applied to this element -->
```

#### [attribute~="value"] Selector
The [attribute~="value"] selector selects elements with an attribute value containing a specified word. For example, if we want to get every element with a target attribute with the value `_blank` we can select it in the CSS by doing the following:

```
[target~="_blank"] {
  background:red;
}
```

#### [attribute|="value"] Selector
The [attribute|="value"] selector selects elements with a specified attribute starting with the specified value. It must be the whole word or separated by dashes though.

e.g.
```
<!-- html section -->
<div class="class-selector">hello!</div> <!-- styles will be applied to this element -->
<p class="class-paragraph">hey!</p> <!-- styles will be applied to this element -->
<div class="classhowdy">howdy!</div> <!-- styles will not be applied to this element -->

<!-- css section -->

[class|="class"] {
  background:red;
}
```

#### [attribute^="value"] Selector
The [attribute^="value"] selector is very similar to the [attribute|="value"] selector which we talked about above. It is used to select elements whose attribute value starts with a specified value just like the selector above. But the value doesn't have to be be the whole word or separated by dashes.

e.g.
```
<!-- html section -->
<!-- styles will be applied to all elements -->
<div class="class-selector">hello!</div>
<p class="class-paragraph">hey!</p>
<div class="classhowdy">howdy!</div>

<!-- css section -->

[class|^="class"] {
  background:red;
}
```

#### [attribute$="value"] Selector
The [attribute$="value"] selector is the same as the above selector([attribute^="value"] selector) except it selects elements whose attribute value ends with a specified value.

e.g.
```
<!-- html section -->
<!-- styles will be applied to all elements -->
<div class="selector-class">hello!</div>
<p class="paragraph-class">hey!</p>
<div class="howdyclass">howdy!</div>

<!-- css section -->

[class|$="class"] {
  background:red;
}
```

#### [attribute*="value"] Selector
The [attribute*="value"] selector is used to select elements that contain a specified value anywhere in the attribute value.

e.g.
```
<!-- html section -->
<!-- styles will be applied to all elements -->
<div class="selector-class">hello!</div>
<p class="paragraph-class">hey!</p>
<div class="howdyclass">howdy!</div>

<!-- css section -->

[class|*="cl"] {
  background:red;
}
```

## Pseudo-Elements
Pseudo-Elements are used to select specific parts of an element. The way to use them is to place them after a normal selector.

e.g.
```
p::pseudo-element {
  /* styles go here */
}
```

#### ::before
The ::before pseudo-element is used to inject an element before all content in the specified element. You must add the declaration `content` the both this pseudo-element and the ::after element. Once you add content you can add style like any other element.

e.g.

```
<!-- html section -->
<div>hello!</div>

<!-- css section -->
div::before {
  content: "hey!";
  background: red;
}
```

result:

<span style="background-color: red">hey!</span>hello!

You may leave the the quotation marks empty in the value of content. But if it's empty you must add a height, width and make the position absolute or fixed.

e.g.

```
div::before {
  content: "";
  width:10px;
  height:10px;
  position: absolute;
  background: red;
}
```

#### ::after
The ::after pseudo-element is used to inject an element after all content in the specified element. You must add the declaration `content` the both this pseudo-element and the ::before element. Once you add content you can add style like any other element.

e.g.

```
<!-- html section -->
<div>hello!</div>

<!-- css section -->
div::after {
  content: "hey!";
  background: red;
}
```

result:

hello!<span style="background-color: red">hey!</span>

Just like the ::before element, you may leave the quotation marks empty. If they are empty you must add a height, width and make the position absolute or fixed.

e.g.

```
div::after {
  content: "";
  width:10px;
  height:10px;
  position: absolute;
  background: red;
}
```

#### ::first-letter
The first-letter pseudo-element will select the first letter in the specified element.

e.g.
```
<!-- html section -->
<p>hello!</p>

<!-- css section -->

p::first-letter {
  background:red;
}
```
result:

<span style="background-color: red">h</span>ello!

#### ::first-line
The first-line pseudo-element is very similar to the first-letter pseudo-element. The only difference between them is that first-line selects the first line of text in an element.

e.g.
```
<!-- html section -->
<p>hello!</p>

<!-- css section -->

p::first-line {
  background:red;
}
```
result:

<span style="background-color: red">hello!hey!howdy!hi!morning!g'day!</span> <br>
hello!hey!howdy!hi!morning!g'day!<br>
hello!hey!howdy!hi!morning!g'day!

#### ::selection
The selection pseudo-element is sued to style the section of an element that has been selected or highlighted

e.g.
```
p::selection {
  background:red;
}
```

## Pseudo-classes
Pseudo-classes are used for selecting an element in a certain state. The syntax is almost the same as pseudo-elements except for instead of using two colons, you only use one.

e.g.
```
p:pseudo-class {
  /* styles go here */
}
```

#### :active
The active pseudo-class selects an element that is being clicked.

e.g.
```
a:active {
  background:red;
}
```
#### :checked
The checked pseudo-class selects an input element that is checked

e.g.
```
input:checked {
  background:red;
}
```
#### :disabled
The disabled pseudo-class selects an input element that is disabled

e.g.
```
<!-- html section -->
<form action="">
  Input 1: <input type="text" value="disabled-input" disabled><br>
  Input 2: <input type="text" value="enabled-input">
</form>

<!-- css section -->
input:disabled {
  background:red;
}
```
result:

<form action="">
  Input 1: <input style="background:red;" type="text" value="disabled-input" disabled><br>
  Input 2: <input type="text" value="enabled-input">
</form>

#### :enabled
The enabled pseudo-class is very similar to the disabled pseudo-class. the difference is that it selects an input element that is enabled as opposed to disabled.

e.g.
```
<!-- html section -->
<form action="">
  Input 1: <input type="text" value="disabled-input" disabled><br>
  Input 2: <input type="text" value="enabled-input">
</form>

<!-- css enabled -->
input:disabled {
  background:red;
}
```
result:

<form action="">
  Input 1: <input type="text" value="disabled-input" disabled><br>
  Input 2: <input style="background:red;" type="text" value="enabled-input">
</form>

#### :empty
The empty pseudo-class selects a specified element that has no children

e.g.
```
<!-- html section -->
<div>
  hello!
  <p>hey!</p>
</div>

<div>
  howdy!
</div>

<!-- css section -->
div:empty {
  background:red;
}
```

result:

<div>
  hello!
  <p>hey!</p>
</div>

<div style="background:red;">
  howdy!
</div>

#### :first-child
The first-child pseudo-class selects the first child element in a specified element.

e.g.
```
<!-- html section -->
<div> <!-- parent -->
  hello!
  <p>hey!</p> <!-- first child -->
  <p>howdy!</p> <!-- last child -->
</div>

<!-- css section -->
div:first-child {
  background:red;
}
```

result:

<div>
  hello!
  <p style="background:red;">hey!</p>
  <p>howdy!</p>
</div>

#### :last-child
The last-child pseudo-class is very similar to the first-child selector. The difference is the last-child selects the last child element in a specified element.

e.g.
```
<!-- html section -->
<div> <!-- parent -->
  hello!
  <p>hey!</p> <!-- first child -->
  <p>howdy!</p> <!-- last child -->
</div>

<!-- css section -->
div:last-child {
  background:red;
}
```

result:

<div>
  hello!
  <p>hey!</p>
  <p style="background:red;">howdy!</p>
</div>

#### :first-of-type
The first-of-type pseudo-class selects an specified element that is the first one of it's kind in it's parent.

e.g.
```
<!-- html section -->
<div>
  hello!
  <p>hey!</p> <!-- first of type -->
  <p>howdy!</p> <!-- second of type -->
</div>

<!-- css section -->
div:first-of-type {
  background:red;
}
```

result:

<div>
  hello!
  <p style="background:red;">hey!</p>
  <p>howdy!</p>
</div>

#### :last-of-type
The last-of-type pseudo-class is very similar to the first-of-type pseudo-class. The difference is the last-of-type selects a specified element that is the last one of it's kind in it's parent.

e.g.
```
<!-- html section -->
<div>
  hello!
  <p>hey!</p> <!-- first of type -->
  <p>howdy!</p> <!-- second of type -->
</div>

<!-- css section -->
div:last-of-type {
  background:red;
}
```

result:

<div>
  hello!
  <p>hey!</p>
  <p style="background:red;">howdy!</p>
</div>

#### :nth-of-type()
The nth-of-type pseudo-class is very similar to the pseudo-classes last-of-type and first-of-type. It selects a specified element that is a specified number from the beginning of the parent element.

e.g.
```
<!-- html section -->
<div>
  <p>hello!</p> <!-- 1st of type -->
  <p>hey!</p> <!-- 2nd of type -->
  <p>howdy!</p> <!-- 3rd of type -->
</div>

<!-- css section -->
p:nth-of-type(2) {
  background:red;
}
```

result:

<p>hello!</p>
<p style="background:red;">hey!</p>
<p>howdy!</p>

#### :only-of-type
The only-of-type pseudo-class selects a specified element that is the only of it's kind in it's parent.

e.g.
```
<!-- html section -->
<div>
  <p>hello!</p> <!-- 1st of type -->
  <p>hey!</p> <!-- 2nd of type -->
</div>

<div>
  <p>howdy!</p> <!-- 1st of type -->
  <span>hi!</span> <!-- 1st of type -->
</div>

<!-- css section -->
p:only-of-type {
  background:red;
}
```

result:
<div>
  <p>hello!</p>
  <p>hey!</p>
</div>
<div>
  <p style="background:red;">howdy!</p>
  <span>hi!</span>
</div>

#### :only-child
The only-child pseudo-class selects a specified element that is the only child in it's parent.

e.g.
```
<!-- html section -->
<div>
  <p>hello!</p> <!-- 1st child -->
  <p>hey!</p> <!-- 2nd child -->
</div>

<div>
  hi!  <!-- not a child just part of the div element -->
  <p>howdy!</p> <!-- 1st child -->
</div>

<!-- css section -->
p:only-child {
  background:red;
}
```

result:
<div>
  <p>hello!</p>
  <p>hey!</p>
</div>
<div>
  hi!
  <p style="background:red;">howdy!</p>
</div>

#### :focus
The focus pseudo-class selects an element that has focus(focus is only allowed on elements that accept keyboard events or other user inputs)

e.g.
```
<!-- html section -->
<button>hello!</button>

<!-- css section -->
button:focus {
    background-color: red;
}
```

#### :hover
The hover pseudo-class selects a specified element that the user is currently hovering over with their mouse.

e.g.
```
<!-- html section -->
<p>hello!</p>

<!-- css section -->
button:hover {
    background-color: red;
}
```

#### :in-range
The in-range pseudo-class selects a specified element in a specified range.

e.g.
```
<!-- html section -->
<input type="number" min="-5" max="5" value="0">

<!-- css section -->
button:in-range {
    background-color: red;
}
```

#### :out-of-range
The checked pseudo-class selects elements with range limitations with a value that's outside specified range.

e.g.
```
<!-- html section -->
<input type="number" min="-5" max="5" value="0">

<!-- css section -->
button:out-of-range {
    background-color: red;
}
```

#### :invalid
The invalid pseudo-class selects form elements that's value does not validate according to the element's settings.

e.g.
```
<!-- html section -->
<input type="email" value="email">

<!-- css section -->
input:invalid {
    background-color: red;
}
```

#### :valid
The valid pseudo-class selects form elements that's value does validate according to the element's settings.

e.g.
```
<!-- html section -->
<input type="email" value="email">

<!-- css section -->
input:valid {
    background-color: red;
}
```

#### :lang(language)
The lang pseudo-class selects a specified element containing a lang attribute with the specified value.

e.g.
```
<!-- html section -->
<p lang="fr">Bonjour!</p>
<p>hello!</p>

<!-- css section -->
p:lang(fr) {
    background-color: red;
}
```

result:

<p style="background:red;">Bonjour!</p>
<p>hello!</p>

#### :link
The link pseudo-class selects unvisited links.

e.g.
```
<!-- html section -->
<a href="link.com">hello!</a>

<!-- css section -->
a:link {
    background: red;
}
```

#### :visited
The visited pseudo-class selects visited links.


e.g.
```
<!-- html section -->
<a href="link.com">hello!</a>

<!-- css section -->
a:visited {
    background: red;
}
```

#### :not()
The not pseudo-class selects all elements that are not a specified element.

e.g.
```
<!-- html section -->
<p class="hello-paragraph">hello!</p>
<span>hey!</span>
<p>howdy!<p>

<!-- css section -->
:not(p) {
    background: red;
}

p:not(.hello-paragraph) {
  color: blue;
}
```

result:

<p style="background: red;">hello!</p>
<span>hey!</span>
<p style="color: blue;">howdy!<p>

#### :nth-child()
The nth-child pseudo-class selects an element that is a specified number from the beginning of the parent element.

e.g.
```
<!-- html section -->
<div> <!-- parent -->
  <p>hello!</p> <!-- 1st child -->
  <p>hey!</p> <!-- 2nd child -->
  <p>howdy!</p> <!-- 3rd child -->
</div>

<!-- css section -->
p:nth-child(2) {
    background: red;
}
```

result:

<p>hello!</p>
<p style="background: red;"">hey!</p>
<p>howdy!</p>

#### :nth-last-child()
The nth-last-child pseudo-class is very similar to the nth-child pseudo-class except it counts front the last of the parent instead of the first.

e.g.
```
<!-- html section -->
<div> <!-- parent -->
  <p>hello!</p> <!-- 1st child -->
  <p>hey!</p> <!-- 2nd child -->
  <p>howdy!</p> <!-- 3rd child -->
</div>

<!-- css section -->
p:nth-last-child(3) {
    background: red;
}
```

result:

<p style="background: red;"">hello!</p>
<p>hey!</p>
<p>howdy!</p>

#### :optional
The optional pseudo-class selects input elements without the attribute required.

e.g.
```
<!-- html section -->
<!-- html section -->
Input 1: <input type="text" value="required-input" required><br>
Input 2: <input type="text" value="optional-input">


<!-- css section -->
input:optional {
    background-color: red;
}
```

result:

Input 1: <input type="text" value="required-input" required><br>
Input 2: <input style="background-color: red;" type="text" value="optional-input">

#### :required
The optional pseudo-class selects input elements with the attribute required.

e.g.
```
<!-- html section -->
<!-- html section -->
Input 1: <input type="text" value="required-input" required><br>
Input 2: <input type="text" value="optional-input">


<!-- css section -->
input:required {
    background-color: red;
}
```

result:

Input 1: <input style="background-color: red;" type="text" value="required-input" required><br>
Input 2: <input type="text" value="optional-input">

#### :read-only
The checked pseudo-class selects input elements that contain the readonly attribute.

e.g.
```
<!-- html section -->
<!-- html section -->
Input 1: <input type="text" value="now-readonly-input"><br>
Input 2: <input readonly type="text" value="readonly-input">

<!-- css section -->
input:read-only {
    background-color: red;
}
```

result:

Input 1: <input type="text" value="now-readonly-input"><br>
Input 2: <input readonly style="background:red;" type="text" value="readonly-input">

#### :read-write
The checked pseudo-class selects input elements that do not contain the readonly attribute.

e.g.
```
<!-- html section -->
<!-- html section -->
Input 1: <input type="text" value="now-readonly-input"><br>
Input 2: <input readonly type="text" value="readonly-input">

<!-- css section -->
input:read-write {
    background-color: red;
}
```

result:

Input 1: <input style="background:red; type="text" value="now-readonly-input"><br>
Input 2: <input readonly" type="text" value="readonly-input">

#### :root
The root pseudo-class selects the document's root element(the `html` element)

e.g.
```
:root {
    background-color: red;
}
```

#### :target
URLs with an # followed by an anchor name link to a certain element within a document. The element being linked to is the target element.

The :target selector can be used to style the current active target element.

e.g.
```
:target {
    background-color: red;
}
```

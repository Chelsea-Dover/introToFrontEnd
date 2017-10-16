# CSS hierarchy
---
CSS is like an epic battle of styles trying to override each other. The way they do that is by either being more quince or being the lowest(that last to be rendered). Here's a few ways you can make styles override each other:
- Using CSS cascading properties
- Chaining selectors
- Using more unique selectors
- Using inline css
- Using the !important rule (WARNING! This is a last resort and should be avoided at all costs)

The last two should be avoided.

## Using CSS cascading properties
The C in CSS stands for cascading, and that's because of it's waterfall like properties. That means that as long as it's the same whatever's last will always override the declarations above it.

So let's try this out. Let's say we have two styles with the same selectors, and same properties but different values. Would the paragraph background be red or green?

```
p {
  background:red;
}

p {
  background:green;
}
```

It would be green! That's because it was last it overrode the declaration above it.

Now let's say that the paragraph had another declaration inside it. Would there be a border on the paragraph or not?

```
p {
  background:red;
  border:solid;
}

p {
  background:green;
}
```

It would! That's because it goes by declaration not the entire block.

## Chaining selectors
Chaining selectors is a great way to make the style more unique.

Let's say we have some HTML with a paragraph inside a div and one outside like so:

```
<div>
  <p>Hello!</p>
<div>
<p>Hey!</p>
```

If we only wanted to add styling to the paragraph inside div we can chain selectors. So in the CSS it would look something like:

```
div p {
  background:red;
}
```

So now it will only look for a paragraph that is inside a div.

Let's say we have two styles, one with one selector and another one below with two like below. Which one would override which?

```
div p {
  background:red;
}

p {
  background:green;
}
```

The one with two selectors! That's because it's only looking for paragraphs inside divs therefor is more unique.

When chaining selectors it doesn't always have to be certain elements inside certain elements.

It can be from parent to direct child like so:

```
<!-- html section -->

<div>
  <p>hello!</p> <!-- css will apply to this element -->
  <aside>
    <p>hey!</p> <!-- css will not apply to this element -->
  </aside>
<div>

<!-- css section -->

div > p {
  background: red;
}

```

An element following a certain element:

```
<!-- html section -->

<div>
  <aside>farewell!</aside>
  <p>hello!</p> <!-- css will not apply to this element -->

  <div>good bye!</div>
  <p>hey!</p> <!-- css will apply to this element -->

  <aside>cheers!</aside>
  <p>howdy!</p> <!-- css will apply to this element -->
<div>

<!-- css section -->

div ~ p {
  background: red;
}
```

An element that's directly after a certain element:

```
<!-- html section -->

<div>
  <aside>farewell!</aside>
  <p>hello!</p> <!-- css will not apply to this element -->

  <div>good bye!</div>
  <p>hey!</p> <!-- css will apply to this element -->

  <aside>cheers!</aside>
  <p>howdy!</p> <!-- css will not apply to this element -->
<div>

<!-- css section -->

div + p {
  background: red;
}
```

You can read more about selectors and get the full list of them [here](https://goo.gl/LcTdBH)

## Using more unique selectors
Using more unique selectors is a very sleek way to keep you selectors in CSS short.

You might have seen an html element with attributes such as `class` and `id` these are used for selection.

e.g.
`<p class="class-selector" id="id-selector">hello!</p>`

`class` is for multiple elements and `id` is for one element. Think of it like this: a cohort(or class) can have multiple students(or elements) but each student(or element) will have a unique id.

The way we access an element using a `class` in CSS is using a period and then whatever you specified the class for that element in the HTML such as below:
```
.class-selector {
  background:red;
}
```

The way we access an element using an `id` in CSS is using a pound sign and then whatever you specified the id for that element as in the HTML such as below:
```
#id-selector {
  background:red;
}
```

There is also the star(`*`) selector. That will select all elements.

```
<!-- html section -->
<!-- styles will be applied to every element -->
<div>
  <aside>farewell!</aside>
  <p>hello!</p>

  <div>good bye!</div>
  <p>hey!</p>

  <aside>cheers!</aside>
  <p>howdy!</p>
<div>

<!-- css section -->

* {
  background: red;
}
```

There are also things called `pseudo classes` and `pseudo elements` which can select an element in a certain state and insert an element. You can read more about selectors and pseudo classes and elements __here__


## Using inline CSS
Because inline CSS must be applied to each element you want your styles on, therefor it is one of the most unique ways to add style. There is only one other way to override it(which is the next topic below). They way to apply inline style is by using the `style` attribute on the element you wish to style.

e.g.
`<p style="background:red;">hello!</p>`

## Using the !important rule
The !important rule is the most powerful selection so it will override everything. It is very *very* bad practice to use this and should be avoided at all costs.

How to use the !important rule is to stick it at the end of your declaration in the CSS. Because it's applied to declarations it will only override that one value, not the whole style block.

e.g.
```
<!-- html section -->
<div>
  <p id="id-selector">hello!</p> <!-- background will be red and border will be dashed -->
<div>

<!-- css section -->
p {
  background:red!important;
  border:solid;
}

#id-selector {
  background:green;
  border: dashed;
}
```

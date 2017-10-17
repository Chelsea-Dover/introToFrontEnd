# Where to put CSS
---

There are three places to add css to your webpage.
- inline
- embedded
- external

## Inline
Inline CSS is the least desirable out of the three because it can be quite hard to maintain. In the CSS hierarchy it is one of the most unique, therefor it will override almost all other CSS.

The placement of inline CSS is in your HTML file. The way to add inline style to your HTML is by using the `style` attribute on the element you would like to style. Here's an example:
`<p style="background:red;">hello!</p>`

## Embedded
Embedded css is the second least desirable out of the three. It's better than inline when it comes to maintenance but it's still not the best. In the CSS hierarchy it will act the same way as an external stylesheet, so how unique the style is will depend on the selectors you use.

The way to add embedded style to your HTML is by using the `<style>` tags in the head of your HTML file.

 Here's an example:
```
<style>
  p {
    background:red;
  }
</style>
```

## External
External CSS is the most desirable out of the three. You can use the same stylesheet for multiple HTML files making maintenance easier and helps section out your file for a more clear file. In the CSS hierarchy it will act the same way as an embedded stylesheet, so how unique the style is will depend on the selectors you use.

The way to add an external stylesheet to your HTML is by creating a separate CSS file e.g. `style.css` and then in your HTML file using a `<link/>` tag in your HTML head with the path to your css file and . Here's an example:
`<link rel="stylesheet" type="text/css" href="style.css">`

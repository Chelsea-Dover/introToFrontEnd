# HTML syntax
HTML stands for HyperText Markup Language. It consists of tags telling the browser what elements to display and how.

## Basic HTML elements
Here's an example of an HTML element:
`<p>You only live once, but if you do it right, once is enough.</p>`

The result of that will be :

    You only live once, but if you do it right, once is enough.

The HTML element starts with an opening tag which consists of two angle brackets with the type of tag between them. e.g. `<p>`. there are many more types of tags and each one has a different purposes for instance, the `<p>` tag is for paragraphs and the `<nav>` tag is for navigation.

After the start of the element has been defined we can add substance to it. There are many options for what to put inside your element such as text, or another element but there are a few rules. For instance it's bad practice to put images in an h1 tag.

To close the element place the closing tag below everything you want inside the element. The closing tag will to almost identical to the opening tag. The only difference is a forward slash before the tag name. e.g. `</p>`.

## Self-closing elements
Here's an example of a self-closing element:
`<img src="link-to-image.png alt="placeholder image"/>"`

The result of that will be :
![alt text](http://lorempixel.com/output/cats-q-c-100-100-1.jpg "placeholder image")

Some HTML elements can't contain anything therefor don't need a separate closing bracket. We call these self-closing elements. Most(but not all. for example the `<br>` tag will add a line brake but wont be displayed) of these elements contain attributes that provide information on what content to show. The forward slash on self-closing tags are stylistic preference that you can either include or not.

## HTML attributes
Here's an example of an HTML element with attributes:
`<a href=”link.com”>content</a>`

HTML elements may contain attributes. Attributes carry extra data about the HTML element. They are located in the opening tag, after the tag name. There are some attributes for specific tags,=. such as the `src` attribute, which is only for images. They're also global attributes that can be added to any element. Such as `class`(defines a a way to look up the element later)
and `style`(specifies an inline CSS style for an element).
## Comments in HTML
Here's an example of a comment in HTML:
`<!-- Merp derp you will never see this! -->`

The result of that will be this(nothing rendering):

     

The syntax for comments in HTMl are two arrows surrounding what you want to comment. The opening arrow consists of an angle bracket `<`, a bang `!` and two dashes `--`. The closing arrow is a mirror of the opening tag without the bang e.g. `-->`.

Comments can be useful for leaving notes about the file for future you or anyone else who may be working on your project. It can also be useful for removing code for a short period without losing it(although it is *very* bad practice to leave comments in your code in production).

You're comment can be as long or as short as you'd like. When writing multiple line comments it's best practice to have the arrows on new lines.
e.g.
`<!--`
`So many lines`
`wow this comment is so long`
`so many lines`
`-->`

# Stacking elements
When writing HTML it can get messy and confusing if you don't format the elements correctly.
For example, look at this bit of HTML:
`<article><p><a href="link"><img src="image.png/></a></p><p>Wow that is one cool picture!</p></article>`

It's already hard to read. Imagine what it would be like for a full website!

Okay so lets put each element on a new line.
```
<article>
<p>
<a href="link">
<img src="image.png/>
</a>
</p>
<p>Wow that is one cool picture!</p>
</article>
````

That's slightly better but not by much. Let's add some indentation!
```
<article>
    <p>
        <a href="link">
            <img src="image.png/>
        </a>
    </p>
    <p>Wow that is one cool picture!</p>
</article>
```
Now that looks much better! You can clearly see when an element starts and ends and what is in each element. For the second paragraph there was only a small bit of text so I felt there was no need for a new line and indentation. Play it by thumb and try to make it as readable for you as possible.

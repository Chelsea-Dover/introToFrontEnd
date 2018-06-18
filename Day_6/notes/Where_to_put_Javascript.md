# Where to put Javascript
There are two ways to connect JS to your HTML.

 You can put JS in either `head` or `body` although it is best practice to put them above the closing `body` tag.

There are two ways to add JS
to your webpage. Both ways involve the `script` tags.
- embedded
- external

**embedded**
When using embedded JS it must be between `script` tags.

e.g.
```
<script>
console.log('hello there!');
</script>
```

**external**
Setting up external JS is very similar to the setup of external CSS.
 1. Create a file ending in `.js`
 2. In your HTML file(either in your head or at the bottom of your body) add a script tag with the path to your JS file (e.g. <script src="exapmle.js"></script>)
 3. Now your file is setup and you can start adding your JS to your file!

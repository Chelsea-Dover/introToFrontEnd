# Exercise: Create Navigation Bar Using CSS Positioning

## Objective
Create navigation bar using CSS positioning


- Create a new HTML file called `position.html`
- Create a new CSS file called `position_style.css`
- Link up your CSS file to you HTML file using the `link` tag in you HTML `head`(if both your HTML file and CSS file are in the same place the link would be `<link rel="stylesheet" type="text/css" href="position_style.css">`)
- Paste the following HTML in the body of your `position.html` file:

```
<nav>
	<div>
		<div></div>
		<h1>The best</h1>
	</div>
</nav>

<ul>
		<li>home</li>
		<li>green</li>
		<li>blue</li>
</ul>

<img src="http://alimentotumascota.es/wp-content/uploads/2017/04/5507692-cat-m-1024x548-1024x548.png">
```
- **Normal option** Paste the following CSS in you `position_style.css` file(if you decide to do this skip the next step) all styling is done with this option so you will only need to apply the `position` properties and the sub properties:

```
body {
	height:100vh;
}

div div {
	width:100px;
	height:100px;
	background: #465C69;
	border-radius:50%;
}

nav {
	border-bottom:solid;
	background:#333;
}

nav > div {
	height:120px;
}

nav {
	width:100%;
}

ul {
	border-right: solid;
	width: 100px;
	height: 100%;
	padding: 10px 0;
	margin-top: 120px;
}

ul li:hover {
	color: #465C69;
}

img {
	width:500px;
}
```
- **Advanced option**
Paste the following CSS in you `position_style.css` file(if you decide to do this skip the previous step):

```
body {
	height:100vh;
}

```
- Using [this page](https://codepen.io/Chelsea-Dover/full/mMVyrY/) as a reference make your page match.

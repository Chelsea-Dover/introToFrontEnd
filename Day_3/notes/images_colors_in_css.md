# Image and colors in CSS

Colors and images is a very fast and easy way to add some personality to your website.
------

## Text
Almost every single website will use this property. By default most of the text on your page will be black with a few exceptions such as links.
It's a good idea to change your main color from black to an almost black color just as `#333` as it is easier on the eyes.

The property to change the font color is `color`. The value can be any type of color such as Cross-browser color names, RGBA and Hexadecimal. Hexadecimal is the fasted for rendering.

e.g.
> color: black;  
> color: rgba(255, 0, 0, 0.5);  
> color: #333333;  

## Background Colors and Images
You can add a background to any element.

### Background properties:
  ##### Background Color

  e.g.
  > background-color: #333333;  
  > background-color: blue;  
  > background-color: linear-gradient(to right, red , yellow);  

  Background color specifies what color the elements background will be. This will color the content and the padding but will not include the margin.
  Background color can take in any type of color (such as Cross-browser color names, RGBA and Hexadecimal), but can also take in gradients. The way to create a gradient is to either use `linear-gradient` or `radial-gradient` with the colors you want between the parentheses and separated by commas.


  ##### Background Image

  e.g.
  > background-image: url(photo.png);  
  > background-image: url(https://www.exapmle.com/photo.png);  

  Background Image will add an image as your background. The value for this property is `url()` with the path to the image in the parentheses. You can either use a url from online or a path to it from your machine

  ##### Background Position

  e.g.
  > background-position: center center;  
  > background-position: left bottom;  
  > background-position: 20% 50%;  
  > background-position: 20px 50px;  

  Background position specifies where your image is displayed in relation to your element. It takes in two values. One for the x-axis and the other for the y-axis. If there's only one value the z-axis will use center.

  The values you can use for background position are:
    - center
    - left
    - right
    - top
    - bottom
    - integer (any kind of size unit such as 20px or 20%)

  ##### Background Size

  e.g.
  > background-size: cover;  
  > background-size: contain;  
  > background-size: 200px 300px;  
  > background-size 20% 50%;  
  > background-size: auto;  

  Background size specifies how large your background image will be.

  The values you can use for background size are:
    - auto(default): image will be its original size
    - cover: scale the image so all sides of the element are covered
    - contain: scale the image so the whole image is shown
    - integer: any kind of size unit such as 20px. If only one is given the other will be auto. If you use a percentage it will be a percent of the parent element


  ##### Background Repeat

  e.g.
  > background-repeat: no-repeat;  
  > background-repeat: repeat;  
  > background-repeat: repeat-y;  


  Background repeat specifies how/if the background image will be repeated.

  The values you can use for background size are:
    - repeat(default): image will be repeated on both the x-axis and y-axis to cover the whole element
    - no-repeat: image will not repeat on the x-axis or y-axis.
    - repeat-y: image will not repeat on the x-axis but will repeat on the y-axis.
    - repeat-x: image will not repeat on the y-axis but will repeat on the x-axis.


  ##### Background Origin

  e.g.
  > background-origin: padding-box;  
  > background-origin: border-box;  
  > background-origin: content-box;  

  Background origin specifies the placement of the background image.

  The values you can use for background origin are:
    - padding-box(default): image starts from the upper left corner of the padding edge
    - border-box: image starts from the upper left corner of the border
    - content-box: image starts from the upper left corner of the content



  ##### Background Clip

  e.g.
  > background-clip: border-box;  
  > background-clip: padding-box;  
  > background-clip: content-box;  

  Background clip specifies the canvas for the background image.

  The values you can use for background clip are:
   - border-box(default): image will be clipped to the border-box
   - padding-box: image will be clipped to the padding-box
   - content-box: image will be clipped to the content-box

  ##### Background Attachment

  e.g.
  > background-attachment: scroll;  
  > background-attachment: fixed;  

  Background attachment manipulates how the image will react when the page is scrolling.

  The values you can use for background attachment are:
    - scroll(default): image will scroll with element
    - fixed: image will stay fixed to viewport
    - local: image scrolls along with the element's contents


  ##### Background

  e.g.
  > backgroundL: yellow url(photo.png) cover no-repeat center padding-box fixed;  
  > backgroundL: pink;  
  > backgroundL: url(photo.png) cover no-repeat center;  

  Background is a shorthand property for all the properties above. Using this shorthand you can do things like make a tinted background image if you'd like to know how to do that you can read about it [here](https://css-tricks.com/tinted-images-multiple-backgrounds/).

## Borders and Box-shadows:
Borders and Box-shadows can make your elements pop out but can also make your page boxy and a bit cluttered if done wrong.

### Box Shadows
Box-shadows use colors and add a shadow either inside or outside your element.

The values for a box shadow are:
 - x-axis(required): This takes in a size unit (such as px, vh, em). It specifies how far on the shadow will be on the x axis. 0 is in the center of the element so 20px would be 20px from the right of the element and -20px would be 20px from the left.
 - y-axis(required): This takes in a size unit (such as px, vh, em). It specifies how far on the shadow will be on the y axis. 0 is in the center of the element so 20px would be 20px from the top of the element and -20px would be 20px from the bottom.
 - blur: This takes in a size unit (such as px, vh, em). It defines the distance of the blur on your shadow. 0 will have no blur and 20px will have a 20px to go from the edge to the solid color.
 - spread: Spread takes in a size unit (such as px, vh, em). It specifies how large the shadow is. If you put 20px it will be 20px bigger than the element. If you put -20px it will be 20px smaller than the element.
 - color: Color takes in any kind of color value (hexadecimal, RGBA, Cross-browser color names, etc). This value will change the color of your shadow. By default it will be black.
 - inset: Unlike the others this can only take one value. If you add `inset` it will go from being a shadow outside of your element and will now be inside.

   e.g.
     > box-shadow: 20px 20px; (This is all you need to get a shadow to appear)  
     > box-shadow: 20px 20px 5px 5px yellow;  
     > box-shadow: 20px 20px 5px 5px pink inset;  


### Borders
Borders can use colors and images for the value. You can also add a border to a specific side of your element.

### Borders with colors:
Borders take in multiple properties:
  ##### Border Style

    e.g.
      > border-style: solid;  
      > border-style: dashed;  

  Border style specifies the style of the border. This is the only border property you need for a border to show up. After this all other properties will use the default values.

  The options are:
   - solid
   - dashed
   - dotted
   - double
   - groove
   - ridge
   - inset
   - outset
   - none
   - hidden

  ##### Border Width

    e.g.
    > border-width: 5px;  
    > border-width: thin;  
    > border-width: 10vh;  

  Border with specifies how thick the border will be. There are specific values for border width you could use, or you could use any size unit.

  The specific border values are:
   - medium (default)
   - thin
   - thick
   - length
   - initial
   - inherit

   ##### Border Color

   e.g.
   > border-color: red;  
   > border-color: #333333;  
   > border-color: rgba(255, 0, 0, 0.5);  

    This is where the colors come in. The values of this property have to be some type of color. They can be anything such as Cross-browser color names, RGBA and Hexadecimal.

   #### Border

   Instead of using every single one of these properties we can use the shorthand property `border`

   e.g.
   > border: solid 5px red;  

   You can also add a border to a specific using the following ad the properties and the same values as the shorthand `border`:
     - border-left
     - border-right
     - border-bottom
     - border-top

   e.g.
   > border-left: solid 20px green;  
   > border-top: dashed 2px yellow;  

## Borders with Images
Borders with images are a separate property from borders with colors. None of the properties be used in the shorthand `border`.

The properties for borders with images are:

##### Border Image Source

    e.g.
    > border-image-source: url(image.png);  
    > border-image-source: url(www.photos.com/image.png);  

This specifies what image your border will display.

##### Border Image Slice

    e.g.
    > border-image-slice: 30;  
    > border-image-slice: fill;  


This property specifies how your image will be sliced.
The values of this property are:
  - an integer
  - a percentage
  - fill
  - initial
  - inherit


##### Border Image Width

    e.g.
    > border-image-width: 10px;  
    > border-image-width: 1;  
    > border-image-width: auto;  

Border image width specifies how wide the border image is. It can take in any size units, auto, initial and inherit.


##### Border Image Outset

    e.g.
    > border-image-outset: 10px;  
    > border-image-outset: 1 1 0 1;  

Border Image Outset specifies how much the border image area extends beyond the border box. It can take in any size units, auto, initial and inherit.

##### Border Image Repeat

    e.g.
    > border-image-repeat: repeat;  
    > border-image-repeat: round;  

Border Image Repeat specifies how the border image should be repeated, rounded or stretched.

  The values of this property are:
    - stretch(default)
    - repeat
    - round
    - space
    - inherit
    - initial

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

## Borders and Box-shadows:
Borders and Box-shadows can make your elements pop out but can also make your page boxy and a bit cluttered if done wrong.

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


    ##### border-image-outset

    ##### border-image-repeat

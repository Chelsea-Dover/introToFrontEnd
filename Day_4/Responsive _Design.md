# Responsive Design in CSS
With all the different kinds of devices and sizes of screens these days responsive design in websites is one of the most important things for a website.

#### Responsive size unites
Responsive size unites can go a long way for making your website responsive.

Using fixed size unites(especially on width) can be very bad for responsive design. If you set a width of an element larger than the viewport it can cause the viewport to scroll horizontally to fit all the elements or cut off your content depending on your CSS.

**Percentage(%)**
Percentage relative to another value(typically an enclosing element).

**em**
Measurement relative to the height of the font therefore, if you set `font-size` to 20px, 1 em unit would be 20px.

e.g.

```
div {
  font-size: 20px;
  width: 2em; /* width would be 40px */
}
```

**ex**
measurement relative to a font's x-height(x-height is defined by the font's lowercase letter x).

**vh**
1% of the viewport height.

e.g.

```
div {
  height: 100vh; /* height would take up full height of viewport */
}
```
**vw**
1% of the viewport width.
e.g.

```
div {
  width: 100vh; /* width would take up full width of viewport */
}
```

#### Media Rule
The `@media` rule defines what styles to apply based on different media types/devices.

Syntax:
```
@media not|only mediatype and (media feature) {
    CSS-Code;
}
```

Media queries look at the capability of the device.

They can be used to check for:
 - width and height of the viewport
 - width and height of the device
 - orientation of the device
 - resolution
 - and many more!

 Media Types:
 - all: all media type devices
 - print: for printers
 - screen: computer screens, tablets, smart-phones etc.
 - speech: for screenreaders

Media Features:
 - any-hover: does the device include a mechanism that allows the user to hover over elements?
 - any-pointer: does the device have an input mechanism pointing device and how accurate is it?
 - aspect-ratio: The ratio between the width and the height of the viewport
 - color: the number of bits per color component for the output device
 - color-index: the number of colors the device can display
 - grid: whether the device is a grid or bitmap
 - height: the viewport height
 - hover: does the device have a primary mechanism allow the user to hover over elements?
 - inverted-colors: is the browser or underlying OS inverting colors?
 - light-level: current light level
 - max-aspect-ratio: the maximum ratio between the width and the height of the display area
 - min-color: the minimum number of bits per color component for the output device
 - min-color-index:	the minimum number of colors the device can display
 - min-device-aspect-ratio: the minimum ratio between the width and the height of the device
 - min-device-width: the minimum width of the device, such as a computer screen
 - min-device-height: the minimum height of the device, such as a computer screen
- min-height: the minimum height of the display area, such as a browser window
- min-monochrome: the minimum number of bits per "color" on a monochrome (greyscale) device
- min-resolution: The minimum resolution of the device, using dpi or dpcm
- min-width: the minimum width of the display area, such as a browser window
- monochrome: the number of bits per "color" on a monochrome (greyscale) device
- orientation: the orientation of the viewport (landscape or portrait mode)
- overflow-block: how does the output device handle content that overflows the viewport along the block axis
- overflow-inline: can content that overflows the viewport along the inline axis be scrolled
- Pointer: is the primary input mechanism a pointing device, and if so, how accurate is it?
- resolution: he resolution of the output device, using dpi or dpcm
- scan: the scanning process of the output device
scripting	Is scripting (e.g. JavaScript) available?
- update-frequency: how quickly can the output device modify the appearance of the content
- width: the viewport width

e.g.
```
@media only screen and (max-width: 500px) {
    div {
      background: red; /* styles will aply until viewport width exceeds 500px */
    }
}
```
#### Layouts
Using layouts such as flexbox and CSS grid as well as Javascript layout libraries such as bootstrap are very helpful when it comes to responsive design.

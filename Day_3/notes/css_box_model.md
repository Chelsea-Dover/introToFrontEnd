# Box Model in CSS

In HTML everything is considered a box. The **box model** is what is used in CSS when talking about design and layout.

The CSS box model is what wraps around every HTML element. It consists of the following:
 - margins
 - borders
 - padding
 - content of the element

![css syntax](http://i.imgur.com/wLk0AsV.png "css box model")

**margin** is like the elements space bubble. It defines the least amount of space it will allow between another element.

**border** is the border that goes around the padding and content.

**padding** is like the fat of the element. It adds more bulk to the element.

**content** is what gets rendered from the HTMl. That includes all text and images.

When setting the height and width of your element in CSS in most browsers it will only change the content area. It will not calculate the border, padding or margin.

**Warning!** Remember how I said "most browsers"? That's because Internet Explore has a different way of calculating the hight and width. They include not only the content, but the padding and border as well.

#### Fixing the the box model!
Around 2010, W3C added a way to customize which box model you use to the CSS spec. The declaration to do that is `box-sizing: border-box;`

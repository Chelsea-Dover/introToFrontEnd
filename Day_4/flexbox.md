# CSS Flex Box Layout
Believe it or not creating layouts on the web has been an uphill battle for a long time. First people hacked layouts by using tables. Then CSS was created and people started using properties such as `float`, `position` and `display` to create layouts. While these were better than using tables they were still not the best. In the 2000s the desire for more "liquid layouts" grew in part because of the growing number of smartphones and tablets. In the 2010s a hero was born and that hero was flexbox(there was also another hero that was born a bit later called `CSS Grid`).

The Flexbox Layout module is used to create more efficient way to dynamically lay out, align and distribute space among sibling elements in a container.

While most of the time in CSS you apply styles directly to the element affected by the declaration, when using flexbox you apply most styles to the parent container.

![flexbox element](http://i.imgur.com/uEc6Na0.png "flexbox element")

#### Properties for the Parent

**display**
`display` is the one property that is required to use flexbox. The `display` property can in quite a few different values. If you want to use flexbox the value you want to use is `flex` (or inline-flex if you want the container to be inline).

e.g.

```
.parent {
  display: flex;
}
```

**align-items**
`align-items` is used to define how the flex items will be laid out along the cross axis(same as justify-content does for the main axis).

The possible values for align-items are:
- stretch(default): flex elements will stretch to fill the container
- flex-start: flex items cross-start margin edge is placed on cross-start
- flex-end: flex items cross-end margin edge is placed on cross-end
- center: flex items are placed in the center of the cross-axis
- baseline: items are aligned such as their baselines align


**align-content**
`align-content` is used when a flexbox have multiple lines and will have no effect if the flexbox only has a single line of flex items. It's purpose is to manipulate how the flex items lineup with the extra space in the cross-axis.

The possible values for align-content are:
  - stretch(default): flex items stretch to fill up the entire flex container
  - center: lex items packed in the center of the flex container
  - flex-start: flex items packed to the start(top) of flex container
  - flex-end: flex items are packed to the end(bottom) of the flex container
  - space-around: Starting and ending with space, flex items are distributed evenly in the flex container
  - space-between: Starting and ending with flex items. It will distribute everything evenly in the flex container

**justify-content**
`justify-content` is used to define hot the flex items will be laid out along the main axis(same as align-items does for the cross axis)

The possible values for justify-content are:
- flex-start(default): flex items are packed toward the start the main axis line
- flex-end: flex items are packed towards the end of the main axis line
- center: flex items are centered along the main axis line
- space-between: Starting and ending with flex items. It will distribute all flex items evenly in the main axis line
- space-around: Starting and ending with space, flex items are distributed evenly in the main axis line



**flex-direction**
`flex-direction` manipulates the direction the flex items are displayed inside the flex container.

The possible values for flex-direction are:
- row(default): flex items are displayed left to right staring at the main start
- row-reverse: flex items will be displayed in reverse. Right to left and starting and the main ending
- column: same as row but top to bottom
- column-reverse: same as row-reverse but bottom to top

**flex-wrap**
`flex-wrap` manipulates how the flex container will deal with overflowing flex items.

The possible values for flex-wrap are:
- no-wrap(default): all flex items will be on one line. If flex container is overflowing with flex items the flex items will shrink until they all fit.
- wrap: if flex container is overflowing with flex items the flex items will wrap onto a new line from top to bottom
- wrap-reverse: if flex container is overflowing with flex items the flex items will wrap onto a new line from bottom to top

**flex-flow**
`flex-flow` is shorthand for `flex-direction` and `flex-wrap`.

e.g. `flex-flow: ‘flex-direction value’ ‘flex-wrap value’`


#### Properties for the children

**align-self**
`align-self` allows the flex item it is specified on to override align-items(that is either specified in the container or by default).

Properties are the same as align-items.

**order**
`order` allows you to manipulate the order of your flex item. By default all items order is 0. The larger the integer you put as the value to further back it goes.

**flex-grow**
`flex-grow` allows you to manipulate how much a flex item is able to grow if necessary. It accepts a unitless value that serves as a proportion. It dictates what amount of the available space inside the flex container the item should take up.

If all items have flex-grow set to 1, the remaining space in the container will be distributed equally to all children. If one of the children has a value of 2, the remaining space would take up twice as much space as the others (or it will try to, at least).

**flex-shrink**
`flex-shrink` allows you to manipulate how much a flex item is able to grow if necessary.

**flex-basis**
`flex-basis` defines to default size of a flex item before the space is distributed.

**flex**
`flex` is shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`

e.g. `flex: ‘flex-grow value’ ‘flex-shrink value’ 'flex-basis value'`

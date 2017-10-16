# CSS Position
The `position` property allow you to manipulate where an element is in the flow of the page and the location of the element.

### Position Properties
When you add the `position` property to an element you will get access to these new properties(the exception being static and in some cases inherit).

These properties are `top`, `bottom`, `left`, `right` and `z-index`

`top`/`bottom`/`left`/`right` specifies how far way the corresponding side of the element is based on what it's relative to. So if we put `top:50px` the elements top side would be 50px from what it's relative to.

`z-index` specifies it's placement in the flow of the page. Elements are stacked in 2d as we can see on the webpage. But they can also stack on top of each other too! All elements have a `z-index` of zero to start off with. So if you add `z-index:1` to an element it will be above every other element in the flow unless specified otherwise.

## Back to Position

There are six different values for the `position` property
 - static
 - relative
 - absolute
 - fixed
 - sticky
 - inherit

#### static
`static` is the default value of elements. It will behave naturally in the page flow and the properties left, right, top, bottom and z-index will have no effect on it.

#### relative
`relative` is similar to `static` as it's original position will stay in the page flow. Where it changes is the properties left, right, top, bottom and z-index. When an element is `relative` it now has access to all of these properties.

A `relative` elements positioning is based on where it's original placement on the page was. So if we added the declaration `left: 50px;` to a `relative` element it would move so it's left side would be 50px from where it originated.

#### absolute
`absolute` will remove the element from the flow of the page. All other elements will ignore it and act as if it's not there. Elements positioned `absolute` will have access to the properties left, right, top, bottom and z-index.

When using the left, right, top and bottom properties an `absolute` elements placement will be based on the webpage. So if we put the declaration `top:0;` to an element that's `absolute` it's top side will be 0 pixels from the top of the page.

Here's where it get's tricky. You know how above I said an `absolute` elements placement while using the  left, right, top and bottom properties will be based on the webpage? Well that's not always the case. If an `absolute` element has a parent that's positioned `relative`, the element switches from being based to the webpage to being based on the `relative` parent. So if we have a `absolute` element that's a child of a `relative` parent and we apply the declaration `top:0;` the top side of the `absolute` element will be 0 pixels from the `relative` parent.

#### fixed
`fixed` is very similar to `absolute`. Like `absolute` it will be taken out of the flow and therefor be ignored by the other elements. Also it will also have access to the properties left, right, top, bottom and z-index just like an `absolute` element. Where they differ is what they are relative to and it's behavior when the webpage is scrolling.

Unlike an element with `absolute` positioning, a `fixed` element will always be relative to the webpage. That means that if the element is `fixed` and the declaration `bottom:20px;` is applied to it it will be 20 pixels from the bottom no matter what the parents position is.

Another way it differs(and the way it differs most) from an `absolute` positioned element is the way it behaves on the page when a user scrolls. Where as an `absolute` positioned element is relative to the webpage and will scroll with the page. A `fixed` element is relative to the viewport(what the user sees. It's very similar to the webpage except for you can make something in the webpage exceed the the viewport) and will not scroll with the page. Instead it will stick where it is on the page and not move at all.

#### sticky
`sticky` is the newest of the positioning properties. A `sticky` element will act just like a `static` element until it reaches the top of the viewport. Once it reaches the top of the viewport it will change into something very similar to a fixed element. It will be taken out of the flow  be relative to the and therefor be ignored by the other elements and also it's left, right, top and bottom properties will be based on the viewport.

#### inherit
`inherit` will inherit it's positioning from it's parent. This can be useful as cascading positioning is not a thing.

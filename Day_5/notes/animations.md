# Animation in CSS

#### Transitions
Transitions are used to make an element go from one state to another in a fluid motion.

Transitions are most often used when an element is hovered on/off, clicked or when elements are added/removed from the page.

The only propertie you need to apply for a transition to work is `transition-duration`

**properties**
- transition-duration: How long it takes to get from point a to point b in seconds (e.g. 5s) or milliseconds (e.g. 200ms)
- transition-property: What property you want the transition to apply to (e.g. width). If you leave this property out the transition will apply to all properties
- transition-timing-function: the flow of the animation. The possible values are:
  - ease(default): starts slow, speeds up , then slows down
  - ease-in: animation starts slow
  - ease-out: animation ends slow
  - ease-in-out: animation ends and starts slow
  - cubic-bezier(0,0,0,0): custom animation flow. Possible values are numeric values from 0 to 1
  - linear: same speed from a to b
  - initial: sets value to default value
  - inherit: inherits from parent element
- transition-Delay: How long of a delay until the transition starts in seconds (e.g. 5s) or milliseconds (e.g. 200ms)

Instead of writing out of the above you can use the shorthand `transition` (e.g. `transition: [transition-duration] [transition-property] [transition-timing-function] [transition-delay];`). You can also chain as many transitions as you'd like by separating them with commas (e.g. `transition: 2s width linear 1s, 5s background ease 0.5s;`)

#### CSS Animations
Animations are for more complex animations. Whereas transitions can only go from a to b, animations can have as many stages as you'd like and start from whatever stage.

There are two parts of animations
 - @keyframes rule: specifies the stages of the animations
 - animation properties: specifies what elements the animation will be applied to and how it will be animated

 **@keyframes**
 @keyframes consist of the name of the keyframe (which can be whatever you'd like) followed by each stage of the animation containing declarations for what styles you want applied for that stage.

 For the stages of the animation you can use either percentages or from/to. The pros of  using percentages over from/to is that you can use as many different stages.

 e.g.
 ```
 @keyframes bg-color {
	0% {
		background-color: red;
	}
	100% {
		background-color: yellow;
	}
}
 ```
 ```
 @keyframes example {
	from {background-color: red;}
	to {background-color: yellow;}
}
 ```

 **animation properties**
 There is quite a bit of similarities with the animation properties and the transition properties.

 The only two properties you need to make an animation work is `animation-name` and `animation-duration`.

 - animation-name: name of the animation you called in the @keyframes
 - animation-duration: how long the duration of the animation will play in seconds (e.g. 5s) or milliseconds (e.g. 200ms)
 - animation-timing-function: the flow of the animation, The possible values are:
   - ease(default): starts slow, speeds up , then slows down
   - ease-in: animation starts slow
   - ease-out: animation ends slow
   - ease-in-out: animation ends and starts slow
   - cubic-bezier(0,0,0,0): custom animation flow. Possible values are numeric values from 0 to 1
   - linear: same speed from a to b
   - initial: sets value to default value
   - inherit: inherits from parent element
 - animation-delay: how long to wait before the animation starts in seconds (e.g. 5s) or milliseconds (e.g. 200ms)
 - animation-iteration-count: how many times the animation will play. If you'd like it to continue playing you can set the value to `infinite`
 - animation-direction: which way the animation will play. The possible values for this properties are:
   - normal(default): animation plays forward. The animation resets to the initial state and then plays forward again
   - reverse: animation plays backwards. The animation resets to the end state and then plays backwards
   - alternate: animation reverses direction every cycle. Animation plays forward on odd cycles and backwards on even cycles
   - alternate-reverse: animation reverses direction every cycle. Animation backwards on odd cycles and forward on even cycles
 - animation-fill-mode: specifies whether or not the animation styles are visible before or after the animation plays. The possible values for this properties are:
   - normal(default): animation does not apply any styles to the element before or after the animation
   - forwards: styles defined in the final keyframe stay applied to the element after the animation is finished.
   - backwards: styles defined in the starting keyframe are applied to the element before the animation starts
   - both: animation does will follow both forwards and backwards
 - animation-play-state: specifies if the animation is currently playing or paused.  The possible values for this properties are:
   - running: animation is currently playing
   - paused: animation is currently paused

 Instead of writing out of the above you can use the shorthand `animation` (e.g. `animation: [animation-name] [animation-duration] [animation-timing-function]
[animation-delay] [animation-iteration-count] [animation-direction]
[animation-fill-mode] [animation-play-state];`). You can also chain animations by separating them with commas (e.g. `animation: animation1 1s linear 1s, animation2 1s linear 1s;`)

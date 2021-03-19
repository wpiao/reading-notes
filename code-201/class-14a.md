# Read: 14a - CSS Transforms, Transitions, and Animations 

## CSS Transforms 

```CSS
anyselector {
  transform: rotate(20deg); /* 2D Rotate */
  transform: scale(0.75); /* 2D Scale */
  transform: translate(-10px, 25%); /* 2D Translate */
  transform: skew(5deg, -20deg); /* 2D Skew */
  transform: rotate(25deg) scale(0.75); /* Combining transforms */
  transform: perspective(200px) rotateX(45deg); /* 3D Rotate */
  transform: perspective(200px) scaleZ(1.75) rotateX(45deg); /* 2D Scale */
}
```

## CSS Transitions, and Animations 
```CSS
anyselector {
  transition-propery: background;
  transition-duration: 1s;
  transition-time-function: linea
}
```
@keyframs rule includes the animation name, any animation breakpoints, and the properties intended to animated.

``CSS
.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
}

.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
}

```
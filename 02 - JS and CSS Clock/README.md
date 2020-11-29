## Day 2: JS and CSS Clock

![day2-js-css-clock](../images/day2-js-css-clock.gif)

### What I learned:

- How to convert time (e.g: seconds) into degrees:

```js
// set seconds
const seconds = now.getSeconds();
const secondDegrees = (seconds / 60) * 360 + 90;
secondHand.style.transform = `rotate(${secondDegrees}deg)`;
```

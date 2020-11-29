## Day 1: JavaScript Drum Kit

![day1-drumkit-image](../images/day1-drumkit-image.gif)

### What I learned:

- Key Events
- Playing audio

```js
function playSound(event) {
  const audio = document.querySelector(`audio[data-key="${event.keyCode}"]`);
  const key = document.querySelector(`.key[data-key="${event.keyCode}"]`);
  if (!audio) return; // stop the function from running all together
  audio.currentTime = 0; // rewing to start
  audio.play();
  key.classList.add("playing");
}
```

- Listing for the transition end event

```js
function removeTransition(event) {
  if (event.propertyName !== "transform") return; // skip of it's not a transform
  this.classList.remove("playing");
}
keys.forEach((key) => key.addEventListener("transitionend", removeTransition));
```

# 30 Day Vanilla JS coding challenge course

![js3-social-share](images/JS3-social-share.jpeg)

## Background

I decided to take [30 Day Vanilla JS coding Challenge](https://javascript30.com/) by [@wesbos](https://github.com/wesbos/JavaScript30). By the end of this course, I will build 30 things in 30 days with 30 tutorials.

## Day 1: JavaScript Drum Kit

![day1-drumkit-image](images/day1-drumkit-image.gif)
**[Code :rocket:](/01%20-%20JavaScript%20Drum%20Kit)** | **[Demo :computer:]()**

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

## Useful Links

- [Starter Files for the challenge](https://github.com/wesbos/JavaScript30)
- [JavaScript keycode keypress and key event generator](https://jskeycode.info/).

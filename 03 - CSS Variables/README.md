## Day 3: CSS Variables

![day3-css-variables](../images/day3-css-variables.gif)

### What I learned:

- How to declare CSS variables:

```css
// style.css

:root {
  --base: #ffc600;
  --spacing: 50px;
  --blur: 10px;
}

img {
  padding: var(--spacing);
  background: var(--base);
  filter: blur(var(--blur));
}
```

- And how to update them:

```js
// index.html

function handleUpdate() {
  const suffix = this.dataset.sizing || "";
  document.documentElement.style.setProperty(
    `--${this.name}`,
    this.value + suffix
  );
}
```

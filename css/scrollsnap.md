# Scroll Snap

On an scrolling container, you can specify the scroll snapping automatically, with several options. As usual, MDN has great [documentation](https://developer.mozilla.org/en-US/docs/Web/CSS/scroll-snap-type).

Worth noting: This standard is in flux.

```CSS
#scroll-snap {
  height: 300px;
  width: 300px;
  overflow-x: scroll;
  overflow-y: hidden;
  scroll-snap-type: mandatory;
  scroll-snap-points-x: repeat(100%);
}
```

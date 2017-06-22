# `minmax()`

Being able to do math calculations in JavaScript is super handy. CSS is starting to do that, starting with `calc()`. Now there is a `minmax()` function, which allows you to specify two values and it selects a value greater than the min value and a value lesser than the max value. MDN has great [docs](https://developer.mozilla.org/en-US/docs/Web/CSS/minmax) for it.

```CSS
.width-element {
  width: minmax(500px, 100%);
}
```

# Custom Properties

CSS now provides "variables" in the form of custom properties. There is a great demo of this on [codepen](https://codepen.io/keithclark/pen/qbdVJr)

The idea is that you place your custom properties, with default values, on a `:host` or `:root` selector, and then access the properties inline with the `var()` function. You can use any type of property as a custom property - length, time, percentage, colors, etc.

```CSS
:root {
  --theme-font-size: 125%;
}

p {
  font-size: var(--theme-font-size);
}
```

Then you can adjust the custom properties with JavaScript.

```JavaScript
  var rootStyles = document.styleSheets[0].cssRules[0].style;
  rootStyles.setProperty('--theme-font-size', '24px');
```

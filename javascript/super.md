# `super`

Since classes are so different in Javascript than they are in Java or other popular OOP languages, I wasn't sure how easy it would be to call methods on a parent class. Apparently, it's as easy as you would expect.

```JavaScript
// Define my class
class Person {
  whoami(attribute) {
    return `I am a ${attribute} person.`;
  }
}

// Define my subclass
class Awesome extends Person {
  whoami() {
    return super.whoami('AWESOME!');
  }
}

const me = new Awesome();
console.log(me.whoami());
// 'I am a AWESOME! person.'

```

Cool!

Source: [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super)

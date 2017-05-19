# Class Getters and Setters

When defining a JavaScript class, you can also define getters and setters. They work just like you would expect in any other language:

```JavaScript
class Person {
  constructor(props) {
    this.firstName = props.firstName;
    this.lastName = props.lastName;
  }
  get fullName() {
    return this.firstName + ' ' + this.lastName;
  }
  set fullName(name) {
    const nameArray = name.split(' ');
    this.firstName = nameArray[0];
    this.lastName = nameArray[1];
  }
}

const me = new Person({firstName: "Alex", lastName: "Anderson"});

console.log(me.fullName);
// "Alex Anderson

me.fullName = "Alex Awesome";
console.log(me.lastName);
// "Awesome"
```

You can also define static getters which can be used on the class itself

```JavaScript
class BiasedPerson extends Person {
  static get bestPersonEver() {
    return "That would be Alex Anderson!"
  }
}
console.log(BiasedPerson.bestPersonEver);
// "That would be Alex Anderson!"
```

# Javascript Questions

### 1. What's the output?

```javascript
function sayHi() {
  console.log(name);
  console.log(age);
  var name = 'Rushi';
  let age = 20;
}
sayHi();
```
<b>Answer :- </b>

`undefined` and `ReferenceError`

### 2. What's the output?

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}

for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}
```
<b>Answer :- </b>

`3 3 3`  and  `0 1 2` 

### 3. What's the output?

```javascript
const shape = {
  radius: 10,
  diameter() {
    return this.radius * 2;
  },
  perimeter: () => 2 * Math.PI * this.radius,
};
console.log(shape.diameter());
console.log(shape.perimeter());
```
<b>Answer :- </b>

`20` and `NaN`

### 4. What's the output?

```javascript
+true;
!'Lydia';
```

<b>Answer :- </b>

`1` and `false`


### 5. Which one is true?

```javascript
const bird = {
  size: 'small',
};

const mouse = {
  name: 'Mickey',
  small: true,
};
```
<b>Answer :- </b>

 `mouse.bird.size` is not valid

### 6. What's the output?

```javascript
let c = { greeting: 'Hey!' };
let d;

d = c;
c.greeting = 'Hello';
console.log(d.greeting);
```
<b>Answer :- </b>

`Hello`

### 7. What's the output?

```javascript
let a = 3;
let b = new Number(3);
let c = 3;

console.log(a == b);
console.log(a === b);
console.log(b === c);
```
<b>Answer :- </b>

`true` `false` `false`

### 8. What's the output?

```javascript
class Chameleon {
  static colorChange(newColor) {
    this.newColor = newColor;
    return this.newColor;
  }

  constructor({ newColor = 'green' } = {}) {
    this.newColor = newColor;
  }
}
```
<b>Answer :- </b>

`TypeError`

### 9. What's the output?

```javascript
let greeting;
greetign = {}; // Typo!
console.log(greetign);
```

<b>Answer :- <b/>

 `{}`

### 10. What happens when we do this?

```javascript
function bark() {
  console.log('Woof!');
}

bark.animal = 'dog';
```
<b>Anwser :- </b>

Nothing, this is totally fine!

### 11. What's the output?

```javascript
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const member = new Person('Lydia', 'Hallie');
Person.getFullName = function() {
  return `${this.firstName} ${this.lastName}`;
};

console.log(member.getFullName());
```
<b>Answer:- </b>

`TypeError`

### 12. What's the output?

```javascript
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}

const lydia = new Person('Lydia', 'Hallie');
const sarah = Person('Sarah', 'Smith');

console.log(lydia);
console.log(sarah);
```
<b>Answer :- </b>

`Person {firstName: "Lydia", lastName: "Hallie"}` and `undefined`
  
### 13. What are the three phases of event propagation?

- A: Target > Capturing > Bubbling
- B: Bubbling > Target > Capturing
- C: Target > Bubbling > Capturing
- D: Capturing > Target > Bubbling

<b>Answer: D</b>

During the **capturing** phase, the event goes through the ancestor elements down to the target element. It then reaches the **target** element, and **bubbling** begins.

<img src="https://i.imgur.com/N18oRgd.png" width="200">



### 14. All object have prototypes.

- A: true
- B: false

<b>Answer :- </b>

All objects have prototypes, except for the **base object**. The base object is the object created by the user, or an object that is created using the `new` keyword. The base object has access to some methods and properties, such as `.toString`. This is the reason why you can use built-in JavaScript methods! All of such methods are available on the prototype. Although JavaScript can't find it directly on your object, it goes down the prototype chain and finds it there, which makes it accessible for you.

### 15. What's the output?

```javascript
function sum(a, b) {
  return a + b;
}

sum(1, '2');
```
<b>Answer :- </b>

`"12"`

### 16. What's the output?

```javascript
let number = 0;
console.log(number++);
console.log(++number);
console.log(number);
```
<b>Answer :- <b>

`0` `2` `2`

### 17. What's the output?

```javascript
function getPersonInfo(one, two, three) {
  console.log(one);
  console.log(two);
  console.log(three);
}

const person = 'Lydia';
const age = 21;

getPersonInfo`${person} is ${age} years old`;
```

<b>Answer :-</b>

`["", " is ", " years old"]` `"Lydia"` `21`


### 18. What's the output?

```javascript
function checkAge(data) {
  if (data === { age: 18 }) {
    console.log('You are an adult!');
  } else if (data == { age: 18 }) {
    console.log('You are still an adult.');
  } else {
    console.log(`Hmm.. You don't have an age I guess`);
  }
}

checkAge({ age: 18 });
```
<b>Answer :- </b>

`Hmm.. You don't have an age I guess`

### 19. What's the output?

```javascript
function getAge(...args) {
  console.log(typeof args);
}

getAge(21);
```
<b>Answer :- </b>

`"object"`

### 20. What's the output?

```javascript
function getAge() {
  'use strict';
  age = 21;
  console.log(age);
}

getAge();
```
<b>Answer :- </b>

`ReferenceError`

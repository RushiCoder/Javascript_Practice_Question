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

### 21. What's the value of `sum`?

```javascript
const sum = eval('10*10+5');
```
<b>Answer :-</b>
`105`

### 22. How long is cool_secret accessible?

```javascript
sessionStorage.setItem('cool_secret', 123);
```
<b>Answer :-</b>

 When the user closes the tab.

 ### 23. What's the output?

```javascript
var num = 8;
var num = 10;

console.log(num);
```
<b>Anwer :- </b>

`10`

### 24. What's the output?

```javascript
const obj = { 1: 'a', 2: 'b', 3: 'c' };
const set = new Set([1, 2, 3, 4, 5]);

obj.hasOwnProperty('1');
obj.hasOwnProperty(1);
set.has('1');
set.has(1);
```

<b>Answer :-</b>
`true` `true` `false` `true`

### 25. What's the output?

```javascript
const obj = { a: 'one', b: 'two', a: 'three' };
console.log(obj);
```
<b>Answer :-</b>

`{ a: "three", b: "two" }`

### 26. The JavaScript global execution context creates two things for you: the global object, and the "this" keyword.

<b>Answer :- <b/>

true

### 27. What's the output?

```javascript
for (let i = 1; i < 5; i++) {
  if (i === 3) continue;
  console.log(i);
}
```
<b>Answer:-</b>

`1` `2` `4`

### 28. What's the output?

```javascript
String.prototype.giveLydiaPizza = () => {
  return 'Just give Lydia pizza already!';
};

const name = 'Lydia';

console.log(name.giveLydiaPizza())
```

<b>Answer :-</b>

`"Just give Lydia pizza already!"`

### 29. What's the output?

```javascript
const a = {};
const b = { key: 'b' };
const c = { key: 'c' };

a[b] = 123;
a[c] = 456;

console.log(a[b]);
```
<b>Answer:-</b>

`456`

### 30. What's the output?

```javascript
const foo = () => console.log('First');
const bar = () => setTimeout(() => console.log('Second'));
const baz = () => console.log('Third');

bar();
foo();
baz();
```
<b>Answer :- </b>

`First` `Third` `Second`

### 31. What is the event.target when clicking the button?

```html
<div onclick="console.log('first div')">
  <div onclick="console.log('second div')">
    <button onclick="console.log('button')">
      Click!
    </button>
  </div>
</div>
```
<b>Answer:-</b>

`button`

### 32. When you click the paragraph, what's the logged output?

```html
<div onclick="console.log('div')">
  <p onclick="console.log('p')">
    Click here!
  </p>
</div>
```
<b>Answer:- </b>

`p` `div`

### 33. What's the output?

```javascript
const person = { name: 'Lydia' };

function sayHi(age) {
  return `${this.name} is ${age}`;
}

console.log(sayHi.call(person, 21));
console.log(sayHi.bind(person, 21));
```
<b>Answer:-</b>

`function` `function`

### 34. What's the output?

```javascript
function sayHi() {
  return (() => 0)();
}

console.log(typeof sayHi());
```
<b>Answer:-</b>

`"number"`
### 35. Which of these values are falsy?

```javascript
0;
new Number(0);
('');
(' ');
new Boolean(false);
undefined;
```
<b>Answer:-</b>

`0`, `''`, `undefined`

### 36. What's the output?

```javascript
console.log(typeof typeof 1);
```
<b>Answer :-</b>

`"string"`

### 37. What's the output?

```javascript
const numbers = [1, 2, 3];
numbers[10] = 11;
console.log(numbers);
```
<b>Answer :-</b>

`[1, 2, 3, empty x 7, 11]`

### 38. What's the output?

```javascript
(() => {
  let x, y;
  try {
    throw new Error();
  } catch (x) {
    (x = 1), (y = 2);
    console.log(x);
  }
  console.log(x);
  console.log(y);
})();
```
<b>Answer :-</b>

`undefined` `undefined` `undefined`

### 39. Everything in JavaScript is either a...

<b>Answer :-</b>

primitive or object

JavaScript only has primitive types and objects.

Primitive types are `boolean`, `null`, `undefined`, `bigint`, `number`, `string`, and `symbol`.

What differentiates a primitive from an object is that primitives do not have any properties or methods; however, you'll note that `'foo'.toUpperCase()` evaluates to `'FOO'` and does not result in a `TypeError`. This is because when you try to access a property or method on a primitive like a string, JavaScript will implicitly wrap the primitive type using one of the wrapper classes, i.e. `String`, and then immediately discard the wrapper after the expression evaluates. All primitives except for `null` and `undefined` exhibit this behaviour.

### 40. What's the output?

```javascript
[[0, 1], [2, 3]].reduce(
  (acc, cur) => {
    return acc.concat(cur);
  },
  [1, 2],
);
```
<b>Answer :-</b>

`[1, 2, 0, 1, 2, 3]`

### 41. What's the output?

```javascript
!!null;
!!'';
!!1;
```
<b>Answer :- </b>

`false` `false` `true`

###### 42. What does the `setInterval` method return in the browser?

```javascript
setInterval(() => console.log('Hi'), 1000);
```

<b>Answer :-</b>

a unique id


### 43. What does this return?

```javascript
[...'India'];
```

<b>Answer :-</b>

 `["I", "n", "d", "i", "a"]`

 ### 44. What's the output?

```javascript
function* generator(i) {
  yield i;
  yield i * 2;
}

const gen = generator(10);

console.log(gen.next().value);
console.log(gen.next().value);
```

<b>Answer :-</b>

`10, 20`

### 45. What does this return?

```javascript
const firstPromise = new Promise((res, rej) => {
  setTimeout(res, 500, 'one');
});

const secondPromise = new Promise((res, rej) => {
  setTimeout(res, 100, 'two');
});

Promise.race([firstPromise, secondPromise]).then(res => console.log(res));
```
<b>Answer :-</b>

`"two"`

### 46. What's the output?

```javascript
let person = { name: 'Lydia' };
const members = [person];
person = null;

console.log(members);
```
<b>Answer :-</b>

`[{ name: "Lydia" }]`

### 47. What's the output?

```javascript
const person = {
  name: 'Lydia',
  age: 21,
};

for (const item in person) {
  console.log(item);
}
```
<b>Answer :-</b>

`"name", "age"`

### 48. What's the output?

```javascript
console.log(3 + 4 + '5');
```
<b>Answer :-</b>

`"75"`

### 49. What's the value of `num`?

```javascript
const num = parseInt('7*6', 10);
```
<b>Answer :-</b>

`7`

### 50. What's the output?

```javascript
[1, 2, 3].map(num => {
  if (typeof num === 'number') return;
  return num * 2;
});
```
<b>Answer :-</b>

`[undefined, undefined, undefined]`

### 51. What's the output?

```javascript
function getInfo(member, year) {
  member.name = 'Lydia';
  year = '1998';
}

const person = { name: 'Sarah' };
const birthYear = '1997';

getInfo(person, birthYear);

console.log(person, birthYear);
```
<b>Answer :-</b>

`{ name: "Lydia" }, "1997"`

### 52. What's the output?

```javascript
function greeting() {
  throw 'Hello world!';
}

function sayHi() {
  try {
    const data = greeting();
    console.log('It worked!', data);
  } catch (e) {
    console.log('Oh no an error:', e);
  }
}

sayHi();
```
<b>Answer :-</b>

`Oh no an error: Hello world!`

### 53. What's the output?

```javascript
function Car() {
  this.make = 'Lamborghini';
  return { make: 'Maserati' };
}

const myCar = new Car();
console.log(myCar.make);
```
<b>Answer :-</b>

`"Maserati"`

### 54. What's the output?

```javascript
(() => {
  let x = (y = 10);
})();

console.log(typeof x);
console.log(typeof y);
```
<b>Answer :-</b>

`"undefined", "number"`

### 55. What's the output?

```javascript
class Dog {
  constructor(name) {
    this.name = name;
  }
}

Dog.prototype.bark = function() {
  console.log(`Woof I am ${this.name}`);
};

const pet = new Dog('Mara');

pet.bark();

delete Dog.prototype.bark;

pet.bark();
```
<b>Answer :-</b>

`"Woof I am Mara"`, `TypeError`

### 56. What's the output?

```javascript
const set = new Set([1, 1, 2, 3, 4]);

console.log(set);
```
<b>Answer :-</b>

`{1, 2, 3, 4}`

### 57. What's the output?

```javascript
// counter.js
let counter = 10;
export default counter;
```

```javascript
// index.js
import myCounter from './counter';

myCounter += 1;

console.log(myCounter);
```
<b>Answer :-</b>

`Error`

### 58. What's the output?

```javascript
const name = 'Lydia';
age = 21;

console.log(delete name);
console.log(delete age);
```
<b>Answer :-</b>

`false`, `true`

### 59. What's the output?

```javascript
const numbers = [1, 2, 3, 4, 5];
const [y] = numbers;

console.log(y);
```
<b>Answer :-</b>

`1`

### 60. What's the output?

```javascript
const user = { name: 'Lydia', age: 21 };
const admin = { admin: true, ...user };

console.log(admin);
```
<b>Answer :-</b>

`{ admin: true, name: "Lydia", age: 21 }`

### 62. What's the output?

```javascript
const settings = {
  username: 'lydiahallie',
  level: 19,
  health: 90,
};

const data = JSON.stringify(settings, ['level', 'health']);
console.log(data);
```
<b>Answer :-</b>

`"{"level":19, "health":90}"`

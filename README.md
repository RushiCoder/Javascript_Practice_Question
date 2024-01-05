 # JavaScript Questions

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

### 61. What's the output?

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

### 62. What's the output?

```javascript
const person = { name: 'Lydia' };

Object.defineProperty(person, 'age', { value: 21 });

console.log(person);
console.log(Object.keys(person));
```
<b>Answer :-</b>

`{ name: "Lydia", age: 21 }`, `["name"]`

### 63. What's the output?

```javascript
let num = 10;

const increaseNumber = () => num++;
const increasePassedNumber = number => number++;

const num1 = increaseNumber();
const num2 = increasePassedNumber(num1);

console.log(num1);
console.log(num2);
```
<b>Answer :-</b>

`10`, `10`

### 64. What's the output?

```javascript
const value = { number: 10 };

const multiply = (x = { ...value }) => {
  console.log((x.number *= 2));
};

multiply();
multiply();
multiply(value);
multiply(value);
```
<b>Answer :-</b>

`20`, `20`, `20`, `40`

### 65. What's the output?

```javascript
[1, 2, 3, 4].reduce((x, y) => console.log(x, y));
```
<b>Answer :-</b>

`1` `2` and `undefined` `3` and `undefined` `4`

### 66. With which constructor can we successfully extend the `Dog` class?

```javascript
class Dog {
  constructor(name) {
    this.name = name;
  }
};

class Labrador extends Dog {
  // 1
  constructor(name, size) {
    this.size = size;
  }
  // 2
  constructor(name, size) {
    super(name);
    this.size = size;
  }
  // 3
  constructor(size) {
    super(name);
    this.size = size;
  }
  // 4
  constructor(name, size) {
    this.name = name;
    this.size = size;
  }

};
```
<b>Answer :-</b>

2

### 67. What's the output?

```javascript
// index.js
console.log('running index.js');
import { sum } from './sum.js';
console.log(sum(1, 2));

// sum.js
console.log('running sum.js');
export const sum = (a, b) => a + b;
```
<b>Answer :-</b>

`running sum.js`, `running index.js`, `3`

### 68. What's the output?

```javascript
console.log(Number(2) === Number(2));
console.log(Boolean(false) === Boolean(false));
console.log(Symbol('foo') === Symbol('foo'));
```
<b>Answer :-</b>

`true`, `true`, `false`

### 69. What's the output?

```javascript
const name = 'Lydia Hallie';
console.log(name.padStart(13));
console.log(name.padStart(2));
```
<b>Answer :-</b>

`" Lydia Hallie"`, `"Lydia Hallie"` (`"[1x whitespace]Lydia Hallie"`, `"Lydia Hallie"`)

### 70. What's the output?

```javascript
console.log('🥑' + '💻');
```
<b>Answer :-</b>

`"🥑💻"`

### 71. How can we log the values that are commented out after the console.log statement?

```javascript
function* startGame() {
  const answer = yield 'Do you love JavaScript?';
  if (answer !== 'Yes') {
    return "Oh wow... Guess we're done here";
  }
  return 'JavaScript loves you back ❤️';
}

const game = startGame();
console.log(/* 1 */); // Do you love JavaScript?
console.log(/* 2 */); // JavaScript loves you back ❤️
```
<b>Answer :-</b>

`game.next().value` and `game.next("Yes").value`

### 72. What's the output?

```javascript
async function getData() {
  return await Promise.resolve('I made it!');
}

const data = getData();
console.log(data);
```
<b>Answer :-</b>

`Promise {<pending>}`

### 73. What's the output?

```javascript
function addToList(item, list) {
  return list.push(item);
}

const result = addToList('apple', ['banana']);
console.log(result);
```
<b>Answer :-</b>

`2`

### 74. What's the output?

```javascript
const box = { x: 10, y: 20 };

Object.freeze(box);

const shape = box;
shape.x = 100;

console.log(shape);
```
<b>Answer :-</b>

`{ x: 10, y: 20 }`

### 75. What's the output?

```javascript
const { firstName: myName } = { firstName: 'Lydia' };

console.log(firstName);
```
<b>Answer :-</b>

`ReferenceError`

### 76. Is this a pure function?

```javascript
function sum(a, b) {
  return a + b;
}
```
<b>Answer :-</b>
Yes

### 77. What is the output?

```javascript
const add = () => {
  const cache = {};
  return num => {
    if (num in cache) {
      return `From cache! ${cache[num]}`;
    } else {
      const result = num + 10;
      cache[num] = result;
      return `Calculated! ${result}`;
    }
  };
};

const addFunction = add();
console.log(addFunction(10));
console.log(addFunction(10));
console.log(addFunction(5 * 2));
```
<b>Answer :-</b>

`Calculated! 20` `From cache! 20` `From cache! 20`

### 78. What is the output?

```javascript
const myLifeSummedUp = ['☕', '💻', '🍷', '🍫'];

for (let item in myLifeSummedUp) {
  console.log(item);
}

for (let item of myLifeSummedUp) {
  console.log(item);
}
```
<b>Answer :-</b>

`0` `1` `2` `3` and `"☕"` `"💻"` `"🍷"` `"🍫"`

### 79. What is the output?

```javascript
const list = [1 + 2, 1 * 2, 1 / 2];
console.log(list);
```
<b>Answer :-</b>

`[3, 2, 0.5]`

### 80. What is the output?

```javascript
function sayHi(name) {
  return `Hi there, ${name}`;
}

console.log(sayHi());
```
<b>Answer :-</b>

`Hi there, undefined`

### 81. What is the output?

```javascript
var status = '😎';

setTimeout(() => {
  const status = '😍';

  const data = {
    status: '🥑',
    getStatus() {
      return this.status;
    },
  };

  console.log(data.getStatus());
  console.log(data.getStatus.call(this));
}, 0);
```
<b>Answer :-</b>

`"🥑"` and `"😎"`

### 82. What is the output?

```javascript
const person = {
  name: 'Lydia',
  age: 21,
};

let city = person.city;
city = 'Amsterdam';

console.log(person);
```
<b>Answer :-</b>

- A: `{ name: "Lydia", age: 21 }`

### 83. What is the output?

```javascript
function checkAge(age) {
  if (age < 18) {
    const message = "Sorry, you're too young.";
  } else {
    const message = "Yay! You're old enough!";
  }

  return message;
}

console.log(checkAge(21));
```
<b>Answer :-</b>

`ReferenceError`

### 84. What kind of information would get logged?

```javascript
fetch('https://www.website.com/api/user/1')
  .then(res => res.json())
  .then(res => console.log(res));
```
<b>Answer :-</b>

The result of the callback in the previous `.then()`.

### 85. Which option is a way to set `hasName` equal to `true`, provided you cannot pass `true` as an argument?

```javascript
function getName(name) {
  const hasName = //
}
```
<b>Answer :-</b>

`!!name`

### 86. What's the output?

```javascript
console.log('I want pizza'[0]);
```
<b>Answer :-</b>

`"I"`

### 87. What's the output?

```javascript
function sum(num1, num2 = num1) {
  console.log(num1 + num2);
}

sum(10);
```
<b>Answer :-</b>

`20`

### 88. What's the output?

```javascript
// module.js
export default () => 'Hello world';
export const name = 'Lydia';

// index.js
import * as data from './module';

console.log(data);
```
<b>Answer :-</b>

`{ default: function default(), name: "Lydia" }`

### 89. What's the output?

```javascript
class Person {
  constructor(name) {
    this.name = name;
  }
}

const member = new Person('John');
console.log(typeof member);
```
<b>Answer :-</b>

`"object"`

### 90. What's the output?

```javascript
let newList = [1, 2, 3].push(4);

console.log(newList.push(5));
```
<b>Answer :-</b>

`Error`

### 91. What's the output?

```javascript
function giveLydiaPizza() {
  return 'Here is pizza!';
}

const giveLydiaChocolate = () =>
  "Here's chocolate... now go hit the gym already.";

console.log(giveLydiaPizza.prototype);
console.log(giveLydiaChocolate.prototype);
```
<b>Answer :-</b>

`{ constructor: ...}` `undefined`

### 92. What's the output?

```javascript
const person = {
  name: 'Lydia',
  age: 21,
};

for (const [x, y] of Object.entries(person)) {
  console.log(x, y);
}
```
<b>Answer :-</b>

`name` `Lydia` and `age` `21`

### 93. What's the output?

```javascript
function getItems(fruitList, ...args, favoriteFruit) {
  return [...fruitList, ...args, favoriteFruit]
}

getItems(["banana", "apple"], "pear", "orange")
```
<b>Answer :-</b>

`SyntaxError`

### 94. What's the output?

```javascript
class Person {
  constructor() {
    this.name = 'Lydia';
  }
}

Person = class AnotherPerson {
  constructor() {
    this.name = 'Sarah';
  }
};

const member = new Person();
console.log(member.name);
```
<b>Answer :-</b>

`"Sarah"`

### 95. What's the output?

```javascript
const info = {
  [Symbol('a')]: 'b',
};

console.log(info);
console.log(Object.keys(info));
```
<b>Answer :-</b>

`{Symbol('a'): 'b'}` and `[]`

### 96. What's the output?

```javascript
const getList = ([x, ...y]) => [x, y]
const getUser = user => { name: user.name, age: user.age }

const list = [1, 2, 3, 4]
const user = { name: "Lydia", age: 21 }

console.log(getList(list))
console.log(getUser(user))
```
<b>Answer :-</b>

`[1, [2, 3, 4]]` and `SyntaxError`

### 97. What's the output?

```javascript
const name = 'Lydia';

console.log(name());
```
<b>Answer :-</b>

`TypeError`
### 98. What's the value of output?

```javascript
// 🎉✨ This is my 100th question! ✨🎉

const output = `${[] && 'Im'}possible!
You should${'' && `n't`} see a therapist after so much JavaScript lol`;
```
<b>Answer :-</b>

`Impossible! You should see a therapist after so much JavaScript lol`

### 99. What's the value of output?

```javascript
const one = false || {} || null;
const two = null || false || '';
const three = [] || 0 || true;

console.log(one, two, three);
```
<b>Answer :-</b>

 `{}` `""` `[]`

### 100. What's the value of output?

```javascript
const myPromise = () => Promise.resolve('I have resolved!');

function firstFunction() {
  myPromise().then(res => console.log(res));
  console.log('second');
}

async function secondFunction() {
  console.log(await myPromise());
  console.log('second');
}

firstFunction();
secondFunction();
```
<b>Answer :-</b>


`second`, `I have resolved!` and `I have resolved!`, `second`

### 101. What's the value of output?

```javascript
const set = new Set();

set.add(1);
set.add('Lydia');
set.add({ name: 'Lydia' });

for (let item of set) {
  console.log(item + 2);
}
```
<b>Answer :-</b>

`3`, `Lydia2`, `[object Object]2`

### 103. What's the value of output?

```javascript
const set = new Set();

set.add(1);
set.add('Lydia');
set.add({ name: 'Lydia' });

for (let item of set) {
  console.log(item + 2);
}
```
<b>Answer :-</b>

`3`, `Lydia2`, `[object Object]2`

### 104. What's its value?

```javascript
Promise.resolve(5);
```
<b>Answer :-</b>

`Promise {<fulfilled>: 5}`

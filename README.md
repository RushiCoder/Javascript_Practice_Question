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


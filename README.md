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

`3 3 3` and `0 1 2` 

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


# My JavaScript Style Guide

   1.Use `const` or `let` , avoid using `var`
 
```js
    // bad 
var a = 1;
var b = 2;

    // good 
let a = 1;
const b = 2; 
``` 

2.Use `===` and `!==` over `==` and `!=`
   
```js
    // bad
1 == '1' //true
1 === '1' //false
    
    // good
1 !== '1' //true
1 != '1' //false
```

3.Use shortcuts for booleans, but explicit comparisons for strings and numbers.

```js
// bad
if (isValid === true) {}
if (name) {}
if (collection.length) {}

// good
if (isValid) {}
if (name !== '') {}
if (collection.length > 0) {}
```

4.Ternaries should not be nested and generally be single line expressions.
```js
    // bad
const foo = maybe1 > maybe2
  ? "bar"
  : value1 > value2 ? "baz" : null;

    // good
const maybeNull = value1 > value2 ? 'baz' : null;
const foo = maybe1 > maybe2 ? 'bar' : maybeNull;
```

 5.Avoid unneeded ternary statements. 
```js
// bad
const foo = a ? a : b;
const bar = c ? true : false;
const baz = c ? false : true;

// good
const foo = a || b;
const bar = !!c;
const baz = !c;
```

6.Avoid single letter names. 
Be descriptive with your naming.
Use camelCase when naming objects, functions, and instances.
Use PascalCase only when naming constructors or classes.

```js
    // bad
let obj = {};
function func(){};
class myClass {};

    // good
let myObject ={};
function sumEvenNumbers(){};
class MyClass {};
```

7.Terminate your statements with semicolons ;.

```js
    // bad
const myObj = {}

    // good
const myObj ={};
```

8.Additional trailing comma

```js
    // bad
const webHeroes = {
  firstName: 'Dana',
  lastName: 'Scully'
};

    // good
const webHeroes = {
  firstName: 'Dana',
  lastName: 'Scully',
};
```

9.Set off operators with spaces. 

```js
// bad
const x=y+5;

// good
const x = y + 5;
```

10.Start all comments with a space to make it easier to read.
```js
// bad
//is current tab
const active = true;

// good
// is current tab
const active = true;
```
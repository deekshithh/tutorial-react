# Next-generation JavaScript

Next-generation JavaScript could be thought of as the latest version of ECMAScript, the standardized specification for JavaScript. Each version endeavors to improve upon and add new functionality to this increasingly popular programming language. [Source link](https://mp4-a.udemycdn.com/2018-02-24_15-07-52-641f1a20850d31648cdb7a0b8996a6d2/original.pdf?ESQtNT-s8xssnXRemh553sKK0J8vRdlAxiDlCnIT4eKnxVWibttcCZelWQ0fFdI6DhAdkaQ_VuYNaw0Qc0auZ1XvrRV-9LSv-aw-vOhHE5Y7C2F77rF2ZYy4_6WgmKHpCErpqphVuWhO_jD18MR3UqxOIiW7M0ktmFftjLDWWmo)

## let & const
These keywords were introduced in ES6.

**let**: used to store variable values.   
**const**: used to store constant values.

## Arrow functions
Arrow functions allow us to write shorter function syntax.

```javascript
const hello = () => {
  return "Hello World!";
}
```

## Exports and Imports(Modules)

In React projects (and actually in all modern JavaScript projects), you split your code across multiple JavaScript files - so-called modules. You do this, to keep each file/module focused and manageable.To still access functionality in another file, you need export (to make it available) and import (to getaccess) statements.

You got two different types of exports: default (unnamed) and namedexports:
```javascript
default => export default ...; 
named => export const someData = ...; 
```

You can import default exports like below. Surprisingly, someNameOfYourChoice is totally up to you.
```javascript
import someNameOfYourChoice from './path/to/file.js'; 
```

Named exports have to be imported by their name:
```javascript
import { someData } from './path/to/file.js';
```

A file can only contain one default and an unlimited amount of named exports. You can also mix the one default with any amount of named exports in one and the same file. When importing named exports, you can also import all named exports at once with the following syntax:
```javascript
import * as upToYou from './path/to/file.js';
const a = upToYou.someData;
```

## Understanding Classes

Classes are a feature which basically replace constructor functions and prototypes. You can define blueprints for JavaScript objects with them. 

```javascript
class Human {
  species = 'human';
}

class Person extends Human {
  // property(similar to variables)
  name = 'Max';
  // method(similar to functions)
  printMyName = () => {
    console.log(this.name);
  }
}

const person = new Person();
person.printMyName(); // prints 'Max'
console.log(person.species); // prints 'humam'
```

## Spread & Rest Operator

The spread and rest operators actually use the same syntax: `...`
It's usage determines whether you're using it as the spread or rest operator.

**Spread:**
The spread operator allows you to pull elements out of an array (=> split the array into a list of its elements) or pull the properties out of an object.

```javascript
const oldArray = [1, 2, 3];
const newArray = [...oldArray, 4, 5]; // This now is [1, 2,3, 4, 5];

const oldObject = {
  name: 'Max'
};
const newObject = {
  ...oldObject,
  age: 28
};
// result
// {
//   name: 'Max',
//   age: 28
// }
```

**Rest:**
It is used to pass unlimited number of arguments to the function.

```
const even_numbers = (...numbers)=>{
  return numbers.filter( num => (num%2 == 0) }  
}

console.log(even_numbers(1,2,3,4)); // returns [3,4]
```

## Destructuring

Destructuring allows you to easily access the values of arrays or objects and assign them to variables.

```javascript
const array = [1, 2, 3];
const [a, b] = array;
consolelog(a); // prints 1
consolelog(b); // prints 2
consolelog(array); // prints [1, 2, 3]

const myObj = {
  name: 'Max',
  age: 28
}
const {name} = myObj;
consolelog(name); // prints 'Max'
consolelog(age); // prints undefined
consolelog(myObj); // prints {name: 'Max', age: 28}
```

Destructuring is very useful when working with function arguments. Consider this example:

```javascript
const printName = (personObj) => {
  consolelog(personObjname);
}
printName({name: 'Max', age: 28}); // prints 'Max'

const printName = ({name}) => {
  consolelog(name);
}
printName({name: 'Max', age: 28}); // prints 'Max')
```

## Reference and primitive types

An explanation of JavaScript's pass-by-value, which is unlike pass-by-reference from other languages.

**Primitive Types:**
The in-memory value of a primitive type is it's actual value (e.g. boolean `true`, number `42`). A primitive type can be stored in the fixed amount of memory available.

- null
- undefined
- Boolean
- Number
- String

Primitive types are also known as: scalar types or simple types.

**Reference Types:**
A reference type can contain other values. Since the contents of a reference type can not fit in the fixed amount of memory available for a variable, the in-memory value of a reference type is the reference itself (a memory address).

- Array
- Object
- Function

Reference types are also known as: complex types or container types.

## Array functions
[10 JavaScript array methods you should know](https://dev.to/frugencefidel/10-javascript-array-methods-you-should-know-4lk3).  
[A list of all array functios](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)






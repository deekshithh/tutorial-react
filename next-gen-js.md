# Next-generation JavaScript

Next-generation JavaScript could be thought of as the latest version of ECMAScript, the standardized specification for JavaScript. Each version endeavors to improve upon and add new functionality to this increasingly popular programming language.

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

## 

---
title: Javascript
createDate: 2024-11-16
published: 
tags:
  - Javascript
---
## Miscellaneous
- Using `//` for 1 line comment, `/* */` for multi-line comments
- JS can be execute without `;` but it's minified need to be `;`
- Variable and function name are case sensitive
- Variables/functions should be names with format camel case (`nameOfVariable`)
	- Name a constant: `const FAV_PET = 'Cat'`
	- `UpperCamelCase` should be used by conversion for ES6 class names.
- Using `\` for special characters, for example `\"` for `"` inside double quote
## Practice directly on the browser
Open the browser (I use `Brave`), press `F12` to open *Inspect* window, then choose tab `Console`. Now you can practice on this console window, for example, try with `console.log("Hello World")` end press `Enter`
## ES6
- "ES" = "**E**CM**S**cript" ~ "Javascript"
- Most of browser use ES6 but not all
- ES6 = ES2015
- New feature: `Arrow Function`, `Classes`, `Modules`, `Promise`, `Generator`, `let` and `const`
- Read more about ES on w3schools.
### Concise things
```js title="main.js"
// Concise Object Literal Declaration
const getMousePosition = (x, y) => ({ x, y});
```

```js title="main.js"
// Concise Declarative Functions
const persons = {
	name: "Nam Nguyen",
	sayHello() {
		return `Hello. My name is ${this.name}`; // Hello. My Name is Nam Nguyen
	}
}
```

### Getters and setters
```js title="main.js"
class Book {
	constructor(author) {
		this._author = author;
	}

	// getter
	get author() {
		return this._author;
	}

	// setter
	set author(author) {
		this._author = author;
	}
}

const book = new Book('anonymous');
console.log(book.author); // anonymous
```

## Export/Import to share code blocks
```js title="calculator.js"
const add = (x, y) => x + y;
const subtract = (x, y) => x - y;

export { add, subtract};

export default function (x, y) {
	return x + y;
}
```

```js title="main.js"
import { add, subtract } from './calculator.js' // only add, subtract
import * as everthing from './calculator.js'; // everything
import anything from './calculator.js' // import default
```

## Declare variables & scope
```js title="main.js"
var name; // global scope
let age; // ES6, block scope (inside {} or function,...)
const PI = 3.14; // ES6 can't be changed
```

```js title="main.js"
function funcName() {
	let nameInFuc = 'anonymous'; 
}


console.log(nameInFuc); // undefined

```

> [!multi-column]
> 
>> [!example] Var Bl
>> ```js
>> var a = 1;
>> var a = 2; // ok a = 2 now
>> a = 5; // ok a = 5 now
>>```
>
>> [!]


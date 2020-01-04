# JavaScript ES6 Modules 🎒

`Author : Maye Edwin`

**Modules** in javascript allow you to split JavaScript programs up into separate **chuncks** that can be imported when needed.

**Modern browsers** now support module functionality natively - browsers can optimize loading of modules,
making it more efficient than having to use a library to achieve the same.

### Why modules?

1.  Maintainability

2.  Resusability

3.  Perfomance

4.  Productivity

Read more [about JavaScript Modules](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules).

### Using Modules ( Export and Import )

`export` : is used to expose public variables, functions and classes.

```javascript
   // Add.js
    const Add = () {
       return a + b;
    }

    export { Add }
```

`import` : is then used to pull items from a module into another script or module.

```javascript
// App.js
import { Sum } from "./Add.js";
console.log(Add(1, 2)); // 3
```

### Advanced Recipe

A single `export` statement can be used as shown below.

```javascript
export { Add, Subtract };
```

A single `import` statement can be used as shown below for all public items.

```javascript
import { Add, Subtract } from "./Calculate.js";
```

Or use `export` as you declare a function, class or variable.

```javascript
   // export a function
   export const Add = () {
     return a + b ;
   }

   // or a variable
   export let name = `Maye Edwin`;
```

Or use `as` and `*` to import all exports from a given module.

```javascript
import * as App from "./Calculate.js";

// using each export
App.Add();
App.Divide();
```

Or use `as` to import an export or exports from a given module (helps to prevent naming problems).

```javascript
import { user as Bio } from "./Users.js";
import { sum as Add, product as Multiply } from "./Calculator.js";
```

It's possible to re-export a **module** - also called aggregating

```js
// re-export a module
export { name } from './Module.js';

// an equivalent to
import { name } from './Module.js';
export name;
```

There are two different types of export,
**named** and **default**. You can have **multiple named exports per module** but only **one default export**.

**Named exports** are useful to export several values. During the import, it is mandatory to use the same name of the corresponding object.

```js
// 1.0 named export
export let age = 30;
```

a) Importing the named export....

```js
// 1.0 named import
import { age } from "./Module.js";
```

But a **default export** can be imported with any name.

```js
// 2.0 default export
let age = 30;
export default age;
```

b) Importing default export...

```js
// 2.0 default export import - we have freedom to use any name
import { aged } from "./Module.js";
```

All **module import** scripts must be loaded by setting a **type="module"** attribute in the **<script>** tag.

```javascript
<script type="module" src="./App.js"></script>
```

## The challenge 👷

Add subtraction, multiplication and division modules to this app! Good luck!

## Setting up the project

### Styling

All file names start with **capital letter** for scripts and styles. Example : `App.js` or `App.css`

### ← README.md

That's this file, where I tell people what your cool website does and how you built it.

### ← index.html

Where you'll write more content of your remix.

### ← App.css

CSS files add styling rules this web app.

### ← App.js

The main `Modules` import file.

### ← assets

Drag in `assets`, like images or music, to add them to your project.

## Made by [Maye Edwin](https://github.com/mayeedwin)

\ ゜ o ゜)ノ

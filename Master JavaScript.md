# Javascript

## JavaScript Syntax





## JavaScript Objects





## JavaScript Functions

JavaScript functions are **defined** with the `function` keyword.

### Function Declaratons

```javascript
function functionName(parameters) {
  // code to be executed
} 
```

Declared functions are not executed immediately. 

They are "saved for later use",  and will be executed later, when they are **invoked** (called upon).



#### Function Expressions

A JavaScript function can also be defined using an **expression**.

A function expression can be stored in a variable:

```javascript
var x = function (a, b) {return a * b};
```

The function above is actually an **anonymous function** (a function without a  name).

Functions stored in variables do not need function names. They are always  invoked (called) using the variable name.



#### The Function() Constructor

Functions can also be defined with a built-in JavaScript function constructor called  `Function()`.

```javascript
var myFunction = new Function("a", "b", "return a * b");

var x = myFunction(4, 3); 
```

Most of the time, you can avoid using the `new` keyword in JavaScript.



#### Function Hoisting

Hoisting is JavaScript's default behavior of moving declarations to the  top.

Hoisting applies to **variable declarations** and to **function declarations**.

Functions defined using an expression are **not** hoisted.



#### Self-Invoking Functions

Function expressions can be made "self-invoking".

A self-invoking expression is invoked (started) automatically, without being called.

Function expressions will execute automatically if the expression is followed  by ().

You cannot self-invoke a function declaration.

You have to add  parentheses around the function to indicate that it is a function expression:

```javascript
(function () {
  var x = "Hello!!";  // I will invoke myself
})();
```

The function above is actually an **anonymous self-invoking function** (function  without name).



#### Functions Can Be Used as Values

```javascript
function myFunction(a, b) {
  return a * b;
}

var x = myFunction(4, 3); 
```



#### Functions are Objects

The `typeof` operator in JavaScript returns "function" for  functions.

But, JavaScript functions can best be described as objects.

JavaScript functions have both **properties** and  **methods**.

The `arguments.length` property returns the number of arguments received when  the function was invoked:

The `toString()` method returns the function as a string.



A function defined as the property of an object, is called a **method** to the object.

A function designed to create new objects, is called an **object constructor**.



#### Arrow Functions

Arrow functions allows a short syntax for writing function expressions.

You don't need the `function` keyword, the `return` keyword, and the  **curly brackets**.

```javascript
// ES5
var x = function(x, y) {
  return x * y;
}

// ES6
const x = (x, y) => x * y;
```

Arrow functions do **not** have their own `this`. They are not well suited for defining **object methods**.

Arrow functions are **not** hoisted. They must be defined **before** they are used.

Using `const` is safer than using `var`, because a function expression is  always constant value.

You can only omit the `return` keyword and the curly brackets if the function is a single statement.  Because of this, it might be a good habit to always keep them



### Function Parameters





### Function Invocation





### Function Call





### Function Apply





#### Function Closures





## JavaScript HTML DOM





## JavaScript Browser BOM


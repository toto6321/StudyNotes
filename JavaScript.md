# JavaScript

#### Main References:

* https://www.w3schools.com/js/default.asp
* https://developer.mozilla.org/en-US/docs/Web/JavaScript



## JavaScript Syntax

### JS Data Type

* Primitives Data Types 
  * undefined
  * Boolean
    * true
    * false
  * Number
    * number 
      * 64 bits  double-precision floating-point 
        * sign bit: 1
        * exponent bits: 11
        * significand precision: 53
      * Integar: -(2^53-1) to 2^53-1, aka, Number.MIN_SAFE_INTEGER to Number.MAX_SAFE_INTEGER)
      * 0 === -0 === +0
    * Infinity
    * -Infinity
    * NaN
  * String
  * BigInt
  * Symbol
* special primitive type
  * null
* special non-data but structural type
  * Object
* a non-data structure
  * Function



```javascript
typeof undefined // "undefined"

typeof Boolean // "function"
typeof Number // "function"
typeof String // "function"
typeof BigInt // "function"
typeof Symbol // "function"

typeof null // "object"
typeof Object // "function"
typeof Function // "function"

typeof 
```





### JS Type Conversion

| Original Value   | Converted to Number               | Converted to String | Converted to Boolean |
| ---------------- | --------------------------------- | ------------------- | -------------------- |
| false            | 0                                 | "false"             | false                |
| true             | 1                                 | "true"              | true                 |
| 0                | 0                                 | "0"                 | false                |
| 1                | 1                                 | "1"                 | true                 |
| "0"              | 0                                 | "0"                 | <strong style="color:red">true</strong> |
| "000"            | 0                                 | "000"               | <strong style="color:red">true</strong> |
| "1"              | 1                                 | "1"                 | true                 |
| NaN              | NaN                               | "NaN"               | false                |
| Infinity         | Infinity                          | "Infinity"          | true                 |
| -Infinity        | -Infinity                         | "-Infinity"         | true                 |
| ""               | 0                                 | ""                  | <strong style="color:red">false</strong> |
| "20"             | 20                                | "20"                | true                 |
| "twenty"         | NaN                               | "twenty"            | true                 |
| [ ]              | 0                                 | ""                  | <strong style="color:red">true</strong> |
| [20]             | <strong style="color:red">20</strong> | "20"                | true                 |
| [10,20]          | <strong style="color:red">NaN</strong> | "10,20"            | true                 |
| ["twenty"]       | NaN                               | "twenty"            | true                 |
| ["ten","twenty"] | NaN                               | "ten,twenty"       | true                 |
| function(){}     |        <strong style="color:red">NaN</strong>                           | <strong style="color:red">"function(){}"</strong> | <strong style="color:red">true</strong> |
| { }              | <strong style="color:red">NaN</strong> | <strong style="color:red">"[object Object]"</strong> | <strong style="color:red">true</strong> |
| null             | <strong style="color:red">0</strong>   | "null"              | false                |
| undefined        | NaN                               | "undefined"         | false                |

```javascript
(!(~+[])+{})[--[~+""][+[]]*[~+[]] + ~~!+[]]+({}+[])[[~!+[]]*~+[]]

// 'sb'
```







## JavaScript Objects

### JS  equal assignment vs shadow copy vs JS deep copy

#### '=': equal assignment
#### shadow copy
#### deep copy

## JavaScript Functions

JavaScript functions are **defined** with the `function` keyword.

### Function Declarations

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

A JavaScript `function` does not perform any checking on  parameter values (arguments).



#### Function Parameters and Arguments

```javascript
function functionName(parameter1, parameter2, parameter3) {
  // code to be executed
}
```

Function **parameters** are the **names** listed in  the function definition.

Function **arguments** are the real **values**  passed to (and received by) the function.



#### Parameter Rules

JavaScript function definitions do **not** specify **data types** for  parameters.

JavaScript functions do **not** perform type **checking** on the passed  arguments.

JavaScript functions do **not** check the **number of arguments** received.



#### Parameter Defaults

If a function is called with **missing arguments** (less than declared), the missing values are set to: **undefined**.

[ECMAScript 2015](https://www.w3schools.com/js/js_es6.asp) allows default parameter values in the function declaration.

```javascript
function (a=1, b=1) {
  // function code
}
```



#### The Arguments Object

JavaScript functions have a built-in object called the **arguments** object.

The argument object contains an array of the arguments used when the function  was called (invoked).

```javascript
x = findMax(1, 123, 500, 115, 44, 88);

function findMax() {
  var i;
  var max = -Infinity;
  for (i = 0; i < arguments.length; i++) {
    if (arguments[i] > max) {
      max = arguments[i];
    }
  }
  return max;
}
```

If a function is called with **too many arguments** (more than declared), these arguments can be reached using **the arguments object**.



#### Arguments are Passed by Value

JavaScript arguments are passed by **value**: The function only  gets to know the values, not the argument's locations.

If a function changes an argument's value, it does not change the parameter's  original value.

**Changes to arguments are not visible (reflected) outside the function.**

```javascript
let a = 1

function increment(x) {
    x++
    return x
}

console.log(increment(a)) // 2
console.log(a) // 1

```





#### Objects are Passed by Reference

In JavaScript, object references are values. 

Because of this, objects will behave like they are passed by **reference:**

If a function changes an object property, it changes the original value.

**Changes to object properties are visible (reflected) outside the function.**

```javascript
let obj={
    'a':1
}

function increment_obj(o) {
    obj.a++
    return obj.a
}

console.log(increment_obj(obj)) // 2
console.log(obj.a) // 2
```





### Function Invocation

The code inside a JavaScript `function` will execute when "something" invokes it.



#### Invoking a JavaScript Function

The code inside a function is not executed when the function is **defined**.

The code inside a function is executed when the function is **invoked**.

It is common to use the term "**call a function**" instead of "**invoke  a function**".

It is also common to say "**call upon a function**", "start a function", or  "execute a function".

Here, we will use **invoke**, because a  JavaScript function can be **invoked without being called**.



#### Invoking a Function as a Function

```javascript
function myFunction(a, b) {
  return a * b;
}
myFunction(10, 2); 
```

The function above does not belong to any object.  But in JavaScript there  is always a default global object.

In HTML the default global object is the HTML page itself, so the function above "belongs" to the  HTML page.

In a browser the page object is the browser window. The function above  automatically becomes a window function.

myFunction() and window.myFunction() is the same function:

```javascript
 function myFunction(a, b) {
  return a * b;
}
window.myFunction(10, 2);    // Will also return 20 
```

This is a common way to invoke a JavaScript function, but not a very good practice.
 Global variables, methods, or functions can easily create name conflicts and bugs in the global object.



#### The ***this*** Keyword

In JavaScript, the thing called `this`, is the object that  "owns" the current code.



#### Invoking a Function as a Method

In JavaScript you can define functions as **object methods**.

```javascript
 var myObject = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  }
}
myObject.fullName();         // Will return "John Doe" 
```

The **fullName** method is a function. The function belongs to  the object. **myObject** is the owner of the function.

The thing called `this`, is the object that  "owns" the JavaScript code. In this case the value of `this`  is **myObject**. 



#### Invoking a Function with a Function Constructor

If a function invocation is preceded with the `new` keyword,  it is a **constructor invocation**.

```javascript
// This is a function constructor:
function myFunction(arg1, arg2) {
  this.firstName = arg1;
  this.lastName  = arg2;
}

// This creates a new object
var x = new myFunction("John", "Doe");
x.firstName;                             // Will return "John" 
```

The `this` keyword in the constructor does not have a value.

The value of `this` will be the new object created when the function is invoked.





### Function Call





### Function Apply





#### Function Closures





## JavaScript HTML DOM





## JavaScript Browser BOM


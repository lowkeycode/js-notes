# Javascript

---

# JAVASCRIPT FUNDAMENTALS - PART 1

---

What is Javascript?

- A high-level, object-oriented, multi-paradigm programming language.

High Level

- It abstracts a lot of the smaller and complex details away from us.
  Ex.) We don't have to worry about things like memory management

Object-Oriented

- Based on objects for storing most kinds of data

Multi-paradigm

- We can use many different programming styles if we want to structure our code
  Ex.) Imperative or Declarative Programming

What is Javascript used for?

The 3 core technologies of the web are HTML, CSS and JS

HTML is responsible for the content of the page

CSS is responsible for the presentation of that content

JS is responsible for the dynamic and interactive effects on the web, manipulating CSS, load data from remote servers and build entire applications in the browser that are called web applications.

There are Javascript libraries that are tools that make writing large scale web apps faster and easier. These libraries are all based on Javascript(JS), so learning JS fundamentals is essential as these libraries/technologies change/become outdated and with a core understanding one will never fall behind.

JS can also run outside web browsers
Ex.) Back-end web servers
...with technologies like node.js. This allows us to create back-end applications that run a web server and can interact with things like databases.

When we use JS in the browser the apps we create are called front-end applications.

JS can also be used to build applications for mobile and even desktop.

Almost any type of applications can be built using JS.

---

There are also JS releases/versions.

An extremely large update was release in ECMASCript 2015 also called ES6. Now releases are done every year as to not overwhelm with many new features all at once. Everything from ES6 and on is called modern JS.

# Data Types

There are 2 types:

1. Objects
2. Primitives

Primitives have 7 kinds:

1. Number
2. String
3. Boolean
4. Undefined
5. Null
6. Symbol
7. Big Int

---

1. Number

- so-called floating point numbers (always have a decimal even if we can't see them or define them)

```js
23 = 23.0;
```

In other programming languages there will be different data types for integers and decimals but in JS they are the same. All numbers are of the type Number.

2. String

- a sequence of characters wrapped in quotes used for text

3. Boolean

- Logical type that can only be true or false (used for making decisions)

4. Undefined

- Value taken by a variable that is not yet defined but already declared. We have not assigned a value to it. (empty value)

5. Null

- Also means empty value

6. Symbols

- Value that is unique and cannot be changed

7. Big Int

- Another type for numbers, specifically built for very large integers that are too big for the number type to hold

Javascript has dynamic typing:

We do not have to manually define the type of data being stored in a variable, they are determined automatically for us.

In other languages you have to define the data type.

Values only have types not variables.

- Note on Null

```js
console.log(typeof null); // object
```

This is actually a bug in JS and will not be corrected because of legacy reasons(It will break the JS language to change)

# Variable Declaration

let... is used for variables that will be reassigned to another value later (mutated)

```js
let age = 30;
age = 31;
```

const... is used to assign values to variables that will not change (immutable)

```js
const birthYear = 1991;
```

You cannot declare empty const variables.

Best practice is to use const by default and only let when you are sure the variable needs to change in the future. Changing variables increases the chance of introducing bugs.

var... is outdated and should not be used but is important to know how it works.

```js
var job = "programmer"; // programmer
job = "teacher"; // teacher
```

Variables do not need to be declared. But this should never been done because it doesn't create a variable in the current scope but rather creates a property on the global object.

```js
lastName = "Remesz";
console.log(lastName); // Remesz
```

Always properly declare variables.

# Operators

An operator allows us to transform value or combine multiple values and work with different data.

There are many different types.

Mathematic Operators (Follow BEDMAS)

```js
+ // Addition
- // Subtraction
* // Multiplication
/ // Division
% // Modulus (Division Remainder)
++ // Increment
-- // Decrement
```

Assignment Operators

```js
= // Assignment operator
+= // x = x + y
-= // x = x - y
*= // x = x * y
/= // x = x / y
%= // x = x % y
**= // x = x ** y Exponent
```

Comparison Operators

```js
== // equal to (has type coercion)
=== // equal value and equal type
!= // not equal (has type coercion)
!== // not equal value or not equal type
> // Greater than
< // Less than
>= // Greater than or equal to
< // Less than or equal to
? // Ternary operator used for boolean comparison
```

Logical Operators

```js
&& // logical and
|| // logical or
! // logical not
```

Type Operators

```js
typeof // Returns type of variable
instanceof // Returns true/false if object is an instance of an object type
```

# Operator Precedence

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence


# Type Conversion & Coercion

Conversion 
- when we manually explicitly convert from one type to another.

Coercion 
- when JS automatically does it implicitly behind the scenes for us.

NaN means invalid number and is returned when a failed conversion to a number happens

Conversion can only happen between 3 types.

1. Strings
2. Numbers
3. Booleans

# Boolean Logic

Using true and false values to solve complex problems.

&& And
|| Or
! Not


# Switch Statement

```js
const day = 'monday';

switch(day) {
  case 'monday':
    console.log('Its monday');
    break;
  case 'tuesday':
    console.log('Its tuesday');
    break;
  case 'wedday':
    console.log('Its wedday');
    break;
  case 'thursday':
    console.log('Its thursday');
    break;
  case 'friday':
    console.log('Its friday');
    break;
  case 'saturday':
    console.log('Its saturday');
    break;
  case 'sunday':
    console.log('Its sunday');
    break;
  default:
    console.log('Not a valid day');
}
```

# Statements & Expressions

An expression is a piece of code that produces a value.(word in sentence)

A statement/declaration is a larger piece of code that is executed and does not produce a value on its own.(A full sentence)

# Ternary Operator

We can use ternary operators in template literals because they are expression and produce a value and is the only way we can use conditionals within template literals.

```js
const age = 21;
console.log(`I like to drink ${age >=18 ? 'Wine' : 'Water'}`);
```


# JS Versions/Releases

History

1995 

- Brendan Eich is hired by Netscape to create a programming language in just 10 days called Mocha which is the beginning of JS

1996

- Mocha renamed to Livescript, then to Javascript in order to attract Java developers (Java was hot at the time), but really the renaming just became a source of confusion.

- Microsoft launches internet explorer, copying JS from Netscape and called it JScript

(Now there are 2 very similar and competing languages)

1997

- A need to standardize the language is quickly realized and the language was submitted to an independent standards organization called ECMA and releases ECMAScript 1 (ES1). ECMAScript now being the standard and JavaScript being the language.

2009

- ES5 released with a lot of new features

2015

- ES6/ES2015 the biggest release to the language ever & annual releases made the standard rather than large updates

All new releases are backwards compatible to support the principle of not breaking the web.

---

# Strict Mode

```js
'use strict'
```

Put this as the VERY FIRST THING in your script

This secures our code by forbidding us to do different things and also creates visible errors when we introduce bugs. Otherwise JS will just fail silently.

```js
let hasDriversLicense = false;
const passTest = true;

if(passTest) hasDriverLicense = true;
if (hasDriversLicense) console.log('I can drive');
```

Above the first conditional should set the let variable to true but because it is missing the "s" does not reassign and in turn does not log to the console and does not throw an error. JS fails silently.

With use strict it throws an error for us in the console allowing us to catch the bug sooner.

Not necessarily used for production.

# Functions

When you return a piece of data from a function when defining it, when you call it you can then store that return value of calling the function in a variable to use anywhere else later.

# Function Declaration vs Function Expression

Function declaration are written with the function keyword

```js
function calcAgeDeclaration(birthYear, currentYear) {
  return currentYear - birthYear;
}
```


Function expressions are anonymous functions stored in a variable

```js
const calAgeExpression = function(birthYear, currentYear) {
  return currentYear - birthYear;
}
```

Functions are just values.

The main difference between declarations and expressions is that we can call declarations before they are defined in the code. Not with expressions. This happens because of hoisting.


```js
const age = calcAgeDeclaration(1991, 2020);


function calcAgeDeclaration(birthYear, currentYear) {
  return currentYear - birthYear;
}
```

A benefit to expressions would be that you HAVE to define the function before you can call it which adds structure to code. But both have their place so its important to know how to use both and their use cases.


# Arrow Functions

```js
const calcAgeArrow = birthYear => 2037 - birthYear;
```

All values have implicit returns with one liners.

Multi-param functions need to use the parentheses

Multi-line arrow functions need the explicit return;

```js
const calcAgeArrow = (birthYear, current Year) => {
  currentYear - birthYear;
}
```

```js
const yearsUntilRetirement = birthYear => {
  const age = 2037 - birthYear;
  const retirement = 65 - age;
  return retirement;
}
```

Arrow functions do not get a this keyword.


# Functions Calling Other Functions

```js
function cutFruitInto4Pieces(fruit) {
  return fruit * 4
}


function foodProcessor(apples, oranges) {
  const applePieces = cutFruitInto4Pieces(apples);
  const orangePieces = cutFruitInto4Pieces(oranges);

  const juice = `Juice with ${applePieces} apple pieces and ${orangePieces} orange pieces.`;
  return juice;
}
```

---
# Dev Skills & Editor Setup
---

# Problem Solving

1. Ask all the right questions to get a clear picture of the problems

2. Divide and conquer and break big problems into smaller sub-problems

3. Research if needed

4. Write pseudo code to plan


---
# DOM Manipulation & Event Fundamentals
---

The DOM !== JavaScript

The DOM methods and properties for DOM manipulation are part of the web APIs that JS interacts with.

---
# JS Behind The Scenes
---


JS is a high-level, prototype-based object-oriented, multi-paradigm, interpreted or just-in-time compiled, dynamic, single-threaded, garbage-collected programming language with first-class functions and a non-blocking event loop concurrency model.

1. High-level 

- Has abstractions that allow us not to worry about details like memory management that is dealt with in low level languages like C but means programs will never be as optimized as in those languages because those things happen automatically

2. Garbage-collected

- An algorithm in the JS engine that automatically removes unused object from computer memory

3. Interpreted/Just-in-time compiled

- The computers processor only understands binary and when translated by the JS engine to binary JS we write is then interpreted/just-in-time compiled

4. Multi-paradigm

- JS has multiple approaches/mindsets to structuring code. Ex.) Procedural, Object oriented, Functional programming, Imperative, Declarative whereas other languages may only use one way

5. Prototype-based/Object-oriented

- Everything in JS is an object except for primitives

- JS has a prototype chain that is inherited from the main blueprint of an object/primitive

6. First-class functions

- functions are treated just like regular variables. They can be passed into other functions and even have a function be returned from another function

7. Dynamic

- Dynamically typed, data type of variables is figured out by JS, the programmer doesn't need to specify the data type whereas other languages need the programmer to specify the type

8. Single-threaded

- One stack, one thing at a time

9. Non-blocking event loop concurrency model

- How JS handles multiple tasks happening at the same time


# The JS Engine & Runtime

Engine - The program that executes JS code 

Engine Components

1. Call stack

- Where code is executed using execution contexts

2. Heap

- Unstructured memory pool that stores all the objects that our app needs


Compilation vs Interpretation

Compilation - Entire code is converted into machine code all at once, and written to a portable binary file that can be executed by a computer at any later time

Interpretation - Interpreter runs through the code and executes line by line

JS used to be interpreted but it causes programs to run slow

Modern JS use a mix between both which is called Just-in-time Compilation

Just-in-time - The entire code is converted into machine code all at once then executed immediately (no portable file)


Code executing through the JS engine:

JS code is first parsed, which means reading the code. During parsing the code is put into a data structure called the AST(Abstract Syntax Tree). This works by first splitting up each line of code into pieces that are meaningful to the language and then saving all the pieces into the tree in a structured way. This step also checks for any syntax errors and the resulting tree will later be used to generate the machine code.

Next the generated AST is compiled into machine code. 

Then the execution happens immediately after compilation. This happens in the call stack.

JS engines create an un-optimized version off the start to be able to start executing ASAP. Then in the background the code is optimized and recompiled in the background during the current execution. This process can happen multiple times and on each iteration the more optimized code is swapped out for the old code, never stopping or interrupting the execution.

Javascript Runtime:

A container that includes all the things we need to use JS. (In this example the browser)

All run times contain:
- An engine
Contains the heap and callstack

- Web APIs(DOM, Timers, Fetch APU etc.)
JS gets access to these through the global window object.

- Callback queue
Ex.) Callback functions from event listeners

- Event loop
Watches the callback queue & call stack to run callback functions when the stack is empty

Node JS is also a JS runtime. (Instead of web APIs it has C++ bindings and a thread pool)

# How Is JS Code Executed

Once code is compiled and ready for execution, first:

A global execution context is created for top-level code (code that is not inside any function) This includes variables. Functions are defined but the function body only executed when called later.

Execution context is an abstract concept.

- An environment in which a piece of JS is executed. Stores all the necessary info for some code to be executed

Top level code is then executed in the global execution context.

Then a single execution context is created for each and every function and these make up the call stack.

When done the engine will wait for callback functions to arrive to execute those.

Execution context in detail:

1. Variable Environment
- let const and var declarations
- Functions
- Arguments object (function arguments)

2. Scope chain

3. The this keyword

These 3 things are generated during a "creation phase", right before execution

Execution contexts belonging to arrow functions do not get an arguments object in the variable environment. As well they do not get a this keyword. Instead they can use these 2 things from their closest regular function parent.

These execution contexts are managed by the call stack to keep them in order and keep track of where in the program we are.

# Scope & The Scope Chain

Scoping controls how our programs variables are organized and accessed. It defines where we can and cannot access variables.

JS is lexically scoped meaning that scope is controlled by the placement of functions and blocks in the code.

Scope is the space or environment in which a certain variable is declared(variable environment in the case of functions) There is a global scope, function scope and block scope.

Scope of a variable is the region of our code where a certain variable can be accessed.

3 types of scope:

1. Global
2. Functions
3. Block Scope (ES6)

1. Global

- Outside any function or block
- Variables declared in the global scope are accessible everywhere

2. Functions

- Variables are accessibly only inside a function NOT outside
- Also called local scope

3. Block Scope (ES6)

- Everything inside curly braces Ex.) if block, for loop block
- Variables are accessible only inside the block (block scoped)
- HOWEVER this only applies to let and const variables
- Variables using var would be accessible outside the block to the current function or global scope (function scoped)
- This is why we say let and const are block scoped
- Functions are also block scoped (only in strict mode)

Variables are not copied from scope to scope but when a function needs a variable will try to look up in the scope chain to each of its parents until the global scope

Parents cannot look down the scope chain.

# Hoisting

An execution always contains 3 parts:

1. Variable environment
2. Scope chain
3. this keyword

We need to take a closer look at the variable environment.

Hoisting:

- Makes some types of variables accessible/usable in the code before they are actually declared.

Before execution, code is scanned for variable declarations, and for each variable, a new property is created in the variable environment object.

How hoisting works for different functions & variable types:


1. Function Declarations

- Hoisted? = YES
- Initial Value = Actual function
- Scope = Block(In strict mode)



2. Var Variables

- Hoisted? = YES
- Initial Value = undefined
- Scope = Function

3. let And const Variables

- Hoisted = NO
- Initial Value = uninitialized/TDZ(temporal dead zone)
- Scope = Block

4. Function Expressions

- All depends if you are using var, let or const and behaves accordingly

TDZ (Temporal Dead Zone), let and const

TDZ for job:

```js
const myName = ''Jonas;

if (myName === 'Jonas') {
  // ⤋⤋⤋ Temporal Dead Zone ⤋⤋⤋
  console.log(`Jonas is a ${job}`);
  const age = 2037 - 1989;
  console.log(age);
  // ⤊⤊⤊ Temporal Dead Zone ⤊⤊⤊
  const job = 'teacher';
  console.log(x);
}
```
The job variables is scoped to the if block and is accessible from the line it is defined but since we are trying to access it in the template literal it gives us a " ReferenceError: cannot access 'job before initialization' ".
The variable is only safe to use after the temporal dead zone.

Whereas x will give us " ReferenceError: x is not defined " 

Why TDZ?:

The behavior makes it way easier to avoid and catch errors and bugs.

Makes const variables actually work.


Why Hoisting?

So we can use function declarations before we actually define them. This is used in certain techniques like mutual recursion.

People think it makes code more readable.

var hoisting is just a by product and was the only way JS could work and now it cannot be removed because of legacy reasons.

We now use let and const to get around variables be hoisted as undefined.

# Hoisting In Practice


Variables

```js
console.log(me); // undefined (Hoisted to undefined)
console.log(job); // ReferenceError: Cannot access 'job' before initialization
console.log(year); // ReferenceError: Cannot access 'job' before initialization


var me = 'Jonas';
let job = 'teacher';
const year = 1991;
```

Functions


```js
console.log(addDeclaration(2,3));
// 5

console.log(addExpressionConst(2,3));
// Cannot access 'addExpression' before initialization

console.log(addArrowConst(2,3));
// Cannot access 'addArrow' before initialization

console.log(addExpressionVar(2,3));
// Uncaught TypeError: addExpressionVar is not a function

console.log(addArrowVar(2,3));
// Uncaught TypeError: addExpressionVar is not a function


function addDeclaration(a,b) {
  return a + b;
}

const addExpressionConst(a,b) {
  return a + b;
}

const addArrowConst(a,b) => a + b;

var addExpressionVar(a,b) {
  return a + b;
}

var addArrowVar(a,b) => a + b;
```

With the var expression and arrow functions they are hoisted and set to undefined. Then we are trying to call them as a function and they are undefined...

```js
undefined(2,3);
// Uncaught TypeError: undefined is not a function
```

A common pitfall:

```js
if(!numProducts) deleteShoppingCart();

var numProducts = 10;

function deleteShoppingCart() {
  console.log('All products deleted!');
}
```

Because the var numProducts is hoisted and set to undefined the if statement reads the undefined which holds a falsey value, making the conditional match and running the deleteShoppingCart function even though there are still 10 items in the shopping cart.

In a large code base could become a very hard to find bug.

## Best Practices

1. DONT USE var
2. Use const as a default 
3. Us let when a value needs to change
4. Declare variables at the top of each scope
5. Always declare any type of function first and use them after declaration



```js
var x = 1;
let y = 2;
const z = 3;

console.log(window);
// Here var creates an "x" variable on the window object but let and const do not get

// This could pollute the window object especially in a large app
```

# this Keyword

How it works:

A special variable that is created for every execution context. Takes the value of(points to) the owner of the function in which the this keyword is used.

The this keyword is NOT static. It depends on how the function is called, and its value is only assigned when the function is actually called.

Ways of calling a function:

1. Method
- this = the object calling the method

2. Simple function called
- this = undefined (strict mode) else it points to the global window object

3. Arrow function
- this = the this of the surrounding function (lexical this)

4. Event Listener
- this = the DOM element that the handler is attached to (usually left of the . notation)

* the this keyword does NOT point to the function itself, and also NOT the variable environment of the function

# Regular Functions vs Arrow Functions

```js
const jonas = {
  firstName: 'Jonas',
  year: 1991,
  calcAge: function() {
    console.log(this);
    console.log(2037 - this.year);

  // Function inside a function
    const isMillenial () => {
      console.log(this.year >= 1981 && this.year <= 1996)
    }
  },

  greet: () => console.log(`Hey ${this.firstName}`),
};

jonas.greet(); // Hey undefined

// Arrow function do not get a this keyword but rather its parents, and the parent is the global scope

// Keep in mind object literals like above do not contain their own scope (Objects are NOT code blocks)
console.log(this.firstName)
 // This is the window object and there is no firstName so it is undefined

 // Imagine using var to define a variable called firstName which holds 'Matilda' which will create a property on the global window object so when we log this.firstName we get 'Hey Matilda' which is not at all what we are trying to accomplish
```

If you never use an arrow function as a method as well it will prevent this because even without the var firstName we get the undefined.

A function inside a method on an object would return undefined (strict mode) or the window object in sloppy mode this is because it is a regular function call.

A hack around this is in the method make a variable called self and point it to the this key word, then use the self variable in your function inside the method. This was used pre ES6.

In ES6 the solution is to use an arrow function as it is assigned the this keyword of its parents scope.


Arguments keyword:

Functions also get access to an arguments keyword and is only available in regular function


```js
const addExpressionConst = (a,b) => {
  console.log(arguments);
  return a + b;
}
addExpressionConst(2, 5);
// We can actually add more arguments to a function if we need and they are stored in the arguments array
addExpressionConst(2, 5, 8, 12);

// arguments = Arguments[
//   0: 2
//   1: 5
//   2: 8
//   3: 12
// ]




var addArrowVar = (a,b) => a + b;
```

Arrow functions do not get this keyword. This keyword is not used very much in modern JS.

# Primitives vs Objects (Primitive vs Reference Types)


```js
let age = 30;
let oldAge = age;
age = 31;
console.log(age); // 31
console.log(oldAge); // 30

const me = {
  name: 'Jonas',
  age: 30,
};

const friend = me;
friend.age = 27;
console.log(friend); // friend.age = 27
console.log(me); // me.age = 27
```

Primitive Types

1. Numbers
2. Strings
3. Boolean
4. Undefined
5. Null
6. Symbol
7. BigInt

Everything else is an object.

Objects = Reference Types


Primitives and References are stored differently in memory.

The JS Engine has 2 components. The call stack & heap.

All reference types get stored in the memory heap. 

Primitives are stored in the call stack (in the execution context in which they are declared)


```js
let age = 30;
```

When primitives are stored in the call stack they are assigned 
- An identifier (variable name)
- An address 
- Their value (whatever we declared in the code)

The identifier points to the address in memory and not the value its self

Ex.)  age → address(001)

age = memory address which holds the value of 30

```js
oldAge = age;
```

Ex.) oldAge → address(001)

Now both variable are pointing to the same address in memory

```js
age = 31
```

Ex.)  age → address(002)

The value at a certain memory address is immutable and cannot be changed.

A new piece of memory is now allocated for 31 and the age variable is now pointing to the new address.


Reference Types:

When a new object is created it is stored in the heap and there is a memory address and the value itself.

Ex.) address(D30F) 
value {name:'Jonas',age: 30,}

```js
const me = {
  name: 'Jonas',
  age: 30,
};
```

The me identifier DOES NOT point directly to the new memory address in the heap.

Instead it points to a new piece of memory that is created in the stack with a new address and the value at that address is the address in the Heap

Ex.) me(identifier) → address(003)
value(D30F) → address(D30F)
value {name:'Jonas',age: 30,}

The piece of memory in the call stack has a REFERENCE to the piece of memory in the heap which hold the me object

It works this way because objects could be too large to keep in memory in the stack.


```js
const friend = me;
```

Ex.) friend(identifier) → address(003)
value(D30F) → address(D30F)
value {name:'Jonas',age: 30,}

```js
friend.age = 27;
```

friend(identifier) → address(003)
value(D30F) → address(D30F)
value {name:'Jonas',age: 27,}

Even as a constant we can manipulate the object without problem because we aren't actually changing the value in memory for the friend identifier because it is still D30F.

When you think you are copying an object you are really just creating a variable that points to the exact same object. There are ways around this that we'll visit later on.


Prototypal Inheritance, The Event Loop & Advanced DOM will also be visited later.


---
# Data Structures, Modern Operators & Strings
---

# Destructuring Arrays


```js
const restaurant = {
  name: 'Classico Italiano',
  location: 'Via Angelo Tavanti 23, Firenze, Italy',
  categories: ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'],
  starterMenu: ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad'],
  mainMenu: ['Pizza', 'Pasta', 'Risotto'],

  order: function(starterIndex, mainIndex) {
    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
  },


},


const arr = [2,3,4];
const a = arr[0];
const b = arr[1];
const c = arr[2];

// For destructuring arrays we use square brackets

const [x, y, z] = arr;
console.log(x, y ,z); // 2, 3 ,4
// Destructuring does not affect the original array.

const [first, second] = restaurant.categories;
console.log(first, second); // Italian Pizzaria


// We can skip values we do not want to use by leaving its place blank
const [first, , second] = restaurant.categories;
console.log(first, second) // Italian Vegetarian
```



Without destructuring if we wanted to swap the main and secondary values we would need to create a temp value to pass around the variables so we didn't lose them in memory when reassigning.

```js
let [main, secondary] = restaurant.categories;

const temp = main;
main = secondary;
secondary = temp;
console.log(main, secondary); // Vegetarian Italian
```



With destructuring:

```js
[main, secondary] = [secondary, main];
console.log(main, secondary); // Vegetarian Italian
```



Receiving 2 return values from a function:

```js
// Method on object
  order: function(starterIndex, mainIndex) {
    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];

restaurant.order(2, 0); // Garlic Bread, Pizza

const [starter, main] = restaurant.order(2, 0); 
console.log(starter, main); // Garlic Bread, Pizza
```



Nested arrays:

```js
const nested = [2, 4, [5, 6]];

const [i, ,j] = nested;
console.log(i, j); // 2 [5,6]
```



Returning all values (Destructuring inside of destructuring):

```js
const nested = [2, 4, [5, 6]];

const [i, ,[j, k]] = nested;
console.log(i, j, k) // 2 5 6
```



We can also set default values for the variables when we are extracting them which is useful when we don't know the length of an array.


Default values(Not knowing the length of the array)

```js
const [p, q, r] = [8, 9];
console.log(p, q, r); // 8 9 undefined
```


Set the default values;

```js
const [p = 1, q = 1, r = 1] = [8, 9];
console.log(p, q, r); // 8 9 1
```


# Destructuring Objects

```js
const restaurant = {
  name: 'Classico Italiano',
  location: 'Via Angelo Tavanti 23, Firenze, Italy',
  categories: ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'],
  starterMenu: ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad'],
  mainMenu: ['Pizza', 'Pasta', 'Risotto'],
  openingHours: {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  },
  order: function(starterIndex, mainIndex) {
    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
  },
},
```

For destructing objects we use curly braces and we have to use variables that exactly match the property name on the object. The order of an object is not defined so we can just use the variable names in the order we want them for our new destructured object.

```js
const {name, openingHours, categories} = restaurant;
console.log(name, openingHours, categories);
    // Classico Italiano
    // thu: {
    //   open: 12,
    //   close: 22,
    // },
    // fri: {
    //   open: 11,
    //   close: 23,
    // },
    // sat: {
    //   open: 0, 
    //   close: 24,
    // },
    // ['Italian', 'Pizzeria', 'Vegetarian', 'Organic']
```   




Variable names different from property names(Useful for dealing with 3rd party data that we need to rename):

```js
const {name: restaurantName, openingHours: hours, categories: tags} = restaurant;
console.log(restaurantName, hours, tags);
    // Classico Italiano
    // thu: {
    //   open: 12,
    //   close: 22,
    // },
    // fri: {
    //   open: 11,
    //   close: 23,
    // },
    // sat: {
    //   open: 0, 
    //   close: 24,
    // },
    // ['Italian', 'Pizzeria', 'Vegetarian', 'Organic']
```


Setting default values for properties that do not exist(or we are not sure exist) on the object. Here we set just an empty array as a default for menu as that property does not exist on the object. Without it it will just return undefined

```js
const {menu = [], starterMenu: starters = []} = restaurant;
console.log(menu, starters);
// []
// ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad']
```



Mutating variables while destructuring objects:

```js
let a = 111;
let b = 999;
const obj = {a: 23, b: 7, c: 14};

{a, b} = obj; // Uncaught SyntaxError: Unexpected token '='
```
We want a to become 23 and b to become 7.

We cannot use const because a & b are already declared. We cannot just use let because it would declare new variables and they are already declared. We cannot just omit the variable type declaration because JS expects a code block and we cannot assign anything to a code block so we get an error. The trick is to wrap it in parentheses.

```js
({a, b} = obj);
console.log(a, b) // 23 7
```



Nested Objects:

```js
const restaurant = {
  openingHours: {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0,
      close: 24,
    },
}

const { openingHours } = restaurant;

const {fri} = openingHours;
console.log(fri);
// fri: {
//       open: 11,
//       close: 23,
//     },
```

Destructuring further:

```js
const {fri: {open, close}} = openingHours;
console.log(open, close);
// 11 23
```
We can also rename any variable at any level with the colons:

```js
const {fri: {open: o, close: c}} = openingHours;
```



Destructuring parameters in functions:

Often times there will be functions with a lot of parameters and it can be hard to know the order of the parameters for the person using the function, so instead of defining the parameters manually we can pass the function an object and it will automatically destructure for us


```js
orderDelivery: function({starterIndex = 1, mainIndex = 0, time = '20:00', address}) {
  console.log(`Order received! ${this.starterMenu[starterIndex]} and ${this.mainMenu[mainIndex]} will be delivered to ${address} at ${time}`);
}


restaurant.orderDelivery({
  time: '22:30',
  address: 'Via del Sole, 21',
  mainIndex: 2,
  starterIndex: 2,
});

restaurant.orderDelivery({
  address: 'Via del Sole, 21',
  starterIndex: 1,
});
```

# Spread Operator (...)

Used on the right hand side of the assignment operator ( = ...)

```js
const arr = [7, 8, 9];

const badArr = [1, 2, arr[0], arr[1], arr[2]]; 
console.log(badArr); // [1, 2, 7 , 8, 9]

const newArr = [1, 2, ...arr];
console.log(newArr); // [1, 2, 7 , 8, 9]
```



Passing arguments into functions to get each item individually:

```js
console.log(...newArr) // 1, 2, 7, 8, 9
```

More practical example:

```js
const newMenu = [...restaurant.mainMenu, 'Gnocci'];
console.log(newMenu);
// ['Pizza', 'Pasta', 'Risotto', 'Gnocci'],
```
Again the above creates a brand new array and is not mutating the original

The spread operator takes ALL the elements from an array and also doesn't create new variables.

Can only use it where we have values separated by commas.




2 important use cases:

1. Create shallow copy of an array
2. Merge 2 arrays together


Shallow Copy: 

```js
const mainMenuCopy = [...restaurant.mainMenu];
```

Joining 2 Arrays: 

```js
const menu = [...starterMenu, ...mainMenu];
```



The spread operator works on all iterables(arrays, strings, maps and sets but not objects).

```js
const str = 'Jonas';
const letters = [...str, ' ', 'S.'];
console.log(letters); // ["J", "o", "n", "a", "s", " ", "S."]
```



The spread operator cannot be used within template literals because it does not expect values separated by commas.

```js
console.log(`${...str} Schmedtmann`);
// Uncaught SyntaxError: Unexpected Token '...'
```



Function with spread operator:

(Create a function that only order pasta and the pasta always needs to have exactly 3 ingredients, which we get from a prompt window)

```js
orderPasta: function(ing1, ing2, ing3) {
  console.log(`Here is your delicious pasta with ${ing1}, ${ing2} and ${ing3}`)
}

const ingredients = [prompt('Let\'s make pasta! Ingredient 1?'),
prompt('Ingredient 2?'),
prompt('Ingredient 3?')
];

restaurant.orderPasta(...ingredients);
```



Spread operator with objects:

```js
const newRestaurant = {foundingYear: 1998 , ...restaurant, founder: 'Guiseppe'};
console.log(newRestaurant);
```



Shallow copy with objects:

```js
const restaurantCopy = {...restaurant};
restaurantCopy.name = 'Ristorante Roma';

console.log(restaurantCopy.name); 
// Ristorante Roma
console.log(restaurant.name); 
// Classico Italiano
```



# Rest Pattern & Parameters

The rest pattern has the exact same syntax as the spread operator but does the opposite.

Used on the left hand side of the spread operator ( ... =)

It collects the unused items in the destructuring assignment into one array


```js
const [a, b, ...others] = [1, 2, 3, 4, 5];

console.log(a, b, others);
// 1 2 [3, 4, 5];
```



We can use both spread and rest operator at the same time:

```js
const [pizza, , risotto, ...otherFood] = [...restaurant.mainMenu, ...restaurant.starterMenu];

console.log(pizza, risotto, otherFood)
// Pizza Risotto
// ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad']
```

The rest needs to be the last element and there can be only one in the destructuring assignment or it will not work.



Rest operator with objects:

```js
const { sat, ...weekdays } = restaurant.openingHours;
console.log(weekdays);

//     thu: {
//       open: 12,
//       close: 22,
//     },
//     fri: {
//       open: 11,
//       close: 23,
//     },
```



Rest operator (Rest Arguments) with functions:

It is called rest and not spread here because it is collecting all the individual numbers into one array.

We want our add function to accept any amount of arguments
```js
const add = function(...numbers) {
  let sum = 0;
  for(let i = 0; i < numbers.length; i++) sum += numbers[i];
  console.log(sum);
}
add(2, 3);
add(5, 3, 7, 2);
add(8, 2, 5, 3, 2, 1, 4);
```

Another way:
```js
const x = [23. 5. 7]
add(...x);
```


Examples:

```js
orderPizza: function(mainIngredient, ...otherIngredients) {
  console.log(mainIngredient);
  console.log(otherIngredient);
}

restaurant.orderPizza('mushrooms', 'onion', 'olives', 'spinach');
// mushrooms
//['onion', 'olives', 'spinach']

restaurant.orderPizza('mushrooms');
// mushrooms
// []
```



Recap:


The spread and rest syntax look the exact same but behave in opposite ways depending on where they are used. 

The spread operator is used where we would write values separated by commas. 

The rest operator is used where we would write variable names separated by commas.



# Short Circuiting && and ||

|| operator:

If the first value is truthy it will short circuit and return that value.

The result of the or operator doesn't always have to be a boolean

Logical operators:

1. Can use any data type
2. Return any data types
3. Ability to short circuit

```js
console.log(3 || 'Jonas');
// 3

console.log('' || 'Jonas');
// Jonas
// First value is falsey and second is truthy

console.log(true || 0);
// true

console.log(undefined || null);
// null
// undefined is falsey and returns null even though it is falsey


console.log(undefined || 0 || '' || 'Hello' || 23 || null);
// Hello
```

Short-circuiting:

If the first operand is truthy it will immediately return that value and not evaluate the second operand at all


Property not on an object:

```js
const guests1 = restaurant.numGuests ? restaurant.numGuests : 10;
console.log(guests1); // 10
```

Property is on object:

```js
restaurant.numGuests = 23;
const guests1 = restaurant.numGuests ? restaurant.numGuests : 10;
console.log(guests1); // 23
```

Short-circuiting:

```js
const guests2 = restaurant.numGuests || 10;
```

This allows us to not use if else or ternary.



&& Operator:

Works in the exact opposite way as the  || operator

If the first value is falsey it will short circuit and return that value.

```js
console.log(0 && 'Jonas')
// 0
console.log(7 && 'Jonas')
// Jonas
```


Practical example:

Checking to see if orderPizza exists.

```js
if (restaurant.orderPizza) {
  restaurant.orderPizza('mushrooms', 'spinach');
}
```

```js
restaurant.orderPizza && restaurant.orderPizza('mushrooms', 'spinach')
```

# Nullish Coalescing Operator

When we set the value to 0 which we want but since the short circuit sees 0 as falsey it moves onto the next value which is 10 and sets guests to 10 when it should be 0.

```js
restaurant.numGuests = 0;
const guests = restaurant.numGuests || 10;
console.log(guests);
// 10
```

So we use the nullish coalescing operator:

```js
restaurant.numGuests = 0;
const guests = restaurant.numGuests || 10;

const guestsCorrect = restaurant. numGuests ?? 10;
console.log(guestsCorrect);
// 0
```

This works because this operator works with the concept of nullish values instead of falsey values.

Nullish values are null & undefined. (NOT 0 or the '' empty string)



 # For Of Loop (ES6)

 ```js
const menu = [...restaurant.starterMenu, restaurant.mainMenu];

for (const item of menu) console.log(item);
 ```
 The for of loop removes the need to set up a counter, a condition and operator that you need to do in the for loop.

 In the for of we specify a variable name for each element that will be iterated over in the array and the array of which we will iterate over. Then it automatically loops through the array for us.

 We can also use the continue and break statements with this loop whereas other ways Ex.) forEach() you cannot break.

 The for of is hard to get the index as it is a pain. It was designed just to get the current element in that iteration of the array.

 Loops must contain an iterable. Keep in mind non-iterables like objects will need to be converted before iterating over.

 ```js
for (const [i, element] of menu.entries()) {
  console.log(item);

  console.log(`${i + 1}: ${el}`)
}

console.log(menu.entries()); // Array Iterator - returns an array or arrays
 ```

 We can also use destructuring in loops.


# Enhanced Object Literals

ES6 introduced 3 new ways to write object literals

1. When referencing an object outside and object, you don't need to set the key & value pair to the same name, you just have to state it once

```js

const openingHours = {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  };

const restaurant = {
  name: 'Classico Italiano',
  location: 'Via Angelo Tavanti 23, Firenze, Italy',
  categories: ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'],
  starterMenu: ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad'],
  mainMenu: ['Pizza', 'Pasta', 'Risotto'],

  // Instead of this...
  openingHours: openingHours,
  // We can do this...
  openHours,

  order: function(starterIndex, mainIndex) {
    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
  };

```



2. For methods, we no longer need to create a property and set it to a function expression

```js
const restaurant = {
  // Instead of this...
  order: function(starterIndex, mainIndex) {
  // We can do this...
  order(starterIndex, mainIndex) {


    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
  };

}

```

3. We can now compute property names instead of having to write them out manually/literally. Before property names could not be computed.


```js
const weekdays = ['mon', 'tues', 'wed', 'thurs', 'fri', 'sat', 'sun'];

// Instead of this...
const openingHours = {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, 
      close: 24,
    },
  };

// We can do this...
const openingHours = {
    [weekdays[3]]: {
      open: 12,
      close: 22,
    },
    [weekdays[4]]: {
      open: 11,
      close: 23,
    },
    [`day-${2 + 4}`]: {
      open: 0,
      close: 24,
    },
  };
```


# Optional Chaining

We want to get opening hours for the restaurant for monday. But this property doesn't exist. So in the case where we don't know if the object has that property or not (like if we are using a web API)

```js
console.log(restaurant.openingHours.mon); // Undefined
```

And if we go one step further we hit an error

```js
console.log(restaurant.openingHours.mon.open); // Uncaught TypeError: Cannot read property 'open' of undefined
```

So we would have to check with a conditional statement

```js
if(restaurant.openingHours.mon)
console.log(restaurant.openingHours.mon.open);
```

With deeply nest objects this gets out of hand very quickly especially if the object has many optional properties

```js
if(restaurant.openingHours && restaurant.openingHours.mon)
console.log(restaurant.openingHours.mon.open);
```

So with optional chaining

```js
console.log(restaurant.openingHours.mon?.open);

console.log(restaurant.openingHours?.mon?.open);
```

Only if the property before the question mark exists then the next property will be read, if not a nullish check is preformed and if an undefined or null is found then undefined is immediately returned. The ? optional chaining can have multiple ? in the statement.


We can use the nullish coalescing operator with the optional chaining operator to take the returned undefined value and have a default value that catches it.

```js  Real Example
const weekdays = ['mon', 'tues', 'wed', 'thurs', 'fri', 'sat', 'sun'];

for(const day of weekdays) {
  const open = restaurant.openingHours[day]?.open ?? 'closed';
  console.log(`On ${day}, we open at ${ open}`);
}
```

Optional chaining with methods:


```js
// Exists
console.log(restaurant.order?.(0, 1) ?? 'Method does not exist.');

// Does not exist
console.log(restaurant.orderRisotto?.(0, 1) ?? 'Method does not exist.');
```

Optional chaining with arrays:


```js
const users = [{ name: 'Jonas', email: 'hello@jonas.io' }];

console.log(users[0]?.name ?? 'User array empty');
```

# Looping Objects

We can also loop over objects which are not iterables but we need to do it in an indirect way.

We have different options depending on if we want to loop over the object property names(keys), values or both together.



```js  Keys
const properties = Object.keys(openingHours);
console.log(properties);

console.log(`We are open ${properties.length} days of the week`)

let openStr = `We are open on ${properties.length} days:`;

for(const day of Object.keys(openingHours)) {
  openStr += `${day},`;
  console.log(openStr);
  // We are open on 3 days: thu, fri, sat
}
```


```js Values
Object.values(openingHours);
```



```js Key & Values
const entries = Object.entries(openingHours);

for(const [key, {open , close}] of entries) {
  console.log(`On ${key} we open at ${open} and close at ${close}`);
}
```

With Object.entries the object needs to be passed as an argument to the method whereas with arrays it is called on the array itself using the . notation.
Ex. menu.entries(); 



# Sets

Sets are collections of unique values with no duplicate values.

With sets you need to pass in an iterable, the most common being an array. Sets can also hold mixed data types.

```js
const ordersSet = new Set([
  'Pasta',
  'Pizza',
  'Pizza',
  'Risotto',
  'Pasta',
  'Pizza'
  ]);

console.log(ordersSet);
// Set(3) {"Pasta", "Pizza", "Risotto"}

console.log(new Set('Jonas'));
// Set (5) {"J", "o", "n", "a", "s"}

console.log(ordersSet.size);
// 3

console.log(ordersSet.has('Pizza'));
// True
console.log(ordersSet.has('Bread'));
// False

ordersSet.add('Garlic Bread');
ordersSet.add('Garlic Bread');
console.log(ordersSet);
// Set(4) {"Pasta", "Pizza", "Risotto", "Garlic Bread"}

orderSet.delete('Risotto');
console.log(ordersSet);
// Set(3) {"Pasta", "Pizza", "Garlic Bread"}

orderSet.clear();
console.log(orderSet);
// Set(0) {}
```


There are no indexes in sets. There is no need to get values out of the set. All values are unique and their orders do not matter. You only need to know whether or not the set has the value or not. You do this using the .has() method.

If you need to store data in order and retrieve it then an array is the best use case.

Sets are iterables so we can loop over them.

```js
const ordersSet = new Set([
  'Pasta',
  'Pizza',
  'Pizza',
  'Risotto',
  'Pasta',
  'Pizza'
  ]);

for(const order of ordersSet) console.log(order);

```

A large use case: (Removing duplicate values from arrays)


```js
const staff = ['Waiter', 'Chef', 'Waiter', 'Manager', 'Chef', 'Waiter'];

const staffUnique = new Set(staff);
console.log(staffUnique);
// Set(3) {"Waiter", "Chef", "Manager"}
```

We convert back to an array using the spread operator as it works on ALL iterables.

```js
const staffUnique = [...new Set(staff)];
console.log(staffUnique);
// Array(3) ["Waiter", "Chef", "Manager"]
```

You can skip creating an array if you only need to know the amount of unique positions in the set. The same goes with any other iterable.

```js
console.log(new Set(['Waiter', 'Chef', 'Waiter', 'Manager', 'Chef', 'Waiter']).size)
// 3
```

Sets are not intended to replace arrays. Arrays are great for storing values in order that may contain duplicates. They are also great for manipulating data. Set are great for their property of only holding unique values and a few straight forward methods make them easy to work with. They are not nearly as important as array.


# Maps

Maps are used to map values to keys. They are similar to objects but the main difference is that the key in a maps key/value pair can have any type, whereas in objects the keys can only be strings.


```js
const restaurant = new Map();
restaurant.set('name', 'Classico Italiano');
restaurant.set(1, 'Firenze, Italliano');
restaurant.set(2, 'Lisbon, Portugal');

restaurant
  .set('categories', ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'])
  .set('open', 11)
  .set('close', 23)
  .set(true, 'We are open')
  .set(false, 'We are closed');
// You can chain sets


console.log(restaurant.get('name'));
// Classico Italliano

console.log(restaurant.get(true));
// We are open

// When retrieving keys you must use the matching data type

console.log(restaurant.get('true'));
// Undefined
```


```js
const time = 21;
;
console.log(restaurant.get(time > restaurant.get('open') && time < rest.get('close')));
// We are open
```
The above is clever but fairly unreadable so use with caution.


More methods:

```js
console.log(restaurant.has('categories'));
// true

restaurant.delete(2);

console.log(restaurant.size);
// 7

restaurant.clear();
// Map(0)
```
With objects you can use the delete operator but it is really slow and should be avoided.

Arrays/Objects as map keys:

```js
restaurant.set([1, 2], 'Test')

console.log(restaurant);
// key: [1, 2]
// value: "Test"

console.log(restaurant.get([1, 2]));
// undefined
```

This does not work because these are 2 different objects stored in memory so we would need to store the key array in a variable.

```js
const arr = [1, 2];
restaurant.set(arr, 'Test');

console.log(restaurant.get(arr));
// Test
```


Objects as keys in Maps are very useful for storing DOM elements as they are a special type of object.

```js
restaurant.set(document.querySelector('h1'), 'Heading');
```


# Maps - Iterating


Another way to set keys and values is to pass an array of arrays into the Map because using the set() method can become cumbersome.
```js
const question = new Map([
  ['question', 'What is the best programming language in the world?'],
  [1, 'C++'],
  [2, 'Java'],
  [3, 'JavaScript'],
  ['correct', 3],
  [true, 'Correct!!'],
  [false, 'Try Again!'],
]);
```
Object.entries() returns an array of arrays so this means there is an easy way to convert from Objects to Maps.



```js
const openingHours = {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, 
      close: 24,
    },
  };

const hoursMap = new Map(Object.entries(openingHours));

console.log(hoursMap);
```


Map iteration:


```js
const question = new Map([
  ['question', 'What is the best programming language in the world?'],
  [1, 'C++'],
  [2, 'Java'],
  [3, 'JavaScript'],
  ['correct', 3],
  [true, 'Correct!!'],
  [false, 'Try Again!'],
]);

// Fake quiz app

console.log(question.get('question'))

for (const [key, value] of question) {
  if(typeof key === 'number') {
    console.log(`Answer ${key}: ${value}`);
  }
}
const answer = Number(prompt('Your answer'));
console.log(answer);
// 3

console.log(question.get(question.get('correct') === answer));
```

The quiz app shows the benefit of being able to have booleans as keys.


Converting a map to an array (Using the spread operator):

```js
console.log([...question]);
```

Other Map methods:

```js
question.entries();
question.keys();
question.values();
```
These do return an Iterator so you need to spread them into an array.

```js
console.log([...question.entries()]);
console.log([...question.keys()]);
console.log([...question.values()]);
```


# Which Data Structure To Use

There are 3 sources of data:

1. From the program itself

- Data written directly in source code Ex.) Status messages displayed on webpages based on user actions

2. From the UI

- Data input from the user or data written in the DOM Ex.) tasks in a todo app

3. From external sources

- Data fetched from web APIs

There are usually always collections of this data that needs to be stored and we stored them in data structures.

There are 4 main data structures in Javascript. Objects, Array, Maps & Sets.


Simple list:
Use Arrays or Sets

Key Value pairs:
Use Objects or Maps

Other built-in data-structures:
- WeakMap
- WeakSet

Non-built in:
- Stacks
- Queues
- Linked Lists
- Trees
- Hash Tables


Arrays vs Sets & Objects vs Maps


Arrays:
- Use when you need ORDERED list of values (might contain duplicates)
- Use when you need to MANIPULATE data. (Many built in methods)

Sets:
- Use when you need to work with UNIQUE values
- Use when HIGH-PERFORMANCE is required (Up to 10x faster than arrays ex.) searching/deleting) 
- Use to REMOVE DUPLICATES from arrays

Objects:
- More traditional key/value store but has been abused especially with maps now available in ES6
- Easier to write and access values with . & []
- Use when you need to include functions(methods in the data structure)
- Can use the this keyword to access properties which is impossible in maps
- Use when working with JSON(Can convert to a map)

Maps:
- Better performance
- KEYS can have ANY DATA TYPE
- Easy to iterate
- Easy to compute size
- Use when you simply need to map keys to values
- Use when the keys need to be another data type than string


# Strings

All string methods are case sensitive


```js
const airline = 'Air Canada'
const plane = '747';

console.log(plane[0]);
// "7"
console.log(plane[1]);
// "4"
console.log('747'[2]);
// "7"


console.log(airline.length);
// 10
console.log('747'.length);
// 3


console.log(airline.indexOf('r'));
// 2
console.log(airline.lastIndexOf('a'));
// 10
console.log(airline.indexOf('Canada'));
// Case sensitive 4 (gives starting position)
console.log(airline.indexOf('Air'));
// 0
console.log(airline.indexOf('canada'));
// -1 (not in string)


// Slice allows you to define the desired starting and ending index

console.log(airline.slice(4));
// Canada
console.log(airline.slice(4, 7));
// Can

console.log(airline.slice(0, airline.indexOf(' ')));
// Air
console.log(airline.slice(airline.lastIndexOf(' ') + 1));
// Canada

console.log(airline.slice(-6));
// Canada
console.log(airline.slice(0, -7));
// Air
```


```js Example
// B & E are middle seats in this example
const  checkMiddleSeat = function(seat){
  const letter = seat.slice(-1);
  if(letter === 'B' || letter === 'E') {
    console.log('You got the middle seat');
  } else {
    console.log('You got lucky!')
  }
}

checkMiddleSeat('11B');
checkMiddleSeat('23C');
checkMiddleSeat('3E');
```

Strings are just primitives so why do they have methods?

Whenever we call a method on a string JS converts the primitive to an object with the same content then the methods are called on that object. This is called boxing in JS.

```js
console.log(new String('Jonas'));
// String {"jonas"}

console.log(typeof new String('Jonas'));
// object
```

All methods called on a string object return a primitive string.


```js
console.log(airline.toLowerCase());
// air canada
console.log(airline.toUpperCase());
// AIR CANADA

// Fix capitalization in a names
const passenger = 'jOnAs';
const passengerLower = passenger.toLowerCase();
const passengerCorrect = passengerLower[0].toUpperCase() + passengerLower.slice(1);
console.log(passengerCorrect);
// Jonas

// Comparing email
const email = 'hello@jonas.io';
const loginEmail = '  Hello@Jonas.Io \n';

const lowerEmail = loginEmail.toLowerCase();
const trimmedEmail = lowerEmail.trim();
console.log(trimmedEmail);
// hello@jonas.io

const normalizedEmail = loginEmail.toLowerCase().trim();
console.log(normalizedEmail);
// hello@jonas.io
console.log(email === normalizedEmail);
// true
```


```js Replacing
const priceGB = '288,97£';
const priceUS = priceGB.replace('£', '$').replace(',','.');
console.log(priceUS);
// 288.97$

const annoucement = 'All passengers come to boarding door 23. Boarding door 23.';

console.log(announcement.replace('door', 'gate'));
// All passengers come to boarding gate 23. Boarding door 23.
```

Regular Expression:

```js
console.log(announcement.replace(/door/g, 'gate'));
// All passengers come to boarding gate 23. Boarding gate 23.
```


Booleans:

```js
const plane = 'A320neo';
console.log(plane.includes('A320'));
// true
console.log(plane.includes('boeing'));
// false
console.log(plane.startsWith('Air'));
// false
console.log(plane.endsWith('neo'));
// true
```

All of the above methods DO NOT mutate the original string.



```js
console.log(`a very nice string`.split(' '));
// Array(4) [ "a", "very", "nice", "string" ]

const [firstName, lastName] = 'Jonas Schmedtmann'.split(' ');
console.log(firstName);
// Jonas

const fullName = ['Mr.', firstName, lastName.toUpperCase()].join(' ');
console.log(fullName);
// Mr. Jonas SCHMEDTMANN


const capitalizeName = function(fullName) {
  const names = fullName.split(' ');
  const namesUpper = [];

  for (const name of fullName) {
    // namesUpper.push(name[0].toUpperCase() + name.slice(1));
    namesUpper.push(name.replace(name[0], name[0].toUpperCase()));
  }
  console.log(namesUpper.join(' '));
}

capitalizeName('jessica ann smith davis');
// Jessica Ann Smith Davis
capitalizeName('joans schmedtmann')
// Jonas Schmedtmann
```

Padding a string - add a number of characters to a string until it has a certain desired length

```js
const message = 'Go to gate 23';
console.log(message.padStart(25, '+'));
// This increases the string length to 25
// ++++++++++++Go to gate 23

console.log(message.padStart(25, '+').padEnd(30, '+'));
// Now the string length is 35
// ++++++++++++Go to gate 23+++++
```

```js Credit Card example
const maskCreditCard = function(number) {
  const str = number + '';
  // Converts number to string
  const last = str.slice(-4);
  return last.padStart(str.length, '•')

}

maskCreditCard(99999893);
maskCreditCard(4554466657774989893);
maskCreditCard('4554466657774989893');
```

Repeat Method:

```js
const message2 = 'Bad weather... All Departures Delayed...';
console.log(message.repeat(5));
// "Bad weather... All Departures Delayed...Bad weather... All Departures Delayed...Bad weather... All Departures Delayed...Bad weather... All Departures Delayed...Bad weather... All Departures Delayed..."
```

```js
const planesInLine = function(n) {
  console.log(`There are ${n} planes in line ${'[PLANE]'.repeat(n)}`);
}

planesInLine(5);
// " There are 5 planes in line [PLANE][PLANE][PLANE][PLANE][PLANE] "
```


--- 
# A Closer Look At Functions
---

# Default Parameters


Some parameters in functions can have a set default.


```js
const bookings = [];

const createBooking = function(flightNum,
 numPassengers = 1,
 price = 199 * numPassengers) {

  // Old way of setting default params
  numPassenger = numPassengers || 1;
  price = price || 199;

  // ES6 does it right in the params of the function
  // You can also perform operations in the params
  // In those operations you can use PREVIOUS (only previous) declared params in your operations


  const booking = {
    flightNum,
    numPassengers,
    price
  }
  console.log(booking);
  bookings.push(booking);
}
createBooking('LH123');
// {flightNum: "LH123", numPassengers: undefined, price: undefined}

createBooking('LH123', 2, 800);
// {flightNum: "LH123", numPassengers: 2, price: 800}

createBooking('LH123', undefined, 800);
// The only way to skip a parameter is to set it to Undefined

createBooking('LH123', 800);
// Trying to skip numPassengers and set price to 800 does not work as the arguments are mapped to the params in order
// {flightNum: "LH123", numPassengers: 800, price: undefined}
```


# Passing Arguments - Value vs Reference

```js
const flight = 'LH234';
const jonas = {
  name: 'Jonas Schmedtmann',
  passport: 123456789,
}

const checkIn = function(flightNum, passenger) {
  flightNum = 'LH999';
  passenger.name = 'Mr. ' + passenger.name;

  if(passenger.passport === 123456789) {
    alert('Check in')
  } else {
    alert('Wrong passport')
  }
}

checkIn(flight, jonas);
console.log(flight);
console.log(jonas);
// LH234
// {name: Mr. Jonas Schmedtmann, passport: 123456789}
```

The flight is a primitive (a string) and when it is passed into the function the flightNum param in the checkIn() function is basically a copy of the original value not the original.

It is the same as saying:
```js
const flightNum = flight;
```

So it is a completely different variable and the change will not be reflected outside in the original flight variable.

However the passenger param in the checkIn() function mutates the original object because when you pass a reference type to a function what is copied is the reference to the object in the memory heap.

It is the same as saying:

```js
const passenger = jonas;
```

These both point to the same object in memory and is why it is mutated when altering the passenger param in the checkIn() function.

* See line 907 for chapter on primitives vs reference types.

Passing a primitive type to a function is the same as creating a copy outside the function.

Passing an object to a function, anything altered will be reflected in the original.

Because of this behavior we must be careful and pay attention to multiple functions interacting with the same object and use our knowledge of primitives vs reference types(objects) to avoid issues.

```js Simple example of the issue
const newPassport = function(person) {
  person.passport = Math.trunc(Math.random() * 10000000);
}

newPassport(jonas);
// Here the original object is altered
checkIn(flight, jonas)
// So now this function throws an error
```

Passing by value & passing by reference:

JS does not have passing by reference only passing by value even though it appears to be passing by reference.

In other languages like C++ you can pass a reference to a value instead of the value itself. This works even with primitives so passing a reference to a primitive will actually alter the original. This is called passed by reference.

In JS for objects we pass a reference, however that reference is still a value. Just a value that contains a memory address.

So basically we PASS A REFERENCE to the function but we DO NOT PASS BY REFERENCE.

This is an important distinction.



# First-Class & Higher Order Functions

JS has first class function which allows us to write higher order functions.

JS treats function as first-class citizens meaning that functions are simply values. Functions are just another type of object.

This is an extremely important feature of the language.

Since objects are values and functions are objects that means functions are values too.

This is how we can store them in variables and object properties(methods) for example.

We can also pass arguments to other functions (callbacks).

We can also return functions from other functions.

Functions even have their own set of methods (bind, call ,apply).



Higher Order Function:

These are functions that receive another function as an argument or that returns a new function or both.

And this is only possible because JS has first-class functions.

Ex.) addEventListener('click', greet);

addEventListener is a higher order function with greet being a callback.

First class functions is only a concept. It is the concept that in a language like JS FUNCTIONS ARE VALUES. Thats it.

Because of this we can write higher order functions.


# Functions Accepting Callback functions

```js
// Changes first word to uppercase
const upperFirstWord = function(str) {
  const [first, ...other] = str.split(' ');
  return [first.toUpperCase(), ...others].join(' ');
}


// Higher order function
const transformer = function(str, fn) {
  console.log(`Original string: ${str}`)
  console.log(`Transformed string: ${fn(str)}`);
  console.log(`Transformed by: ${fn.name}`)
}

transformer('Javascript is the best', upperFirstWord);
// Original string: Javascript is the best
// Transformed string: JAVASCRIPT is the best
// Transformed by: upperFirstWord
```

Callbacks are very helpful for abstraction. Hiding away the fine details so we can think about programs at a higher abstract level.


# Functions Returning Functions

```js
const greet = function(greeting) {
  return function(name) {
    console.log(`${greeting} ${name}`);
  }
}

// We store the result of the greet function in a variable and that variable value is now essentially a function. And more specifically it is the returned function within the greet function. And now we can call the greeterHey function as if it was any other function we defined ourselves
const greeterHey = greet('Hey');

greeterHey('Jonas');
// Hey Jonas
greeterHey('Steven');
// Hey Steven
```

YUou can also do it another way all at once instead of storing the inner function call in a variable.

```js
greet('Hello')('Jonas')
// Hello Jonas
```

This concept of functions returning functions is extremely important in the functional programming paradigm.


```js As an arrow function
const greet = greeting => name => console.log(`${greeting} ${name}`);
```


# Call & Apply Methods

Setting the this keyword manually.


```js
const lufthansa = {
  airline: 'Lufthansa',
  iataCode: 'LH',
  bookings: [],
  book(flightNum, name) {
    console.log(`${name} booked a seat on ${this.airline} flight ${this.iataCode}${flightNum}`);

    this.bookings.push({ flight: `${this.iataCode}${flightNum},`, name });
  },
};

lufthansa.book(239, 'Jonas Schmedtmann');
// Jonas Schmedtmann booked a seat on Lufthansa flight LH239

console.log(lufthansa.bookings);
// Array(1){flight: "LH239", name: Jonas Schmedtmann}


const eurowings = {
  airline: 'Eurowings',
  iataCode: 'EW',
  bookings: [],
};

const book = lufthansa.book;

book(23, 'Sarah Williams');
// This throws an error as it is a regular function call and will point to the global object (or undefined in strict mode)

// We need to be able to tell JS which airline to book for by setting the this keyword so we use bind, call and apply



// CALL
// With call the first argument is what you want to set the this keyword to.

book.call(eurowings, 23, 'Sarah Williams');

console.log(eurowings.bookings);
// Array(1){flight: "EW23", name: Sarah Williams}


const swiss = {
  airline: 'Swiss Air Lines',
  iataCode: 'LX',
  bookings: [],
}



// Apply
// With Apply the first argument is what you want to set the this keyword to and the second argument is an array of data.(Not used so much anymore in modern JS)

const flightData = [583, 'George Cooper'];
book.apply(swiss, flightData);
console.log(swiss.bookings);
// Array(1){flight: "EW583", name: George Cooper}

// Now we can just always use call with the spread operator instead of apply
book.call(swiss, ..flightData);
```

# Bind Method

Bind does not immediately call the function. Instead it returns a new function where the this keyword is bound. Its set to whatever value we pass into bind.


```js
const bookEW = book.bind(eurowings);
// Now in the bookEW function the this keyword is always bound to eurowings
bookEW(23, 'Steven Williams');

const bookLH = book.bind(lufthansa);
const bookLX = book.bind(swiss);

// This allows us to set the this keyword only once instead of every time we use the call method


const bookEW23 = book.bind(eurowings, 23);
// We can go further here by presetting the flight number, and all we need to provide now is a name and it will book to the specified airline and flight number
bookEW23('Jonas Schmedtmann');
```

Specifying parts of the arguments before hand is called partial application.


Using Objects with Event Listeners:

```js
lufthansa.planes = 300;
lufthansa.buyPlane = function() {
  console.log(this);
  this.planes++;
  console.log(this.planes);
}

// Imagine a button with class="buy" on a page

document.querySelector('.buy').addEventListener('click', lufthansa.buyPlane);

// When clicking === NaN because the this keyword is now the button element

// So now we need to set the this keyword
// We need to pass in a function and not to call it and we know that the call method calls a function whereas the bind method returns a new function.
document.querySelector('.buy').addEventListener('click', lufthansa.buyPlane.bind(lufthansa));
```

The bind method really needs to be understood. Study if required.

# IIFE (Immediately Invoked Function Expressions)

```js
function runOnce = function() {
  console.log('This will never run again');
}
runOnce();


// IIFE
(function() {
  console.log('This will never run again')
})();
// Here we trick JS into thinking the statement is an expression by wrapping it in parentheses and calling it at the end with a second set of parentheses


// As an arrow function
(() => console.log('This will never run again'))();
```

Functions create scopes. Functions do not have access to variables from an inner scope. 

```js
(function() {
  console.log('This will never run again')
  const isPrivate = 23;
})();
console.log(isPrivate);
// ReferenceError: isPrivate is not defined
```

So here we say this data is private or encapsulated inside the function scope. Many times we need to ensure variables aren't overwritten by other functions or 3rd party libraries so we have a need for data privacy/encapsulation.

Variables declared with let or const create their own scope inside a block.

```js
{
  const isPrivate = 23;
  var notPrivate = 46;
}
console.log(isPrivate);
// ReferenceError: isPrivate is not defined
console.log(notPrivate);
```

IIFE's aren't used as much anymore in ES6 because of this but still have their place.



# Closures

Closures are not a feature that we explicitly use. They happen automatically in certain situations.

```js
const secureBooking = function() {
  let passengerCount = 0;

  return function() {
    passengerCount++;
    console.log(`${passengerCount} passengers`);
  }
}

// Now booker is a function as well
const booker = secureBooking();
```

In the call stack and scope chain:

- Our code starts by running in the global execution context where there is currently only the secureBooking function on the call stack. The global scope now contains secureBooking.

- Then when secureBooking is actually executed a new execution context for secureBooking is put on top of the execution stack and the variable environment of it contains its local variables (passengerCount = 0;), this environment variable is also the scope of this function which then gets access to all the variables of the parents scopes(Global scope) in the scope chain

- In the next line the returned inner function from the secureBooking() function is stored in the booker variable.

- The global scope & global execution context now contain the booker variable

- Now the secureBooking() execution context is finished and pops off the stack


Back to code:

```js
const secureBooking = function() {
  let passengerCount = 0;

  return function() {
    passengerCount++;
    console.log(`${passengerCount} passengers`);
  }
}

// Now booker is a function as well
const booker = secureBooking();

// Now we call it a few times
booker();
booker();
booker();
// 1 passengers
// 2 passengers
// 3 passengers
```

How is it possible that the secureBooking() function has finished executing and its execution context has popped off the call stack but the passengerCount variable is still being updated?


A closure makes a function remember all the variables that existed at the functions "birth place" or declaration.

We can imagine the secureBooking as being the birthplace of the booker function.

Back in the call stack and scope chain:


- Again the secureBooking() execution context has already been removed from the call stack

- Now the booker function runs located in the global scope

- A new execution context is created and put on the call stack and its variable environment is empty because there are no variables declared in this function

- The booker function is a child scope of the global scope

* This is the secret of closures

- Any function always has access to the variable environment of the execution context in which the function was created

- In the case of booker it was declared in the execution context of secureBooking() which was previously popped off the stack

- So the booker function gets access to the variable environment containing the passengerCount variable

- This is how the booker function can read and manipulate the passengerCount variable

This connection is what is called closure


* Any function always has access to the variable environment of the execution context in which the function was created even after that execution context is gone.

So the closure is the variable environment attached to the function exactly as it was at the time and place the function was created.

We say the booker function closed over its parents variable environment or scope.

- The booker function now attempts to increase the passengerCount variable but cannot find it in it's current scope

- JavaScript immediately looks into the closure to see if it can find the variable there even before looking in the scope chain (Closures have priority over the scope chain)

- Then the passengerCount variable is increased to 1 and the booker execution context is popped off the stack

- This is repeated for the next 2 calls of the booker function because the booker function will have access to the variable environment holding the passengerCount variable FOREVER.


Summary/Definitions:

Formal
1. A closure is the closed-over variable environment of the execution context in which the function was created, even after that execution context is gone.

Informal
2. A closure gives a function access to all the variables of its parent function, even after that parent function has returned. The function keeps a reference to its outer scope, which preserves the scope chain throughout time

JS creates closures automatically and there is no way for us to explicitly access closed over variables they are just an internal property of a function.

We can only observe them by seeing that variables are accessible even after they seem to be gone.


```js
console.dir(booker);
// In Chrome we can see in the Scopes tab there is a Closure tab that has the passengerCount variable from the secureBooking
```


---
# Working With Arrays
---

# Simple Array Methods


```js Sample Data
const currencies = new Map([
  ['USD', 'United States dollar'],
  ['EUR', 'Euro'],
  ['GBP', 'Pound sterling'],
]);

const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];
```

All instances of arrays have access to built in methods because of prototypal inheritance.


```js SLICE
// SLICE
// The slice methods allows us to take a piece of an array without mutating the original array.

// The first argument is the beginning and the second argument is where to go to

let arr = ['a', 'b', 'c', 'd', 'e'];

console.log(arr.slice(2));
// ["c", "d", "e"]
console.log(arr.slice(2, 4));
// ["c", "d"]
console.log(arr.slice(-2));
// ["d", "e"]
console.log(arr.slice(-1));
// ["e"]
console.log(arr.slice(1, -2));
// ["b", "c"]

// To create a shallow copy of the entire array omit any arguments

console.log(arr.slice());
// ['a', 'b', 'c', 'd', 'e']
console.log([...arr]);
// ['a', 'b', 'c', 'd', 'e']

// Exact same as using the spread operator and neither one has a benefit over the other except slice can be chained with multiple methods.
```


```js SPLICE
// SPLICE
// The splice method works the same way as slice except it does mutate the original array.

// The first argument is the beginning and the second argument is how many elements to delete

let arr = ['a', 'b', 'c', 'd', 'e'];

console.log(splice(2));
console.log(arr);
// ["a", "b"]

// Mainly used for removing items from an array
// Very common for removing the last item in an arrays

console.log(arr.splice(-1));
console.log(arr);
//['a', 'b', 'c', 'd']

console.log(arr.splice(1, 2));
console.log(arr);
// ["a", "d"]
```


```js REVERSE
// REVERSE
// Reverses an array in place and mutates the original array

let arr2 = ['j', 'i', 'h', 'g', 'f'];

console.log(arr2.reverse());
// ["f", "g", "h", "i", "j"]
console.log(arr2);
// ["f", "g", "h", "i", "j"]
```

```js CONCAT
// CONCAT
// Joins 2 arrays together and does not mutate the originals

const letters = arr.concat(arr2);
console.log(letters);
// ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j"]

// Same with the spread operator (Also doesn't mutate)
console.log([...arr, ...arr2]);
// ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j"]
```

```js JOIN
// JOIN
// Joins elements of an array with a separator that we specify

console.log(letters.join(' - '));
// a - b - c - d - e - f - g - h - i - j
```




# Looping Arrays - forEach


```js forEach
// forEach
//

const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];

// With a for of loop
for (const movement of movements) {
  if(movement > 0) {
    console.log(`You deposited the ${movement}`);
  } else {
    console.log(`You withdrew ${Math.abs(movement)}`);
    // Math.abs = absolute value (removes the negative signs)
  }
}

// You deposited the 200 
// You deposited the 450 
// You withdrew 400 
// You deposited the 3000 
// You withdrew 650 
// You withdrew 130 
// You deposited the 70 
// You deposited the 1300


// With forEach method

// forEach is a higher order function that requires a callback that is called on each element on the array

movements.forEach((movement) => {
  if(movement > 0) {
    console.log(`You deposited the ${movement}`);
  } else {
    console.log(`You withdrew ${Math.abs(movement)}`);
  }
});

// You deposited the 200 
// You deposited the 450 
// You withdrew 400 
// You deposited the 3000 
// You withdrew 650 
// You withdrew 130 
// You deposited the 70 
// You deposited the 1300
```


If we need access to a counter variable

```js
const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];

// With a for of loop we can access the current index by using the .entries method to get an array of arrays

for (const [i, movement] of movements.entries()) {
  if(movement > 0) {
    console.log(`Movement ${i + 1}: You deposited ${movement}`);
  } else {
    console.log(`Movement ${i + 1}: You withdrew ${Math.abs(movement)}`);
    // Math.abs = absolute value (removes the negative signs)
  }
}

// Movement 1: You deposited 200 
// Movement 2: You deposited 450 
// Movement 3: You withdrew 400 
// Movement 4: You deposited 3000 
// Movement 5: You withdrew 650 
// Movement 6: You withdrew 130 
// Movement 7: You deposited 70 
// Movement 8: You deposited 1300



// With forEach
// forEach passes in the current element, the index and the array that we are looping over to its callback function
// 1st is the current element
// 2nd is the index
// 3rd is the array
// We can omit some if we'd like but they will then appear in the corresponding defined order

movements.forEach((mov, i, arr) => {
  if(mov > 0) {
    console.log(`Movement ${i + 1}: You deposited ${mov}`);
  } else {
    console.log(`Movement ${i + 1}: You withdrew ${Math.abs(mov)}`);
    // Math.abs = absolute value (removes the negative signs)
  }
});

// Movement 1: You deposited 200 
// Movement 2: You deposited 450 
// Movement 3: You withdrew 400 
// Movement 4: You deposited 3000 
// Movement 5: You withdrew 650 
// Movement 6: You withdrew 130 
// Movement 7: You deposited 70 
// Movement 8: You deposited 1300
```

Keep in mind these values are reverse from each other when using forEach or for of.

forEach the element is first then the index.

for of the index is first then the element.


When to use:

You cannot break out of a forEach loop and it will always loop over the entire array. With for of you can use the continue and break statements to exit the loop.


# forEach With Maps And Sets

```js MAPS
const currencies = new Map([
  ['USD', 'United States dollar'],
  ['EUR', 'Euro'],
  ['GBP', 'Pound sterling'],
]);


// Similar to the array loop but for a map it goes in the order of value, key then map
currencies.forEach((value, key, map) => {
  console.log(`${key}: ${value}`);
});

///USD: United States dollar 
// EUR: Euro 
// GBP: Pound sterling
```



```js SETS
const currenciesUnique = new Set(['USD', 'GBP', 'USD', 'EUR', 'EUR']);
console.log(currenciesUnique);
//[ "USD", "GBP", "EUR" ]

currenciesUnique.forEach((value, key, map) => {
  console.log(`${key}: ${value}`);
});

// USD: USD 
// GBP: GBP 
// EUR: EUR

// Sets don't have keys or indexes so when designing the forEach loop the developers left it having 3 parameters but when used on sets the 2nd key param just equals the first param 


// In this instance we use an underscore _ which is the standard in JS for just a throw away variable
currenciesUnique.forEach((value, _, map) => {
  console.log(`${key}: ${value}`);
});

// USD: USD 
// GBP: GBP 
// EUR: EUR
```


# Creating DOM Elements

- Instead of working with global variables start with passing that data that a function needs into that function

- textContent returns the text itself while innerHTML returns the HTML as well

- It is bad practice tyo mutate function parameters. Rather create a copy and mutate that




# Map, Filter & Reduce


Overview:

Map:
- Used for looping over Arrays
- Similar to forEach but creates a new array with all the new values mapped to it and does not mutate the original like forEach


Filter:
- Used to filter for elements in the original array that satisfy the conditions
- These elements are put into a new array


Reduce:
- Boils down all the elements of the original array into a single value
- Uses an accumulator and current value


```js MAP METHOD
// We want to convert EUR to USD
// The callback again takes the element, the index and teh array
const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];

const eurToUsd = 1.1;

const movementsUSD = movements.map(mov => {
  return mov * eurToUsd;
});
console.log(movements);
console.log(movementsUSD);
```

The big difference between map and forEach is that the forEach method creates side effects.

A side effect is any application state change that is observable outside the function other than its return value.
Side effects include: Modifying any external variable or object property ex.) a global variable, or a variable in the parent function scope chain.


There is a push toward functional programming in modern JS.


* Side note
It is handy to use the ternary operator especially when working with strings if the returned string needs to be only one or another option.

```js
`Movement ${i + 1}: You ${mov > 0 ? 'deposited' : 'withdrew'}`
```




```js MAP METHOD
const user = 'Steven Thomas Williams'; // stw

const username = user.toLowerCase().split(' ').map(el => {
  return el[0];
}).join('');
// stw


// Also formatting the code makes it more readable
const username = user
  .toLowerCase()
  .split(' ')
  .map(el => el[0])
  .join('');
```

We can combine different methods knowing which method can be called on what data type in the proper order.

Above we have  strong that is changed to lowercase then split into an array. We can then call map which is an array method which returns another array which we can call the array method join on and get our user name as a result.

```js
const createUserNames = (accs) => {
  accs.forEach((acc) => {
    acc.username = acc.owner
      .toLowerCase()
      .split(' ')
      .map(el => el[0])
      .join('');
  });
}
createUserNames(accounts);
```

We then turn it into a reusable function for any data inputted to get the same result.

The forEach method creates the side effect of adding a property of username to each account and updating it with the value we specified. This is why we do not have to explicitly set a return from the function as the forEach just "Does some work" for us.



# Filter Method


```js FILTER
// Filter
// Filter again has a callback that has the current element, the index and the array
const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];

const deposits = movements.filter(function (mov) {
  return mov > 0;
});

console.log(deposits);
// [ 200, 450, 3000, 70, 1300 ]
```

The big advantage of using these built in methods is that we can chain them whereas with the for of loop you cannot


# Reduce Method

```js REDUCE
// Reduce
// In reduces callback function the first param is the accumulator and the second is the current element the third is the index and the fourth is the arr (usually used with just the first 2)
// The accumulated value needs to be returned so the accumulated value can be used in the next iteration of the loop
// The reduce method has a second parameter in addition to its callback. It is the initial value to start at in the first loop iteration, in this case is 0.

const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];


const result = movements.reduce(function(acc, cur) {
  return acc + cur;
}, 0);
console.log(result);
// 3840
```


We can use reduce to return more than just number.

Ex.) Get the max value in the array

```js
const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];

const maxValue = movements.reduce((acc, cur) => {
  acc >= cur ?  acc = acc : acc = cur;
  return acc;
}, movements[0]);
```

Do not use 0 when you are trying to find the max or min value as the second param of reduce. Use the first element in the array.


# Chaining Methods


```js
const eurToUsd = 1.1;

const totalDepositInUsd = movements.filter(mov => mov > 0).map(mov => mov * eurToUsd).reduce((acc, cur) => acc + cur, 0);
// 5522
```

Above the filter method returns an array. We can then call map on that array. and that returns another copied array which we can call the reduce method on and we could even call more filters, maps as required.

Keep in mind "pipelines"(chaining) like this can be hard to debug. So it is good to utilize the array parameter in the callback functions on each following step to find the previous calculation that went wrong


```js Debugging Chaining
// Here maybe we accidentally set the filter to everything less than 0 (withdrawals) when we only wanted positive values(deposits)

const eurToUsd = 1.1;

const totalDepositInUsd = movements
  .filter(mov => mov < 0)
  .map((mov, i, arr) => {
    console.log(arr)
    // [-400, -650, -130]
    return mov * eurToUsd;
  })
  .reduce((acc, cur) => acc + cur, 0);
  // -1298
```

Keep In Mind:

1. Do not overuse chaining as it can cause performance issues. (Try to compress manipulation into as few methods as possible).

2. It is a bad practice in JS to chain methods that mutate the under laying array. Ex.) Splice or reverse. Even though you can but in a large scale app it is good practice to avoid this.


# Find Method


```js Find
// find
// Also takes a callback that loops over the array
// Does not return a new array. It only returns the first element that satisfies the specified condition 

const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];

movements.find(mov => mov < 0);
// -400
``` 

# Random notes

* Side note

For your own sanity, please try to remember use parentheses when calling the preventDefault method.

```js
element.addEventListener('click', function(e) {
  e.preventDefault;
  // This DOES NOT work

  e.preventDefault();
  // This DOES
});
```

- Hitting enter when in an input of a form will cause a submit event on the button attached to that form

- The assignment operator works from right to left and you can use it for multiple variables. Handy for resets.

```js
inputLoginUsername.value = inputLoginPin.value = '';
```

- Optional chaining is important when searching as we can avoid errors or handle them easily with the nullish coalescing because something that is not found will return undefined


# findIndex Method

To delete and element we use the splice method. To use splice we need the index so this is where findIndex comes in.


```js findIndex
// findIndex
// This method also takes a callback function which has 4 params of the current element, index of the current element, the array and a thisArg.

const index = accounts.findIndex(acc => acc.username === currentAccount.username);
accounts.splice(index, 1);
```

The major difference between findIndex and indexOf is that with indexOf you can only search for a value that is in the array.

With findIndex you can create complex logic to return a boolean and get the desired index that satisfies that boolean.


# some & every 

```js includes
const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];

console.log(movements.includes(-130));
// true
```
Includes can only really test for exact equality.


some() allows us to do conditional tests.

```js some
// some
// Takes a callback function for us to create complex conditionals

const anyDeposits = movements.some(mov => mov > 0);
console.log(anyDeposits);
// true
```


```js every
// every
// Similar to some but every single element must meets the condition in the callback function

const anyDeposits = movements.every(mov => mov > 0);
console.log(anyDeposits);
// false
```

If we find that we have repetitive callback methods, then we can put them into a separate callback to be reused across our code base and keep it DRY.

```js
const deposit = mov => mov > 0;

movements.some(deposit);
movements.every(deposit);
movements.filter(deposit);
```


# flat & flatMap

Used for when we have nested arrays

```js flat
// No callback functions
// By default only flattens one level deep
// We pass it an argument which is our depth param and can make it flatten however many levels deep we need (unlike flatMap - can only do one level deep)

const arr [[1, 2, 3], [4, 5, 6], 7, 8];
console.log(arr.flat());
// [1, 2, 3, ,4 ,5, 6, 7, 8];

const arrDeep [[[1, 2], 3], [4, [5, 6]], 7, 8];
console.log(arrDeep.flat());
//[[1, 2], 3, 4, [5, 6], 7 ,8]

console.log(arrDeep.flat(2));
// [1, 2, 3, ,4 ,5, 6, 7, 8];
```

Example:
A bank wants to get the overall balance of all accounts

```js Sample data
const account1 = {
  owner: 'Jonas Schmedtmann',
  movements: [200, 450, -400, 3000, -650, -130, 70, 1300],
  interestRate: 1.2, // %
  pin: 1111,
};

const account2 = {
  owner: 'Jessica Davis',
  movements: [5000, 3400, -150, -790, -3210, -1000, 8500, -30],
  interestRate: 1.5,
  pin: 2222,
};

const account3 = {
  owner: 'Steven Thomas Williams',
  movements: [200, -200, 340, -300, -20, 50, 400, -460],
  interestRate: 0.7,
  pin: 3333,
};

const account4 = {
  owner: 'Sarah Smith',
  movements: [430, 1000, 700, 50, 90],
  interestRate: 1,
  pin: 4444,
};

const accounts = [account1, account2, account3, account4];



const accountMovements = accounts.map(acc => acc.movements);
console.log(accountMovements);
// 0: Array(8) [ 200, 450, -400, … ]
// 1: Array(8) [ 5000, 3400, -150, … ]
// 2: Array(8) [ 200, -200, 340, … ]
// 3: (5) […
const allMovements = accountMovements.flat();
console.log(allMovements);
// Array(29) [ 200, 450, -400, 3000, -650, -130, 70, 1300, 5000, 3400, … ]

overallBalance = allMovements.reduce((acc, cur) => acc + cur, 0);
console.log(overallBalance);
// 17840



// We can chain it as well
overallBalance = accounts
  .map(acc => acc.movements)
  .flat()
  .reduce((acc, cur) => acc + cur, 0);
```

Using a map first then flattening it is a very common operation and that is why flatMap was introduced and is better for performance


```js flatMap
// flatMap
// Also needs a callback like a regular map functions
// CAN ONLY GO ONE LEVEL DEEP

overallBalance = accounts
  .flatMap(acc => acc.movements)
  .reduce((acc, cur) => acc + cur, 0);
// 17480
```


# Sorting Arrays


```js sort
// sort
// MUTATES the original array

const owners = ['Jonas', 'Zach', 'Adam', 'Martha'];

owners.sort();
//[ "Adam", "Jonas", "Martha", "Zach" ]


const movements = [200, 450, -400, 3000, -650, -130, 70, 1300];

movements.sort();
// [ -130, -400, -650, 1300, 200, 3000, 450, 70 ]
// This is not ordered
```

.sort() converts everything to strings then tries to sort

We fix this by passing in a compare callback function


```js sort
// The callback function takes 2 arguments
// a is the current value
// b is the next value

// If we return a value less than 0 then A will be before B (Keep Order)

// If we return a value greater than 0 than B will before A (Switch Order)
movements.sort((a, b) => {
  if(a > b) 
    return 1;
  if(b > a)
    return -1;
});
// ascending
// [ -650, -400, -130, 70, 200, 450, 1300, 3000 ]

movements.sort((a, b) => {
  if(a > b) 
    return -1;
  if(b > a)
    return 1;
});
// descending
// [ 3000, 1300, 450, 200, 70, -130, -400, -650 ]

// We can simplify this be doing 
movements.sort((a, b) => a - b;
);
```
The method works by analyzing if the returned value is greater or less than 0 so we can just use a - b or b - a to get the exact same desired result. We have to return the calculated value from the function. With an arrow function its easy because it has the implicit return.

Ex.) 
400 - (-600) = 1000
(-600) - 400 = -1000


Don't use the sort method on mixed data type arrays.


# State Variable

```js
// Here we set the default of sort to be false as a back up
const displayMovements = (movements, sort = false) => {

  containerMovements.innerHTML = '';

  // If sort is false then create a sorted array and store it in the movs variable to be used to set the html, otherwise if sort is true use the original movements array which is unsorted
  const movs = sort ? movements.slice().sort((a,b) => a - b) : movements;

  movs.forEach((mov, i) => {
    const type = mov > 0 ? 'deposit' : 'withdrawal';

    const html = `
    <div class="movements__row">
      <div class="movements__type movements__type--${type}">${i +1} ${type}</div>
      <div class="movements__value">${mov}</div>
    </div>
    `;
    containerMovements.insertAdjacentHTML('afterbegin', html);
  });
}

...
// We set the state variable outside so it persists and is not recreated every time
// Then every time we click we switch the boolean of the variable

let sorted = false;
btnSort.addEventListener('click', function(e) {
  e.preventDefault();
  displayMovements(currentAccount.movements, !sorted);
  sorted = !sorted;
});
```


# Creating & Filling Arrays


```js fill
// fill

const x = new Array(7);
// This specifies an empty array with the length of 7

x.fill(1);
// [ 1, 1, 1, 1, 1, 1, 1 ]
// Mutates the original arrays
// We can specify a begin and end parameter the same a slice

x.fill(1, 3, 5);
// Array(7) [ <3 empty slots>, 1, 1, <2 empty slots> ]
```


```js Array.from
// Takes an object as the first param specifying the length
// The the second param is a callback function the same as the map method where we get the current element, the index and the array.

const y = Array.from({length: 7}, () => 1);
console.log(y);
// [ 1, 1, 1, 1, 1, 1, 1 ]

// We mark a throw away variable in the callback here with the _ again
const z = Array.from({ length: 7 }, (_, i) => i + 1);
console.log(z);
// [1, 2, 3, 4, 5, 6, 7]
```

This method was originally introduced to create arrays from array-like structures so we can then use all the built in array methods on them.


```js
const movementsUI = Array.from(document.querySelectorAll('movements__value'));
```

You can also convert array-like structures into an array using the spread operator. But then any methods would need to be applied after spreading, you could not chain onto the spread.

```js
const movementsUI  = [...document.querySelectorAll('movements__value')]
```


# Which Array Method To Used

 
Need - MUTATE THE ORIGINAL:

Insert:

- .push (end)
- .unshift (start)

Delete:

- .pop (end)
- .shift (start)
- .splice (any)

Others:

- .reverse 
- .sort
- .fill


Need - A NEW ARRAY:

- .map (copy with a loop & callback)
- .filter (using a condition)
- .slice (copy of a portion or original)
- .concat (joining arrays)
- .flat (flatten as deep as needed)
- .flatMap (flattens 1 level with callback)



Need - ARRAY INDEX:

- .indexOf (based on value)
- .findIndex (based on conditional)


Need - ARRAY ELEMENT

- .find (based on conditional)



Need - ARRAY INCLUDES

- .includes (based on value)
- .some (based on conditional)
- .every (based on conditional)



Need - A NEW STRING

- .join (based on separator)



Need - TRANSFORM A VALUE

.reduce() (boil down to a single value of any type even a new array or object)


Need - TO LOOP AN ARRAY

- .forEach (based on callback/doesn't create a new array just loops over it)


---
# Numbers, Dates, Intl & Timers
---

# Converting & Checking Numbers

In JS all numbers are represented internally as floating point numbers even if we write them at full integers


```js
console.log(23 === 23.0);
// true
```

They are stored in a 64 base 2 format. That means numbers are stored in a binary format. In this binary form (base 2) it is hard to represent fraction that are easy to represent in a base 10 format like the regular deca system.

```js
console.log(0.1 + 0.2);
// 0.30000000000000004
```

In base 10 you can observe similar behavior.

1/10 = 0.1
3/10 = 0.33333333333333333333333

JS does its best in the background to do rounding but sometimes cannot represent some fractions at times.

```js
console.log(0.1 + 0.2 === 0.3);
// false
```

This is why JS is not the best language for precise mathematical or financial calculations.

An easy way to convert a string to a number is using the plus operator because when JS sees it it will try to perform type coercion.


Converting:
```js
console.log(Number(23));
console.log(+'23');
```

Parsing:

```js parseInt
// parseInt
console.log(Number.parseInt('30px'), 10);
// 30
console.log(Number.parseInt('e23'), 10);
// NaN
```
JS has some methods on the Number object to try and figure out what number a string may be. They HAVE TO START WITH A NUMBER to work.


The parseInt function accepts a second argument which is its radix (the base in the mathematical numeral systems) so we should always specify that because depending on the input with no radix specified JS will assume different radix resulting in unreliable behavior.

```js parseFloat
// parseFloat

console.log(Number.parseFloat('2.5rem'));
// 2.5
console.log(Number.parseInt('2.5rem'));
// 2
```


```js
// Check if value is NaN
console.log(Number.isNaN(20));
// false
console.log(Number.isNaN('20'));
// false
console.log(Number.isNaN(+'20X'));
// true
console.log(Number.isNaN(23/0));
// Infinity
// false 

// The isFinite method is the best way to check if a value is a real number when working with Floating Point number, and should be the go to out of these 3

console.log(Number.isFinite(20));
// true
console.log(Number.isFinite('20'));
// false
console.log(Number.isFinite(+'20X'));
// false
console.log(Number.isFinite(23 / 0));
// false

// Or with whole numbers we can use isInteger

console.log(Number.isInteger(23));
// true
```


# Math & Rounding

```js
// Square root
console.log(Math.sqrt(25));
// 5
console.log(25 ** (1/2));
// 5

// Cubic root
console.log(8 ** (1/3));


console.log(Math.max(5, 18, 23, 11, 2));
// 23
console.log(Math.max(5, 18, '23', 11, 2));
// 23
console.log(Math.max(5, 18, '23px', 11, 2));
// NaN
// Does type coercion but not parsing

console.log(Math.min(5, 18, 23, 11, 2));
//2

// Area of a circle (pi times radius squared)
console.log(Math.PI * Number.parseFloat('10px') ** 2)
// 314px


console.log(Math.trunc(Math.random() * 6) + 1);

const randomInt = (min, max) => Math.trunc(Math.random() * (max - min) + 1) + min;
// Math.random give us a number between 0 and 1

// 0...1 -> 0...(max - min) -> min...(max - min + min) -> min...max
```



```js Rounding Intergers

// All these methods do type coercion
console.log(Math.trunc(23.3));
// 23

console.log(Math.round(23.3));
// 23
console.log(Math.ceil(23.3));
// 24
console.log(Math.floor(23.9));
// 23


// .floor and .trunc do the same when dealing with positive numbers

console.log(Math.trunc(-23.3));
// -23
console.log(Math.floor(-23.3));
// -24

// Truncating removes the decimal point completely whereas flooring actually rounds down 
```


```js Rounding decimals
console.log((2.7).toFixed(0));
// 3 
// toFixed always returns a string an not a number
// The argument it takes is how many decimal places you wanted
console.log((2.345).toFixed(2));
// 2.35

// Easy conversion to numbers (just add the plus operator)
console.log(+(2.345).toFixed(0));
```


# Remainder Operator (Modulus)

```js
console.log(5 % 2);
// 1
// 2 * 2 + 1 = 5
```

Calculating even & odd numbers.
All numbers even % 2 number will return 0.
All odd numbers % 2 will return 1.

```js
console.log(6 % 2);
// 0
console.log(7 % 2);
// 1
```
So we can write a function to check if a value is even or odd.

```js
const isEven = n => n % 2 === 0;

isEven(8);
// true
isEven(13);
// false
```

We can then use this in our script for things like manipulating DOM elements. 

```js
// Must be attached to an event listener to run other wise on load the data overwrites it and it just looks normal

  [...document.querySelectorAll('.movements__row')].forEach(function(row, i) {
    if(i % 2 === 0) {
      row.style.backgroundColor = '#DDD';
    }
  })
```


```js With Event Listener
labelBalance.addEventListener('click', () => {
  [...document.querySelectorAll('.movements__row')].forEach(function(row, i) {
    // Every second list item changes its background to a lighter grey
    if(i % 2 === 0) {
      row.style.backgroundColor = '#DDD';
    }
  })
});
```


# BigInt (ES2020)


Numbers are represented internally as 64 bits which means there are 64 0s and 1s to represent any given number. 53 of the 64 are used to store the digits themselves. The rest are for storing the position of the decimal point and the Sin. If there are only 53 bits to store the numbers then that means there is a limit to how big numbers can be.

We can calculate that number:

```js
console.log(2 ** 53 - 1);
// 9007199254740991
console.log(Number.MAX_SAFE_INTEGER);
// 9007199254740991
// Max safe integer means any number above this can not be represented accurately

console.log(2 ** 53 - 1);
// 9007199254740991
console.log(2 ** 53 + 1);
// 9007199254740992
// Should be...
// 9007199254740993
```

```js Big Int
console.log(12352039768982457689245769824785645);
// 1.2352039768982459e+34
// This is the inaccurate versions

// So we put an n on the end to make it a big int
console.log(12352039768982457689245769824785645n);
//12352039768982457689245769824785645n
```

You cannot mix big int with other data types like a regular number in operations.

You can use comparison operators on them.

You can also use the + operator when working with strings.

The Math operations will not work.

Divisions will return the closest big int, cutting off the decimal

```js
huge = 90012094834598743892374982;
num = 2;
console.log(huge * BigInt(num));
// Uncaught TypeError: can't convert BigInt to number

console.log(12345902456092456n > 15);
// true

console.log(203954576578679789789 + ' is a big number');
//203954576578679800000 is a big number

console.log(Math.sqrt(16n));
// Uncaught TypeError: can't convert BigInt to number

console.log(10/3);
// 3.33333333333333333
console.log(10n/3n);
// 3n
```


# Creating Dates

JS Dates use the Unix Epoch which is when time in JS starts counting from. This is Jan 1st 1970 at midnight. Timezones affect this. (Based in miliseconds)

Ex.)  
```js
console.log(new Date(0));
// Wed Dec 31 1969 17:00:00 GMT-0700 (Mountain Standard Time)
```

There are 4 ways to create dates in JS:

1. Calling the Date which creates a date of now

```js
const now = new Date();
console.log(now);
// Date Sat Oct 31 2020 13:59:45 GMT-0600 (Mountain Daylight Time)
```

2. Passing the date function a string 

```js
console.log(new Date('Aug 2 2020 19:05:41'));
// Date Sun Aug 02 2020 19:05:41 GMT-0600 (Mountain Daylight Time)

console.log(new Date('December 25, 2015'));
// This works but passing dates not created by JS can be unreliable
```

3. Passing numbers to the date function in descending order (year, month, day, hour etc.) 

```js
console.log(new Date(2037, 10, 19, 15, 23, 5));
//Date Thu Nov 19 2037 15:23:05 GMT-0700 (Mountain Standard Time)
console.log(new Date(2037, 10, 19));
// JS Months are 0 based as this would normally be expected to be October
```

4. Passing calculations to the date function to work with the Unix Epoch
```js
console.log(new Date(0));
// Wed Dec 31 1969 17:00:00 GMT-0700 (Mountain Standard Time)
console.log(new Date(3 * 24 * 60 * 60 * 1000));
// 3 days after the Epoch
//Sat Jan 03 1970 17:00:00 GMT-0700 (Mountain Standard Time)
```


Working with dates:

```js
const future = new Date(2037, 10, 19, 15, 23);
console.log(future.getFullYear());
// 2027
console.log(future.getFullMonth());
// 0 based
// 10
console.log(future.getDate());
// 19
console.log(future.getDay());
// 0 based
// 4 (Thu)
console.log(future.getHours());
//15
console.log(future.getMinutes());
//23
console.log(future.getSeconds());
// 00

console.log(future.toISOString());
// 2037-11-19T22:23:00.000Z
// Good for storing dates in strings/arrays

console.log(future.getTime());
// 2142282180000
// milliseconds from jan1st 1970

console.log(new Date(2142282180000));
// Thu Nov 19 2037 15:23:00 GMT-0700 (Mountain Standard Time)

console.log(Date.now())
// 1604179326235
```

There are also methods for each of the corresponding methods above for setting.

```js
future.setFullYear(2040)
console.log(future);
// Mon Nov 19 2040 15:23:00 GMT-0700 (Mountain Standard Time)
```

# Random Notes

We can change data types into strings using template literals and then call string methods on them. Here for example we change this date into a string and specify that we want a max length of 2 and a padded character of 0, so if it was 10 or higher it would not pad because the max length  has already been reached

```js
const day = `${now.getDate()}`.padStart(2, 0);
```

A common practice is looping through 2 arrays at the same time (see the for Each loop below)

```js
const account1 = {
  owner: 'Jonas Schmedtmann',
  movements: [200, 455.23, -306.5, 25000, -642.21, -133.9, 79.97, 1300],
  interestRate: 1.2, // %
  pin: 1111,

  movementsDates: [
    '2019-11-18T21:31:17.178Z',
    '2019-12-23T07:42:02.383Z',
    '2020-01-28T09:15:04.904Z',
    '2020-04-01T10:17:24.185Z',
    '2020-05-08T14:11:59.604Z',
    '2020-05-27T17:01:17.194Z',
    '2020-07-11T23:36:17.929Z',
    '2020-07-12T10:51:36.790Z',
  ],
  currency: 'EUR',
  locale: 'pt-PT', // de-DE
};


const displayMovements = function (acc, sort = false) {
  containerMovements.innerHTML = '';

  const movs = sort ? acc.movements.slice().sort((a, b) => a - b) : acc.movements;

  movs.forEach(function (mov, i) {
    const type = mov > 0 ? 'deposit' : 'withdrawal';

    // Since the movements and dates are related they will have the same amount of corresponding indexes. Then we loop over the dates with the index from each movements as they will match each date. We create a date from each iteration and store it in a variable so we can access the Date objects methods.
    const date = new Date(acc.movementsDates[i]);

    const html = `
      <div class="movements__row">
        <div class="movements__type movements__type--${type}">${
      i + 1
    } ${type}</div>
    <div class="movements__date">${displayDate}</div>
        <div class="movements__value">${mov.toFixed(2)}€</div>
      </div>
    `;

    containerMovements.insertAdjacentHTML('afterbegin', html);
  });
};
```

# Operations With Dates


```js
const future = new Date(2037, 10, 19, 15, 23);
console.log(+future);


// Absolute here will negate negative numbers so it doesn't matter which date is first as its the same distance in time away from one another
const calcDaysPassed = (date1, date2) => Math.abs(date2 - date1) / (1000 * 60 * 60 * 24)

daysPassed1 = calcDaysPassed(new Date(2037, 10, 19), new Date (2037, 11, 1));
```

# Random Notes

It can be common to have this many returns, because as the code runs if the condition is met, it will be returned and it will exit the function.

```js
const formatMovementDate = function(date) {
  const calcDaysPassed = (date1, date2) => Math.round(Math.abs(date2 - date1) / (1000 * 60 * 60 * 24));

  const daysPassed = calcDaysPassed(new Date(), date);

  if(daysPassed === 0) return 'Today';
  if(daysPassed === 1) return 'Yesterday';
  if(daysPassed <= 7) return `${daysPassed} days ago`;


  const day = `${date.getDate()}`.padStart(2, 0);
  const month = `${date.getMonth() + 1}`.padStart(2, 0);
  const year = date.getFullYear();
  return `${day}/${month}/${year}`;
  
}
```

# Internationalization (Intl) - Dates/Times

A DOM element can be set as the result of calling the Intl.DateTimeFormat() on it. The formatter accepts 2 arguments, the locale and an options object. We can dynamically grab the locale from the navigator.language so whoever is viewing it the date is formatted in their locale. Then the options object specifies how we want each part of our date to be formatted. This object is usually stored in variable to keep the code cleaner. 
See MDN for reference on specific customization. Then the the we want to format is passed to the formatter using the .format() method with the date passed as the argument.


```js
const now = new Date();
const options = {
  year: 'numeric',
  weekday: 'long',
  month: 'short',
  day: 'numeric',
  hour: 'numeric',
  minute: 'numeric'
}
const locale = navigator.language;
labelDate.textContent = new Intl.DateTimeFormat(locale, options).format(now);
```



# Internationalization (Intl) - Numbers

Similar to the Date/Time API. See MDN for all options.

```js
const num = 3884764.23;
const options = {
  // 3 options for style
  // style: "unit",
  // style: "percentage",
  style: "currency",

  currency: 'EUR',

  // unit: 'mile-per-hour'
  // unit: 'celsius',
}

console.log('US:', new Intl.NumberFormat('en-US', options).format(num));
// US: 3,884,764.23

console.log('GErmany:', new Intl.NumberFormat('de-DE', options).format(num));
// Germany: 3.884.764,23

console.log('Syria:', new Intl.NumberFormat('ar-SY', options).format(num));
// Syria: ٣٬٨٨٤٬٧٦٤٫٢٣

// Or just grab the users locale
console.log(navigator.language, new Intl.NumberFormat(navigator.language, options).format(num));
// en-CA 3,884,764.23


// US: 3,884,764.23 mph 
// GErmany: 3.884.764,23 mi/h 
// Syria: ٣٬٨٨٤٬٧٦٤٫٢٣ ميل/س 
// en-CA 3,884,764.23 mph
```

We can build useful helper functions out of these APIs for reuse across applications.


```js
const formatCur = function(value, locale, currency) {
  return new Intl.NumberFormat(locale, {
    style: 'currency',
    currency,
  }).format(value);
}
```


# Timers

Set timeout takes a callback and how long in milliseconds it should wait until it runs. It only runs once.

```js
setTimeout(() => console.log('Here is your pizza.'),3000);
```

For repeated actions use setInterval.

```js
setInterval(function() {
  const now = new Date();
  console.log(now);
}, 1000)
```


---
# Advanced DOM & DOM EVents
---

The DOM is basically the interface between JS and the browser(More specifically HTML documents that are rendered in and by the browser).

- Allows us to make JS interact with the browser

- We can write JS to create, modify and delete HTML elements, set styles, classes and attribute, and listen and respond to events

- A DOM tree (made up of nodes) is generated from an HTML document, which we can then interact with

- DOM is a very complex API that contains lots of methods and properties to interact with the DOM tree


How the DOM API is organized behind the scenes:

- Every single node in the DOM tree is of the type Node. 

- Each node is represented in JS by an object. (Everything in JS is an object). This gives access to special node methods and properties based on what type of node it is
Ex.) .textContent, .parentNode, .cloneNode() etc.

There are 4 child node types:

- Element
HTML element <p></p>
- Text
paragraph
- Comment
<!--  -->
- Document


Each element will be represented internally as an object and has internally an HTML element child type. There is a different type of HTMLElement for each HTMLElement.
Ex.) HTMLButtonElement, HTMLDivElement, HTMLLinkElement etc.

There is inheritance of methods and properties. All children elements have access to their parents properties.


The DOM API needs a way for all nodes to listen to events. So there is a parent node type called EventTarget that is parent of nodes and parent of the window. So every single type of node has access to event listeners because of inheritance.



# Selecting, Creating & Deleting Elements

Selecting:

```js
// To select the document element:
console.log(document.documentElement);

// Head & body
console.log(document.head);
console.log(document.body);

const allSections = document.querySelectorAll('.section');
// returns a node list
```

The .getElementsByTagName will return an HTML Collection
```js
const allButtons = document.getElementsByTagName('button');
```

An HTML Collection returned from the .getElementsByTagName will auto update (This is called a live collection) so if for example a button is removed from the DOM in the instance above the allButtons would have one less element in it. Whereas with a node list even after deleting a section in the DOM it would still show in the allSection variable. 


```js
 document.getElementsByClassName('btn');
 // This also returns a live HTML collection
```



Creating & Inserting:

```js
// .insertAdjacentHTML

// This creates a DOM element
const message = document.createElement('div');

// And we can alter it
message.classList.add('cookie-message');
message.textContent = 'We use cookies for improved functionality and analytics.';
message.innerHTML = 'We use cookies for improved functionality and analytics. <button class"btn btn--close-cookie">Got it!</button>';

// Then insert it
header.prepend(message);
// Before or...
header.append(message);
// After...
```
Keep in mind because we have created an actual DOM element, we can only put it in one place so the above code the prepend would be overwritten by the append and the element would show at the bottom

So if we wanted 2 of the same, which is usually not common but doable:

```js
header.append(message.cloneNode(true));
// The true is for is if we want to clone all children nodes as well
```

There are 2 more methods:
```js
header.before(message);
header.after(message);
```


Deleting:

```js
document.querySelector('.btn--close-cookie').addEventListener('click',function() {
  message.remove();
});
```
You used to have to go to the parent element of the element you wanted to delete to delete it. The remove() method is recent.

```js Old school
document.querySelector('.btn--close-cookie').addEventListener('click',function() {
  message.parentElement.removeChild(message);
});
```


# Styles, Attributes & classes


Styles:

```js Setting styles
// Defines an in-line style
message.style.backGroundColor = '#37383d';

message.style.width = '120%';

console.log(message.style.height);
// Returns nothing
```

```js Getting styles
console.log(getComputedStyle(message).color);
```

Using getComputedStyle to set styles for elements that have no in-line style defined
```js
message.style.height = Number.parseFloat(getComputedStyle(message).height, 10) + 30 + 'px';
```


CSS Custom Properties (CSS Variables):

```js
document.documentElement.style.setProperty('--color-primary', '#FF0000');
```


Attributes:

```js Reading
const logo = document.querySelector('.nav__logo');

console.log(logo.src);
console.log(logo.alt);
console.log(logo.className);

logo.getAttribute('alt');
```

```js Setting
logo.alt = 'Beautiful Miinimalist Logo'


logo.setAttribute('alt', 'Bankist logo');
```



Data Attributes:

We can specify data attributes on html elements and then access them as a property through . notation in JS.

```html
<img
  src="img/logo.png"
  alt="Bankist logo"
  class="nav__logo"
  id="logo"
  data-version-number="3.0"
/>
```

The value is then located in the dataset object under the name we gave it but camelCased.
```js
console.log(logo.dataset.versionNumber);
// 3.0
```


# Scrolling


Old School ways:

We can use the getBoundingClient to get information about coordinates, scrolling and dimensions the viewport

```js
const btnScrollTo = document.querySelector('.btn--scroll-to');
const section1 = document.querySelector('#section--1');


btnScrollTo.addEventListener('click',function (e) {
  const s1coords = section1.getBoundingClientRect();
  console.log(s1coords);
  console.log(e.target.getBoundingClientRect);
});
// DOMRect
// bottom: 2093.199951171875
// height: 1567.199951171875
// left: 0
// right: 960
// top: 526
// width: 960
// x: 0
// y: 526
```

If we want to scroll to a position on the page we need to add how much we've scrolled with the page offset otherwise it creates a jumpy effect when clicking to scroll at different point of the page because the element will be at different heights from the top of the vierwport.

```js
window.scrollTo(s1coords.left + window.pageXOffset, s1coords.top + window.pageYOffset);
```


We can also pass the scrollTo method an object to specify the behavior.

```js
window.scrollTo({
    left: s1coords.left + window.pageXOffset, 
    top: s1coords.top + window.pageYOffset,
    behavior: 'smooth',
  });
```


Modern Way (Not supported in all browsers):


```js
section1.scrollIntoView({behavior:  'smooth'});
```


# Event Propagation: Bubbling & Capturing

Event listeners by default listen only to the bubbling phase.


Say we have some HTML elements as follows:


```html
<html>
  <body>
    <section>
      <p>
        <a>link</a>
      </p>
    </section>
  </body>
</html>
```

Say a click happens on the link this is what happens.

Capturing Phase:

The click event is created and is generated at the root of the document at the top of the DOM tree. The event travels down the tree and passes through every single parent element of the target element (link) until it hits the target.

document -> html -> body -> section -> p -> a


Target Phase:

Once the event hits the target the target phase begins. This is where events can be handled right at the target.

Bubbling Phase:

When the event phase has finished and the event has been handled then the event bubbles all the way back up to the root of the document, passing through all parent elements.

As the event travels it is as if the event has happened in each parent element and can be caught and handled on parent elements. 

This comes in handy especially when we don't know how many children a parent will have Ex.) a list that is being updated( adding & deleting items)
Then we can just make the parent responsible for the event because we know it will always be there.

Most events capture and bubble but there are some that only happen directly on the target.


All of this is called event propagation.


```js Easy way to visualize in practice
const randomInt = (min,max) => {
  return Math.floor(Math.random() * (max - min + 1) + min);
}
const randomColor = () => `rgb(${randomInt(0, 255)},${randomInt(0, 255)},${randomInt(0, 255)})`;

// Create a target element (link) with a parent element and a parent element for that parent.
// Then add an event listener of click on each of the 3 elements calling the randomColor function to set the backgroundColor.
```
The event target is not the element to which the event listener is attached, but where the event first occurred. So in the above example if you console.log the e.target even when the event occurs at the highest level they will all log the link that was clicked.


The event current target is where the event handler is attached. So the parent elements will log themselves. 

```js
e.currentTarget === this
// true
```

We can also stop event propagation for hitting the parent elements. This isn't used very often.

```js
e.stopPropagation();
```

If we need to listen to the event coming down on the capture phase we pass a 3rd parameter to the addEventListener and set it to true as the default is false.

Capturing is rarely used these days, mostly just bubbling.


# Event Delegation - Page Scrolling


```html
<!-- Navigation Code -->
<li class="nav__item">
  <a class="nav__link" href="#section--1">Features</a>
</li>

...etc

<!-- Section Code -->
<section class="section" id="section--1">
      <div class="section__title">
        <h2 class="section__description">Features</h2>
        <h3 class="section__header">
          Everything you need in a modern bank and more.
        </h3>
      </div>

...etc
```

Here add the corresponding section name to the href in the anchor tag so in the JS we can easily grab it and turn it into an id then scroll it into view when clicked.


```js
document.querySelectorAll('.nav__link').forEach(function(el) {
  el.addEventListener('click', function(e) {
    e.preventDefault();
    const id = this.getAttribute('href');
    console.log(id);
    document.querySelector(id).scrollIntoView({behavior:  'smooth'});
  });
});
```

However this is duplicating the exact same function for however many elements we need which when getting over the size of a couple will begin to impact performance.

So we need to use Event Delegation...

There are basically 2 steps to implementing Event Delegation:

1. 
We put the event listener on a common parent of all the elements we are interested in.

2. 
In the event listener determine which child element omitted the event


```js
document.querySelector('.nav__links').addEventListener('click', function(e) {
  e.preventDefault();

  if(e.target.classList.contains('nav__link')) {
    const id = e.target.getAttribute('href');
    document.querySelector(id).scrollIntoView({behavior:  'smooth'});
  }
  
});
```
To summarize, we add an event listener to the parent of all the links and because of event propagation we have access to the e.target which is what was actually clicked on. Then in the if statement we check if the target contains the same class as the elements we want and if so get their href that matches the corresponding section id so we can use it to smooth scroll into view on click.


# DOM Traversal

In the DOM we can select elements relative to a certain element.

Selecting children:

```js
const h1 = document.querySelector('h1');

// Going down: Children

console.log(h1.querySelectorAll('.highglight'));
// NodeList(2) [span.highlight, span.highlight]

// This selects all ELEMENT children no matter how deeply nested under the h1

console.log(h1.childNodes);
// NodeList(6)
// 0: text
// 1: comment
// 2: text
// 3: span.highlight
// 4: text
// 5: br
// 6: text

// This shows EVERY TYPE of child node under the h1 (this is not used that much)

console.log(h1.children);
// HTMLCollection(3)
// 1: span.highlight
// 2: br
// 3: span.highlight

// Returns a live HTML Collection and only direct children of the h1

h1.firstElementChild.style.color = 'white';
h1.lasttElementChild.style.color = 'orangered';
// We can set properties when traversing the DOM


// Going up: Parents

console.log(h1.parentNode);
console.log(h1.parentElement);


// Finding a parent no matter how far away in the DOM trees
h1.closest('.header').style.background = 'var(--gradient-secondary)';


// Going sideways: Siblings
// In JS we can only access direct siblings (previous and next)

// For elements
console.log(h1.previousElementSibling);
// null
console.log(h1.nextElementSibling);
// <h4>A simpler banking experience</h4>

// for nodes
console.log(h1.previousSibling);
console.log(h1.nextSibling);


// If we want to traverse efficiently across siblings traverse to the parent and then in

// It is common to convert node lists & HTML collections to arrays or different data types to work with them

[...h1.parentElement.children].forEach(function(el) {
  if(el !== h1) el.style.transfor, = 'scale(0.5)';
});
```


# Tabbed Components


```js
tabsContainer.addEventListener('click', function(e) {
  const clicked = e.target.closest('.operations__tab');
  console.log(clicked);
});
```
We can use the closest method when we have nested elements to avoid unwanted issues in the event propagation. Here without it we have a span element inside the button class wrapping the number on the button. But if we are trying to click on the button but click the span then we are dealing with different elements when trying to traverse. We cant just go e.target.parentElement, because when we click the span the parent is the button and when we click the button the parent is a different element. So this helps whichever is clicked find a common parent.

```js
// Guard clause
  if(!clicked) return;
```

In our function we add a guard clause because we could still click outside one of the buttons but inside the tabsContainers that we're listening to, and if there is no parent of the button/span we get a null TypeError.


```js Final Code for reference
tabsContainer.addEventListener('click', function(e) {
  const clicked = e.target.closest('.operations__tab');

  // Guard Clause
  if(!clicked) return;


  // Clear/Remove Clases
  tabs.forEach(t => t.classList.remove('operations__tab--active'));
  tabsContent.forEach(c => c.classList.remove('operations__content--active'));
  
  // Active Tab
  clicked.classList.add('operations__tab--active');

  // Activate Content Area
  document.querySelector(`.operations__content--${clicked.dataset.tab}`).classList.add('operations__content--active');
});
```


# Passing Arguments To Event Handlers


```js

const handleHover = function(e, opacity) {
  if(e.target.classList.contains('nav__link')) {
    const link = e.target;
    const siblings = link.closest('.nav').querySelectorAll('.nav__link');
    const logo = link.closest('.nav').querySelector('img');

    siblings.forEach(el => {
      if(el !==link) el.style.opacity = opacity;
      logo.style.opacity = opacity;
    });
  }
}

nav.addEventListener('mouseover', function(e) {
  handleHover(e, 0.5);
});

nav.addEventListener('mouseout', function(e) {
handleHover(e, 1);
});
```
Here we cannot pass the handleHover directly to the event listeners as we need to pass it parameters and that would result in a function call and our functions don't return anything and would result in undefined being passed as a callback which the add event listener weill not accept. So we use an anonymous function then call our function with the required arguments. 

However we can do better using the .bind method.

```js

const handleHover = function(e) {
  if(e.target.classList.contains('nav__link')) {
    const link = e.target;
    const siblings = link.closest('.nav').querySelectorAll('.nav__link');
    const logo = link.closest('.nav').querySelector('img');

    siblings.forEach(el => {
      if(el !==link) el.style.opacity = this;
      logo.style.opacity = this;
    });
  }
}

nav.addEventListener('mouseover', handleHover.bind(0.5));

nav.addEventListener('mouseout', handleHover.bind(1));
```

A handler callback function can only take one argument which is the event. so we bind the this keyword of the handler function to the value we need as a work around to get an extra value into the function. If we need even more values we could pass an array or even an object instead of just a single value. (A bit of hack or work around)

See line 2783 for the .bind keyword notes.

"Bind does not immediately call the function. Instead it returns a new function where the this keyword is bound. Its set to whatever value we pass into bind."

So because the bind method returns another function and does not actually call a function the add event listener will accept it as a callback.

Pretty fuckin' slick.


# Sticky Nav

```js
const initialCoords = section1.getBoundingClientRect();

window.addEventListener('scroll', function() {
  console.log(window.scrollY);

  if(window.scrollY > initialCoords.top) nav.classList.add('sticky') 
  else nav.classList.remove('sticky');
});
```

Above works but is really bad for performance because when your using the scroll event in th add event listener it fires and listens all the time because of the scrolling. 

Instead we use the Intersection Observer API


# Intersection Observer API

This API allows our code to observe changes to the way that a certain target element intersects another element, or the way it intersects the viewport.

How does it work:


```js
// Intersection Observer
// Takes a callback function and an object of options

const obsCallback = function (entries, observer) {
  entries.forEach(entry => console.log(entry))
};

const obsOptions = {
  root: null,
  threshold: [0, 0.2],
}

const observer = new IntersectionObserver(obsCallback, obsOptions);

observer.observe(section1);




// In the console

// IntersectionObserverEntry
// boundingClientRect: DOMRect { x: 0, y: 404, width: 960, … }
// intersectionRatio: 0.10017866258295048
// intersectionRect: DOMRect { x: 0, y: 404, width: 960, … }
// isIntersecting: true
// rootBounds: DOMRect { x: 0, y: 0, width: 960, … }
// target: <section id="section--1" class="section">
// time: 5874.48
```

The options control the circumstances under which the callback is invoked. It includes the root, rootMargin and threshold. The root defaults to the browser viewport if not specified or if null, otherwise it is the specified element that is used for checking visibility of the target. rootMargin is like an offset and is specified only in pixels. The threshold indicates what percentage of the targets visibility the callback should be executed at NOT MATTER SCROLLING UP OR DOWN (Ex.) Threshold of 0.1 & scrolling only down, it will fire when 10% of the target has entered the viewport AND when there is 10% remaining in the viewport ) and can also be an array of values.


The observer callback takes 2 arguments. Entries & observer object itself.


```js
const header = document.querySelector('.header');

const navOffset = - nav.offsetHeight + 'px';

const stickyNav = function(entries) {
  const [entry] = entries;
  console.log(entry);
  if(!entry.isIntersecting) nav.classList.add('sticky')
  else nav.classList.remove('sticky');
}

const headerObserver = new IntersectionObserver(stickyNav, {
  root: null,
  threshold: 0,
  rootMargin: `${navOffset}`,
});

headerObserver.observe(header);
```



# Reveal Elements On Scroll

```js
const allSections = document.querySelectorAll('.section');

const revealSection = function(entries, observer) {
  const [entry] = entries;
  console.log(entry);

  if(!entry.isIntersecting) return;
  entry.target.classList.remove('section--hidden');
  observer.unobserve(entry.target);
}

const sectionObserver = new IntersectionObserver(revealSection, {
  root: null,
  threshold: 0.15
});

allSections.forEach(function(section) {
  sectionObserver.observe(section);
  section.classList.add('section--hidden');
});
```

Again here we use the IntersectionObserver. We store all sections in the all section variable and loop over them, observing each section and hiding them off the start. Then we define out InterSectionObserver and then define our callback where we destructure each entry from the entries that we told the observer to observe in the forEach. Then we use a guard clause to return if not intersecting and then show each section and finally remove the observer to enhance performance and stop the even from firing even after the animation has already been performed.



# Lazy Loading

Images have the biggest impact on performance. So we can use lazy loading to only load the images when we need them.


```html
<div class="features">
        <img
          src="img/digital-lazy.jpg"
          data-src="img/digital.jpg"
          alt="Computer"
          class="features__img lazy-img"
        />
...etc
```

```js
const imgTargets = document.querySelectorAll('img[data-src]');

const loadImg = function(entries, observer) {
  const [entry] = entries;

  if(!entry.isIntersecting) return;

  // Replace src attr with data-src
  entry.target.src = entry.target.dataset.src;
  // entry.target.classList.remove('lazy-img');

  entry.target.addEventListener('load', function () {
  entry.target.classList.remove('lazy-img');
  });

  observer.unobserve(entry.target);

};

const imgObserver = new IntersectionObserver(loadImg, {
  root: null,
  threshold: 0,
  rootMargin: '200px'
})

imgTargets.forEach(img => imgObserver.observe(img));
```

So we set up the html with a very tiny img that is blurred our with CSS to keep our file size down. Then we use the IntersectionObserver to replace the low res image with the high res one, only removing the blur when the high res img is actually loaded with an event listener on the load event. Otherwise users with slow connections will have the blur removed and will be viewing the low res img while waiting for the high res one to load. We also use the rootMargin to ensure that these images are being lazy loaded a little bit before the user scrolls down as to decrease the amount of time the image is blurry. We don't really need users to know that we are lazy loading.



# Lifecycle DOM Events

Lifecycle means from when the page is first accessed until the user leaves it.


1. DOM Content Loaded

- This event is fired by the document as soon as the HTML is completely parsed which means it has been downloaded and converted to the DOM 
tree. 

- All script must be downloaded and executed before the DOM Content Loaded event can happen.

- It does not wait for other extrenal resources such as images, only HTML and JS need to be loaded

```js
document.addEventListener('DOMContentLoaded', function(e) {
  console.log(e);
});

// DOMContentLoaded
// bubbles: true
// cancelBubble: false
// cancelable: false
// composed: false
// currentTarget: null
// defaultPrevented: false
// eventPhase: 0
// explicitOriginalTarget: HTMLDocument http://127.0.0.1:5500/13-Advanced-DOM-Bankist/starter/index.html#section--2
// isTrusted: true
// originalTarget: HTMLDocument http://127.0.0.1:5500/13-Advanced-DOM-Bankist/starter/index.html#section--2
// returnValue: true
// srcElement: HTMLDocument http://127.0.0.1:5500/13-Advanced-DOM-Bankist/starter/index.html#section--2
// target: HTMLDocument http://127.0.0.1:5500/13-Advanced-DOM-Bankist/starter/index.html#section--2
// timeStamp: 636
// type: "DOMContentLoaded"
```

We can then view this in the network tab (at a slower rate if needed)

So with our script tag at the bottom of the HTML we don't need to listen to this event.


2. Load EVent

- The load event is fired when the HTML AND all external resources like images are loaded. 

```js
window.addEventListener('load', function(e) {
  console.log(e);
});

// load
// bubbles: false
// cancelBubble: false
// cancelable: false
// composed: false
// currentTarget: null
// defaultPrevented: false
// eventPhase: 0
// explicitOriginalTarget: HTMLDocument http://127.0.0.1:5500/13-Advanced-DOM-Bankist/starter/index.html#section--2
// isTrusted: true
// originalTarget: HTMLDocument http://127.0.0.1:5500/13-Advanced-DOM-Bankist/starter/index.html#section--2
// returnValue: true
// srcElement: HTMLDocument http://127.0.0.1:5500/13-Advanced-DOM-Bankist/starter/index.html#section--2
// target: HTMLDocument http://127.0.0.1:5500/13-Advanced-DOM-Bankist/starter/index.html#section--2
// timeStamp: 1069
// type: "load"
```

We can also observe this in the network tab and again see how fast things are loading and how big files are.


3. Before Unload

- This event is created immediately before a user is about to leave a page.

Ex.) When the user clicks the x button to leave the page

- To stop it we can call prevent default

- This is the event we can use to ask users if they are sure they want to leave the page

```js
window.addEventListener('beforeunload', function(e) {
  e.preventDefault();
  console.log(e);
  e.returnValue = '';
});
```

The pop up that asks if they are sure they want to leave is NOT customizable as previous developers abused it.

A messsage like this can be annoying, so only use it if there are things workj that user has done that they may not want to have erased by leaving the page.


# Efficient Script Loading: Defer & Async

We can put our script tags in either the head or the body end...and this is what it looks like in the different scenarios over time.

REGULAR:

Head:

- HTML beigns to parse and the DOM tree begins to be built
built
- The script tag is then found, the HTML is paused until the script tag is exectued
- HTML finsishes parsing after script tag is executed
- DOM Content Loaded Event is fired

Never include the script in the head.

Body:

- HTML is parsed
- Script is found, fetched & exectured
- DOM Content Loaded EVent is fired

Not the most optimied because the script tage could have been found while the HTML was still being parsed.

---
* Keep in mind Async & Defer will never be put in the body end because the HTML will have already finished parsing so it makes no sense they would ever go there.

ASYNC:

Head:

- Script is loaded at the same time that the HTML is being parsed and when executing the HTML is stopped until the script executes and then resumes after the script execution.
- DOM Content Loaded EVent is fired

Even though the pausing of the HTML seems not idela this is still actually faster then just including the script tage at the body end.


---

DEFER:

Head:

- Script is loaded at the same time that the HTML is being parsed and only executed after the HTML is finished
- DOM Content Loaded EVent is fired


---



Regular vs Async vs Defer

* These use cases assume Regular at end of body and both Async & Defer in head as discussed previously.


Regular:

- Scripts are fetched and executed after HTML is completely parsed
- Use if you need to support old browsers (Legacy browsers don't support async & defer)


Async:

- Scripts are fetch asynchronously and executed Immediately
- Usually the DOMContentLoaded event waits for all scripts to execute, except for async scripts. So DOMContentLoaed does not wait for an async script and if there is a large script file may fire before the script is event fetched and ran.
- Scripts are not guaranteed to execute in order, whichever script comes in first is executed first
- Use for any 3rd party scripts that order doesn't matter Ex.) Analytic scripts


Defer:

- Scripts are fetched asynchronously and executed after the HTML is completely parsed

- DOMContentLoaded event fires after the defer script is executed

- Scripts are executed in order

- THIS IS THE BEST OVERALL SOLUTION! USE FOR YOUR OWN SCRIPTS, AND WHEN ORDER MATTERS Ex.) Including a library that your scripts depend on.



```js
<script defer src="script.js"></script>
<script async src="script.js"></script>
```

In the network tab we can view the time it takes for the DOMContentLoaded event to fire and compare the different scenarios.


---
# Object Oriented Programming (OOP)
---

- OOP is a paradigm (style of writing and organizing) that is based on the concept of objects.

- It uses objects to model or describe real world or abstract features.

- By using objects we pack DATA AND the corresponding BEHAVIOUR (methods) into one block.

- In OOP objects are self-contained pieces/blocks of code

- Objects are building block of applications & interact with one another

- Interactions happen through an API: methods that the code outside the object can access and use to communicate with the object

- OOP was developed with the goal of organizing code, to make it more flexible & easier to maintain (avoid "spaghetti code")



Classes & Instances (Traditional OOP):

A class is a blueprint used to create new objects based on rules described in the class.

Objects created from the class are called instances and we can created as many as we need with different data in them but share the same functionality. Creating a new instance is called instantiation.

How to design classes (model real-world data into classes)..

4 Main Principles:

1. Abstraction

- Ignoring or hiding away details that don't matter, allowing us to get an overview perspective of the thing we're implementing, instead of messing with details that don't really matter to our implementation.
Ex.) Designing all the features of an iphone, but the user doesn't need to know how every little feature works it just works in an easy manner

2. Encapsulation

- Keeping properties and methods private inside the class, so they are not accessible from outside the class. Some methods can be exposed as a public interface (API)

3. Inheritance

- Makes all properties and methods of a certain class available to a child classs, forming a hierachical relationship between classes. This allows for reuse of common logic and to model real-world relationships
- Child classes "extend" parent classes and then can have their own individual properties and methods

4. Polymorphism

- A child class can overwrite a method it inherited from a parent class (it is more complex than this, but this is a short summary)


# OOP In JavaScript

Prototypes:

All objects have a prototype and are linked to a prototype object. The prototype object contains methods that all objects can access and use. This behaviour is called prototypal inheritance. This inheritance is different from the previously discussed inheritance. That was one class inheriting from another class, in this way it is basically an instance inheriting from a class.

- Objects are linked to a prototype object

- Prototypal inheritance: The prototype contains methods that are accessible to all objects linked to that prototype

- Objects delegate behaviour (methods) to the linked prototype object.

In classical OOP the behaviour (methods) are copied from the class to all instances.


How do we actually create prototypes?
And how do we link objects to prototypes?
How can we create new objects, without having classes?

3 Ways to implement prototypal inheritance: 

1. Constructor functions
- Technique that was adopted as a standard to create objects from a function
- This is how built-in objects like Arrays, Maps or Sets are actually implemented

2. ES6 Classes
- Modern alternative to constructor function syntax
- Syntactic sugar: behing the scenes, ES6 classes work exactly like constructor functions
- ES6 classes do not behave like classes in classical OOP

3. Object.create()
- Easiest most straightforward way of linking and object to a prototype object

All 4 main principles of OOP are important and valid with prototypal inheritance.


# Constructor Functions & The new Operator

The convention in JS is that all constructor functions are named with the first letter capitalized.

Arrow functions will not work as a constructor function as it does not have a this keyword. Only function declarations and function expressions.

We call the constructor using the new keyword and store it in a variable.

Behind the scenes 4 things happen when using the new keyword to call a constructor function.

1. A new empty object is created
2. The function is called with the this keyword being set to the newly created object in the execution conext
3. The new object is linked to a prototype
4. The function automatically returns the empty object

```js
const Person = function(firstName, birthYear) {
  // Instance properties
  this.firstName = firstName;
  this.birthYear = birthYear;
}

const jonas = new Person('Jonas', 1991);
console.log(jonas);
// Object { firstName: "Jonas", birthYear: 1991 }
```
Now we can use this constructor to create as many objects as we want.

```js
const matilda = new Person('Matilda', 2017);
const jack = new Person('Jack', 1975);
```

There are not actual classes in JS. The constructor function is used to mimick classes and therefore when we create objects using the constructor function those objects are said to be instances of the constructor.
Ex.) jonas, matilda & jack are instances of the Person constructor.

```js
console.log(jonas instanceof Person);
// true
```

Methods:

```js
const Person = function(firstName, birthYear) {
  // Instance properties
  this.firstName = firstName;
  this.birthYear = birthYear;

  // Never create a method inside a constructor function like this
  this.calcAge = function() {
    console.log(2037 - this.birthYear);
  }
}
```

We don't create methods on constructor functions because everysingle instance would carry around that method and would be bad for performance. Instead we use prototypes and prototypal inheritance...


# Prototypes

Each and every function automatically has a property called prototype. Every object created by a certain constructor function will get access to all the methods and properties that we define on the constructors prototype property.


```js

const Person = function(firstName, birthYear) {
  // Instance properties
  this.firstName = firstName;
  this.birthYear = birthYear;
}
const jonas = new Person('Jonas', 1991);

// Setting the prototype method
Person.prototype.calcAge = function() {
    console.log(2037 - this.birthYear);
  };

jonas.calcAge();
// 46

console.log(jonas);
// Object { firstName: "Jonas", birthYear: 1991 }

console.log(jonas.__proto___);
// {…}
// calcAge: function calcAge()
// constructor: function Person(firstName, birthYear)
// <prototype>: {…
// We can see above the prototype of jonas and we can see the calcAge function
// The prototype of the jonas object is essentially the same as the prototype property of the constructor function

console.log(jonas.__proto__ === Person.prototype);
//true
```
Here we can see that the jonas object does not have the calcAge function in it. But we still have access to it due to prototypal inheritance. And now there is only one copy of the function, saving memory. The this keyword is also set to the object calling the method. So everything works.

* Person.prototype is not the prototype of Person. It is used as the prototype of all instances of Person. This is an important distinction.

```js
console.log(Person.prototype.isPrototypeOf(jonas));
// true
console.log(Person.prototype.isPrototypeOf(Person));
// false
```

The confusion is due to bad naming. A better name could have been used such as .prototypeOfInstances or .prototypeOfLinkedObjects

We can also set properties on the prototype, not just methods.

```js
Person.prototype.species = 'Homo Sapiens';
console.log(jonas);
// {…}
// birthYear: 1991
// firstName: "Jonas"
// <prototype>: {…}
//    calcAge: function calcAge()
//    constructor: function Person      (firstName, birthYear)
//    species: "Homo Sapiens"
//    <prototype>: {…

console.log(Person);
// Person(firstName, birthYear)
// arguments: null
// caller: null
// length: 2
// name: "Person"
// prototype: {…}
//    calcAge: function calcAge()
//    constructor: function Person(firstName, birthYear)
//    species: "Homo Sapiens"
//    <prototype>: Object { … }
//    <prototype>: ()

console.log(jonas.hasOwnProperty('firstName'));
// true
console.log(jonas.hasOwnProperty('species'));
// false
```


# Prototypal Inheritance & The Prototype Chain

The constructor has a prototype property that is actually the prototype of all of the instances of that constructor and not the prototype of the constructor itself. We can define methods and properties on the prototype.

Behind the scenes 4 things happen when using the new keyword to call a constructor function.

1. A new empty object is created
2. The function is called with the this keyword being set to the newly created object in the execution conext
3. The new object is linked to a prototype
4. The function automatically returns the empty object

This is how it works with function constructors and ES6 classes but NOT with Object.create()

If a property or method is not found on that object JS will check the prototype and use the property or method from there. We say the object delegated thast property or method to its prototype.

The ability for an object to look to its prototype for a method or property or if not found goes up to the next prototype is called the prototype chain.

The top of the scope chain is null.


# Prototypal Inheritance On Built In Objects

```js
const arr = [3, 6, 4, 5, 6, 9, 3];
console.log(arr.__proto__);
// Shows all built-in array methods
console.log(arr.__proto__ === Array.prototype);
// true

console.log(arr.__proto__.__proto__);
// Object prototype
```

It is possible to change the prototype of the built-in object but it shouldn't be done. If new versions of JS try to add new methods with the same name it will cause applications to break.

Secondly on a team this would become a free for all and would cause major bugs.



# ES6 Classes

Classes in JS implement prototypal inheritance but allow people coming from other programming languages to understand it easier.

```js Class Expression
// Class Expression
class Person {

}

// Class Declaration
const Person = class {
  constructor(firstName, birthYear) {
    this.firstName = firstName;
    this.birthYear = birthYear;
  }

  calcAge() {
    console.log(2037 - this.birthYear);
  }
}

const jessica = new Person('jessica', 1996);
console.log(jessica);
// Object { firstName: "jessica", birthYear: 1996 }
```

Any properties or methods written INSIDE the constructor will be on every instance of that class. Every property or method written OUTSIDE the constructor are automatically put on the prototype property.


Important differences with classes.

1. Classes are NOT hoisted even as class declarations (we can't use them before they are declared in the code)

2. Classes are also first class citizens (we can pass them into functions and return them from functions)

3. Classes are executed in strict mode

Constructor functions are not old or deprecated.



# Setters & Getters

Every object can have setter & getters which get & set a value.

```js
const account = {
  owner: 'jonas',
  movements: [200, 450, -400, 3000, -650, -130, 70, 1300],

  get latest() {
    return this.movements.slice(-1).pop();
  },
  set latest(mov) {
    this.movement.push(mov);
  }
};

console.log(account.latest);

// account.latest(50);
// Calling a method

account.latest = 50;
// Using a setter
```
Getters and setters allow us to access functions as if they were properties instead of using parentheses to call a method. Both must be prepended with their corresponding keyword (get or set) and setters require one single paramater.

```js
// Getters and setters with classes work the same way
const Person = class {
  constructor(firstName, birthYear) {
    this.firstName = firstName;
    this.birthYear = birthYear;
  }

  calcAge() {
    console.log(2037 - this.birthYear);
  }

  get age() {
    return 2037 - this.birthYear;
  }
}

const jessica = new Person('jessica', 1996);
console.log(jessica.age)
// 41
// Sets this as a property on the jessica prototype now as well

// They work pretty much the exact same as any regular method
```


```js
const Person = class {
  constructor(fullName, birthYear) {
    this.fullName = fullName;
    this.birthYear = birthYear;
  }

  calcAge() {
    console.log(2037 - this.birthYear);
  }

  get age() {
    return 2037 - this.birthYear;
  }

  // Setting a property that already exists...

  // This property already exists from the constructor and since both are trying to set it creates an error. So we need to add an underscore to the variable.
  set fullName(name) {
    if(name.includes(' ')) this.fullName = name;
    else alert(`${name} is not a full name!`)
  }
  ---
  // Add an underscore
  set fullName(name) {
    if(name.includes(' ')) this._fullName = name;
    else alert(`${name} is not a full name!`)
  }

  // Then the getter need the underscore as well
  get fullName() {
    return this._fullName;
  }

}

const jessica = new Person('jessica davis', 1996);


// After adding the underscore, we can call it as we normally would to get the same result, but in the class it is now stored with an underscore

console.log(jessica.fullName);
// jessica davis
```

The getters and setter can be useful some times. For example above it allows for validation for the fullName of the class.


# Static Methods

Static methods are attached to the top constructor and not in the prototype chain and such are not inherited by any instances of the class or constructor.

They are more like helper functions for that namespace (data type) or constructor function or class.

```js
Array.from(document.querySelector('h1');)
// []

[1, 2, 3].from();
// Uncaught TypeError, [1, 2, 3].from() is not valid function.
```

We can set them for our own constructors and classes.

Constructor:

```js
Person.hey = function() {
  console.log('Hi there');
  console.log(this);
}
Person.hey();
```

Class:

```js
const Person = class {
  constructor(firstName, birthYear) {
    this.firstName = firstName;
    this.birthYear = birthYear;
  }
  // Instance Methods
  calcAge() {
    console.log(2037 - this.birthYear);
  }

  get age() {
    return 2037 - this.birthYear;
  }
  // Static Methods
  static hey() {
    console.log('Hi there');
    console.log(this);
  }
}
```


# Object.create()


With object.create there is still prototypal inheritance but there is no prototype properties, no constructor function and no new operator. We can use object.create to manually set the prototype of an object to any other object that we want. 


```js
const PersonPrototype = {
  calcAge() {
    console.log(2037 - this.birthYear);
  },
};


const steven = Object.create(PersonPrototype);
console.log(steven);
// {}
// <prototype>: Object { calcAge: calcAge() }
//
```

Whereas constructor functions automatically will set instances of it to a prototype, with Object.create we manually set what prototype of what object we want it to have.



# Inheritance Between "Classes": Constructor Functions



```js
const Person = function(firstName, birthYear) {
  this.firstName = firstName;
  this.birthYear = birthYear;
};

Person.prototype.calcAge = function () {
  console.log(2037 - this.birthYear)
};

const Student = function (firstName, birthYear, course) {
  // This is not the best because if the Person properties ever changed names then it would break
  // this.firstName = firstName;
  // this.birthYear = birthYear;

  // This doesn't work as this is a regular function call and the this variable is set to undefined in regular function calls and a function constructor needs the new keyword
  // Person(firstName, birthYear);

  // So we use the call method to set the this keyword to this constructor
  Person.call(this, firstName, birthYear)

  this.course = course;
};

// We need to add this chain here because Object.create returns an empty object and would overwrite any properties or methods we had previously defined on the Student.prototype
// So to link prototypes...
Student.prototype = Object.create(Person.prototype);

// We cannot do the following as it would break the prototype chain making student & person effectively same object
// Student.prototype = Person.prototype;


Student.prototype.introduce = function () {
  console.log(`My name is ${this.firstName} and I study ${this.course}`);
};

const mike = new Student('Mike', 2020, 'Comp Sci');
mike.introduce();
mike.calcAge();
// The mike.calAge() is found by looking up the prototype chain until it finds it on the person.prototype
```


# Inheritance Between "Classes": ES6 Classes


```js
const Person = class {
  constructor(firstName, birthYear) {
    this.firstName = firstName;
    this.birthYear = birthYear;
  }
  // Instance Methods
  calcAge() {
    console.log(2037 - this.birthYear);
  }

  get age() {
    return 2037 - this.birthYear;
  }
  // Static Methods
  static hey() {
    console.log('Hi there');
    console.log(this);
  }
}

class Student extends Person {
  constructor(firsName, birthYear, course) {
    super(firstName, birthYear)
    // The super(parent class constructor) always needs to happen first because it sets the this keyword
    this.course = course;
  }
}


const martha = new Student('martha', 2012, 'Comp Sci');
```

If you dont need any new properties or methods in the child class you can omit writing the above constructor function and still access the parent constructor.


```js
class Student extends Person {
  
}

const martha = new Student('martha', 2012);

console.log(martha);
// Student { firstName: "martha", birthYear: 2012}
marth.calcAge();
// 25
```


Overwriting methods of parent constructors: (Polymorphism)

```js
class Student extends Person {
  constructor(firsName, birthYear, course) {
    super(firstName, birthYear)
    // The super(parent class constructor) always needs to happen first because it sets the this keyword
    this.course = course;
  }

  calcAge() {
    console.log(`This function overwrites the Person calcAge() function. This is polymorphism.`)
  }
}
martha.calcAge();
// This function overwrites the Person calcAge() function. This is polymorphism.
```


# Inheritance Between "Classes": Object.create()

```js
const PersonProto = {
  calcAge() {
    console.log(2037 - this.birthYear);
  },

  init(firstName, birthYear) {
    this.firstName = firstName;
    this.birthYear = birthYear;
  },
};

const steven = Object.create(PersonProto);

const StudentProto = Object.create(PersonProto);
StudentProto.init = function (firstName, birthYear, course) {
  PersonProto.init.call(this, firstName, birthYear);
  this.course = course;
};

StudentProto.introduce = function () {
  console.log(`My name is ${this.fullName} and I study ${this.course}`);
};

const jay = Object.create(StudentProto);
jay.init('Jay', 2010, 'Compuetr Science');
jay.introduce();
jay.calcAge();
```


# Another Class Example


```js
class Account {
  constructor(owner, currency, pin, movements) {
    this.owner = owner;
    this.currency = currency;
    this.pin = pin;
    this.movements = movements;
  }
}

acc1 = new Account('Jonas', 'Eur', 1111, []);
console.log(acc1);
```

We don't need to pass an empty array as an argument every time we are making a new account or specify the parameter in the constructor function. Instead we can specify it directly in the instance. We can also execute any code we want in that instance(See the console.log).

```js
class Account {
  constructor(owner, currency, pin) {
    this.owner = owner;
    this.currency = currency;
    this.pin = pin;
    this.movements = [];
    this.locale = navigator.language;

    console.log(`Thanks for opening an account, ${owner}`);
  }
}

acc1 = new Account('Jonas', 'Eur', 1111);
console.log(acc1);
// Thanks for opening an account, Jonas
// Object { owner: "Jonas", currency: "Eur", pin: 1111, movements: [], locale: "en-CA" }


// This should not be done, a method to interact with the properties should be created to avoid bugs as the app grows
// acc1.movements.push(250);
// acc1.movements.push(-140);

// This is best
class Account {
  constructor(owner, currency, pin) {
    this.owner = owner;
    this.currency = currency;
    this.pin = pin;
    this.movements = [];
    this.locale = navigator.language;

    console.log(`Thanks for opening an account, ${owner}`);
  }

  // Public Interface (API)
  deposit(val) {
    this.movements.push(val);
  }

  withdraw(val) {
    this.deposit(-val);
  }
}
acc1 = new Account('Jonas', 'Eur', 1111);
acc1.deposit(250);
acc1.withdraw(140);
```



# Encapsulation: Protected Properties & Methods

There are 2 main reasons why we need data encapsulation and privacy:

1. We need to prevent code outside a class to accidentally manipulate data inside the class

2. When we expose only a small interface, then we can change all the other internal methods with more confidence

JS Classes do not yet support real data privacy & encapsulation.

We want to protect the movements array because its mission critical data.

Adding an underscore lets other developers know its a protected property and should not be accessed outside the class but is just a naming convention.

```js
class Account {
  constructor(owner, currency, pin) {
    this.owner = owner;
    this.currency = currency;
    this._pin = pin;
    // Protected
    this._movements = [];
    this.locale = navigator.language;

    console.log(`Thanks for opening an account, ${owner}`);
  }

  // Public Interface (API)
  getMovements() {
    return this.movements;
  }

  deposit(val) {
    this._movements.push(val);
  }

  withdraw(val) {
    this.deposit(-val);
  }

  _approveLoan(val) {
    return true;
  }

  requestLoan(val) {
    if(this._approveLoan(val)) {
      this.deposit(val);
      console.log('Loan approved');
    }
  }
}
acc1 = new Account('Jonas', 'Eur', 1111);
acc1.deposit(250);
acc1.withdraw(140);
```

# Encapsulation: Priavte Class Fields & Methods


This is a proposal currently at Stage 3 so is very likely will move to Stage 4 and become part of the language

In traditional OOP programming languages properties are called fields. More and more JS is moving toward that Classes aren't just syntactic sugar.

As long as you understand prototypal inheritance and constructor functions then there should be no issue.

There are 8 different kinds of fields & methods in this proposal but we will only focus on 4:

1. Public Fields (instances)
- A field is a property that will be on all instances so we could call them public instance fields
- In our example these are the movements and navigator as we explicitly set them
- They are not on the prototype
- Also referenceable by the this keyword

2. Private Fields (instances)
- Makes it so properties ar enot accessible from the outside
- Defined by prepending the # symbol
- Public Methods can still access Private Fields
- They are not on the prototype

3. Public Methods
- This is how the methods already are in the public interface

4. Private Methods
- Useful to hide implementation details from the outside
- Not yet available
- Defined by prepending the # symbol

There is also the static version of these but we wont go through these.

```js
class Account {
// 1. Public Fields
locale = navigator.language;

// 2. Private Fields
#movements = [];
#pin;

  constructor(owner, currency, pin) {
    this.owner = owner;
    this.currency = currency;
    this.#pin = pin;
    // Protected
    // this._movements = [];
    // this.locale = navigator.language;

    console.log(`Thanks for opening an account, ${owner}`);
  }

// 3. Public Methods
  // Public Interface (API)
  getMovements() {
    return this.movements;
  }

  deposit(val) {
    this._movements.push(val);
  }

  withdraw(val) {
    this.deposit(-val);
  }

  requestLoan(val) {
    if(this.#approveLoan(val)) {
      this.deposit(val);
      console.log('Loan approved');
    }
  }

    // 4. Private Methods
  #approveLoan(val) {
    return true;
  }
}
acc1 = new Account('Jonas', 'Eur', 1111);
acc1.deposit(250);
acc1.withdraw(140);

console.log(acc1.#movements);
// Error
console.log(acc1.#pin);
// Error
```


# Chaining Methods

We can chain methods with the methods within our class. We just need to return the object by returning the this keyword in function we want to chain.


```js
class Account {
  constructor(owner, currency, pin) {
    this.owner = owner;
    this.currency = currency;
    this._pin = pin;
    // Protected
    this._movements = [];
    this.locale = navigator.language;

    console.log(`Thanks for opening an account, ${owner}`);
  }

  // Public Interface (API)
  getMovements() {
    return this.movements;
  }

  deposit(val) {
    this._movements.push(val);
    return this;
  }

  withdraw(val) {
    this.deposit(-val);
    return this;
  }

  _approveLoan(val) {
    return true;
  }

  requestLoan(val) {
    if(this._approveLoan(val)) {
      this.deposit(val);
      console.log('Loan approved');
      return this;
    }
  }
}
acc1 = new Account('Jonas', 'Eur', 1111);


// Chaining
acc1.deposit(300).deposit(500).withdraw(35).requestLoan(25000).withdraw(4000);
```

# ES6 Classes Summary

https://www.udemy.com/course/the-complete-javascript-course/learn/lecture/22649125#content



# Project Planning

Overview:

PLANNING:

1. User Stories
- A description of the applications functionality from the users perspective. All the user stories put together will describe the entire functionality of the entire application.

2. User Stories
- The User Stories will layout all the different features that the appplication requires

3. Features
- Then we put all the Features in to a flowchart 
- This is WHAT we are going to build

4. Architecture
- HOW we build it and implement all of the functionality


DEVELOPMENT:

- Implementation of our plan using code


---

In Depth:

1. ## User Stories

- Description of the applications functionality from the user's perspective

- A common format is writing this out in sentences: "As a (typ of user), I want (an action) so that (a benefit)." This answers the who? the what? and the why?

- In this step we really need to put ourselves in the users shoes


2. ## Features

- Directly based on the user stories

- For each corresponding User Story we list out any related feature and the best type of feature to satify the user story


3. ## Flowchart

- Don't waste too much time on this as a beginner. With more experience then more details can be added at the beginning.

- Again starts with the User Story and moves across time with corresponding events from the beginning which is the page load 

- Contains all the features that we need to implement

- Contains how the different parts of the app interact with eachother

- Which event makes sense to implement

- How data flows across the application

- We can include color coded nodes in the flow chart as a legend to help describe things as well as different types of arrows, Ex.) Red nodes for asynchronous steps, green nodes for rendering something to the UI, dotted arrow lines for expressing the need for a binded event handler

- Not all steps of the application need to be put in the flow chart. Just as best of an idea as you can, that's not too strict. Thjings can get added after as required. It is best to allow the application to morph to needs but keeping in mind it should be closed for modification, but open for extension.

- This is only what the prgram does NOT how


4. ## Architecture

- We dont always need the perfect final architecture figured out in the beginning

- We use this step to experiment and test as well as thinking about structure

- As we need more organization and ways to manage data then we come back to architecture planning
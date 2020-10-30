# The Complete Javascript Course: From Zero To Expert!

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

# Bind Methods

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


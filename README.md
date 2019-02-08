# Starlime Web Javascipt Documentation Standards & Naming Conventions.
 Bonus: Small Introduction to JavaScript and ES6(ECMAScript2015 - used in ReactJS and React-Native platforms. ES6 is almost fully compatible with most browsers. [Check here for compatability](https://kangax.github.io/compat-table/es6/)
 
 ### Good React Resources:
 [Facebook's React-Native Docs](https://facebook.github.io/react-native/docs/getting-started)
 
[React-Native DOM for Web](http://reactnative.com/react-native-dom/)

[RN Tester](https://rntester.now.sh/)

[RNWeb Component, APIs, and Example Apps](https://necolas.github.io/react-native-web/storybook/?selectedKind=Components&selectedStory=ActivityIndicator&full=0&addons=0&stories=1&panelRight=0)

[Zeplin](https://zeplin.io/)

[UIZoo](https://myheritage.github.io/UiZoo.js/)

[Redux / Flux Q&A](https://stackoverflow.com/questions/32461229/why-use-redux-over-facebook-flux)

[React SketchApp from AirBnB](https://github.com/airbnb/react-sketchapp)

### React-Native-Web (Compatability React-Native 0.55, current= 0.56)

[React-Native-Web Docs](https://github.com/necolas/react-native-web/blob/master/packages/website/guides/getting-started.md)

### React-Native-Web, web-specific UI patterns
[Links](https://codesandbox.io/s/53r88k5opx)

[Hover styles](https://codesandbox.io/s/o9q8vy70l5)

[Root element styles](https://codesandbox.io/s/52x1871vjl)

# Table of Contents:
### 1. Commenting &amp; Documentation *(read: styleguide)*

### 2. General JavaScript Intro + Best Practice
   - JavaScript Keywords
   - General Guidelines 
	    
	    1. Avoiding Global Namespace
	    
	    2. Declare Functions and Variables
	    
	    3. Declare Expressions cleanly
	    
	    4. Beware of JavaScript Type Conversion
	    
	    5. Comparison Operators, Confusion, and You

### 3. ES6 Syntax and Modularizing the React Workspace
- Modules and Grouping Components

### 4. Summary and Important React Specific Notes

# 1. Commenting & Documentation / StyleGuide

Commenting should describe each function and purpose, but not make the function more confusing. You are describing functionality, not giving your life story. 
P.S. Don't be afraid of whitespace

### Variable Names:
- **camelCase** for identifier names (variables and functions).
- All names start with a **lowercaseLetter**.

### Spaces Around Operators:
Always put spaces around operators ( = + - * / ), and after commas:

#### Examples:
```js
var x = y + z;  
var values = []; // initialize array first
values.push("Volvo",  // then add values 
            "Saab",   
	    "Fiat"    // NOTE! No trailing Comma. Valid 
	   );        // JSON does not use trailing commas
	            // Trailing Commas will crash IE8
console.log(values); // result: ["Volvo", "Saab", "Fiat"]
```


##  General Rules for Statements:

-   Put the opening bracket at the end of the first line.
-   Use one space before the opening bracket.
-   Put the closing bracket on a new line, without leading spaces.
-   Do not end a complex statement with a semicolon.

### Functions:
```js
function  toCelsius(fahrenheit) {  
    return  (5  /  9) * (fahrenheit -  32);  
}
```

### Loops:
```js
for  (i =  0; i <  5; i++) {  
  x += i;  
}
```

### Conditionals:
```js
if  ( time <  20 ) {  
  greeting =  "Good day";  
}  else  {  
  greeting =  "Good evening";  
}
```

## Object Rules

General rules for object definitions:

-   Place the opening bracket on the same line as the object name.
-   Use colon plus one space between each property and its value.
-   Use quotes around string values, not around numeric values.
-   Do not add a comma after the last property-value pair.
-   Place the closing bracket on a new line, without leading spaces.
-   Always end an object definition with a semicolon.

### Example
```js
var  person = {  
  firstName:  "John",  
  lastName:  "Doe",  
  age:  50,  
  eyeColor:  "blue"  
};
```

## Naming Conventions

-   Variable and function names written as  **camelCase**
-   Constants (like PI) written in  **PascalCase**
 - Hyphens can be mistaken as subtraction attempts. Hyphens are NOT    	allowed in JavaScript names.


#### If you still want/ need more info on javascript specific content please reference the  [MDN Dev Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types)

# 2. JavaScript General Guidelines

## Javascript Keywords

### [Link](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Reserved_keywords_as_of_ECMAScript_2015)
### Reserved keywords as of ECMAScript 2015
(Hover over a keyword to learn more about it )

-   [`break`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/break "The break statement terminates the current loop, switch, or label statement and transfers program control to the statement following the terminated statement.")
-   [`case`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch "The switch statement evaluates an expression, matching the expression's value to a case clause, and executes statements associated with that case, as well as statements in cases that follow the matching case.")
-   [`catch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch "The try...catch statement marks a block of statements to try, and specifies a response, should an exception be thrown.")
-   [`class`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/class "The class declaration creates a new class with a given name using prototype-based inheritance.")
-   [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const "The source for this interactive example is stored in a GitHub repository. If you'd like to contribute to the interactive examples project, please clone https://github.com/mdn/interactive-examples and send us a pull request.")
-   [`continue`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/continue "The continue statement terminates execution of the statements in the current iteration of the current or labeled loop, and continues execution of the loop with the next iteration.")
-   [`debugger`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/debugger "The debugger statement invokes any available debugging functionality, such as setting a breakpoint. If no debugging functionality is available, this statement has no effect.")
-   [`default`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/default "The default keyword can be used in two situations in JavaScript: within a switch statement, or with an export statement.")
-   [`delete`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete "The JavaScript delete operator removes a property from an object; if no more references to the same property are held, it is eventually released automatically.")
-   [`do`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/do...while "The do...while statement creates a loop that executes a specified statement until the test condition evaluates to false. The condition is evaluated after executing the statement, resulting in the specified statement executing at least once.")
-   [`else`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else "The if statement executes a statement if a specified condition is truthy. If the condition is falsy, another statement can be executed.")
-   [`export`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/export "The export statement is used when creating JavaScript modules to export functions, objects, or primitive values from the module so they can be used by other programs with the import statement.")
-   [`extends`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/class "The class declaration creates a new class with a given name using prototype-based inheritance.")
-   [`finally`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch "The try...catch statement marks a block of statements to try, and specifies a response, should an exception be thrown.")
-   [`for`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for "The for statement creates a loop that consists of three optional expressions, enclosed in parentheses and separated by semicolons, followed by a statement (usually a block statement) to be executed in the loop.")
-   [`function`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/function "The function declaration defines a function with the specified parameters.")
-   [`if`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else "The if statement executes a statement if a specified condition is truthy. If the condition is falsy, another statement can be executed.")
-   [`import`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import)
-   [`in`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/in "The in operator returns true if the specified property is in the specified object or its prototype chain.")
-   [`instanceof`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/instanceof "The instanceof operator tests whether the prototype property of a constructor appears anywhere in the prototype chain of an object.")
-   [`new`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new "The new operator creates an instance of a user-defined object type or of one of the built-in object types that has a constructor function.")
-   [`return`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/return "The return statement ends function execution and specifies a value to be returned to the function caller.")
-   [`super`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super "The super keyword is used to access and call functions on an object's parent.")
-   [`switch`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch "The switch statement evaluates an expression, matching the expression's value to a case clause, and executes statements associated with that case, as well as statements in cases that follow the matching case.")
-   [`this`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this "A function's this keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.")
-   [`throw`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/throw "The throw statement throws a user-defined exception. Execution of the current function will stop (the statements after throw won't be executed), and control will be passed to the first catch block in the call stack. If no catch block exists among caller functions, the program will terminate.")
-   [`try`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/try...catch "The try...catch statement marks a block of statements to try, and specifies a response, should an exception be thrown.")
-   [`typeof`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/typeof "The typeof operator returns a string indicating the type of the unevaluated operand.")
-   [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var "The var statement declares a variable, optionally initializing it to a value.")
-   [`void`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/void "The void operator evaluates the given expression and then returns undefined.")
-   [`while`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while "The while statement creates a loop that executes a specified statement as long as the test condition evaluates to true. The condition is evaluated before executing the statement.")
-   [`with`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/with "The with statement extends the scope chain for a statement.")
-   [`yield`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/yield "The yield keyword is used to pause and resume a generator function (function* or legacy generator function).")

#  2. General Guidelines:

### This section is for an overview, and will get more in detail in a later section if desired.

### A. Avoid Global Variables: 
  Know the difference between variable declarations. [Read More](https://www.w3schools.com/js/js_best_practices.asp)

### B. Declare Functions and Variables at the top of the appropriate scope. 
 Know the appropriate scope for your variable and type of declaration you should use in JavaScript [Read More](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Variable_scope)
 
### C. Never declare Number, String, or Boolean Objects, there are better ways to declare
 
### D. Beware of Automatic Type Conversions
JavaScript is loosely typed [Read More](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Dynamic_typing)

### E. Comparison Operators ( Use === Comparison)


#
## A. Avoid Global Variables

When you declare a variable outside of any function, it is called a **`global`** variable, because it is available to any other code in the current document. 
When you declare a variable within a function, it is called a
**`local`**  variable, because it is available only within that function. With es6 (in React) There is also a *block* scope which I will discuss further in the declaring variables section.

### Example of Global Variables
```js
//Initiate count  
var count =  0;  
// Function to increment count  
function  add() {  
	count += 1;  
}  
// Call add() 3 times  
add();  
add();  
add();  
  
// The counter is now 3
```

### Local Variable Declaration and Functionality
Example:
```js
const Add = (function(){
	let counter = 0;
    return ()=>{
    	counter += 1; 
	return counter;
    }
})();
Add();
```
- The variable  **add**  is assigned the return value of a self-invoking function.

- The self-invoking function only runs once. It sets the counter to zero (0), and returns a function expression.

- This way add becomes a function. The "wonderful" part is that it can access the counter in the parent scope.

- This is called a JavaScript  **closure.**  It makes it possible for a function to have "**private**" variables.

- The counter is protected by the scope of the anonymous function, and can only be changed using the add function.

For More On JS Closures: [Read Here](https://www.w3schools.com/js/js_function_closures.asp) 

## B.  Variable / Functional Declarations at the Top of Scope:

It is a good coding practice to put all declarations at the top of each script or function.

This will:

-   Give cleaner code
-   Provide a single place to look for local variables
-   Make it easier to avoid unwanted (implied) global variables
-   Reduce the possibility of unwanted re-declarations


Types of Variable Declarations:

[`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var) =  Declares a variable, optionally initializing it to a value.

[`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) = Declares a block-scoped, local variable, optionally initializing it to a value.

[`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const ) = Declares a block-scoped, read-only named constant.

**var**  vs. **let**
Check out the following example:

**var**
```js
if (true) {
  var x = 5;
}
console.log(x);  
// x is 5
```
**let**

```js
if (true) {
  let y = 5;
}
console.log(y);  
// ReferenceError: y is not defined
```

*Variable Hoisting*: 
All `var` statements in a function should be placed as near to the top of the function as possible. It will be *hoisted* if not declared at the top, meaning JavaScript will move the declaration to the top for you, but this is not best practice and you should not rely on it.
[Read More on Variable Hoisting](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Variable_hoisting)

### Function Declaration:
**Always** initialize a function *before* using it.
```js
// Declare and initiate at the beginning 
var firstName = "",
lastName = "",
price = 0,          		   
discount = 0,  		
fullPrice = 0, 
tax = 0,
myArray = [],  
myObject = {}; // remember to end declarations with a semi-colon.

// Declare Functions:
function foo() {
firstName ="Jimmy";
  console.log(firstName);
}

var baz = function() {
  price = 15;
  tax = 10;
  discount = 5;
  fullPrice = (price + tax) - discount;
  console.log(fullPrice);
};

if (foo(); //result: "Jimmy";
baz(); //result: "20";
```
 
## C. Never Initialize a Number, String, or Boolean as Objects, there are Better ways to declare Them

**In these examples, we prefer to declare like x and *NOT* like y.**
```js
var x = "John";  
var y = new String("John");  
console.log(x === y);
/*console log = false 
because x is a string and y is an object.*/
```
or
```js
var x = new String("John");  
var y = new String("John");  
console.log(x == y) 
// console logs false because you cannot compare objects.
```

Keep your declarations like the following:
```js
var x1 = {}; // new object 
var x2 = ""; // new string 
var x3 = 0; // new number  
var x4 = false; // new boolean  
var x5 = []; // new array   
var x6 = /()/; // new regexp   
var x7 = function(){}; // new function
```
 
## D. Beware, Beware the Automatic Type Conversions

For example, you could define a variable as follows:
```js
var answer = 42;
```
And later, you could assign the same variable a string value, for example:
```js
answer = 'Thanks for all the fish...';
```

Because JavaScript is dynamically typed (read: loosely typed), this assignment does not cause an error message.

[Read More](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures#Dynamic_typing)

## 5. Comparison Operators ( Use === Comparison)
 
 The == comparison operator always converts (to matching types) before comparison.

The === operator forces comparison of values and type

#### (==) examples:
```js
1    ==  1         // true
'1'  ==  1         // true
1    == '1'        // true
0    == false      // true
0    == null       // false
var object1 = {'key': 'value'}, object2 = {'key': 'value'}; 
object1 == object2 //false
0    == undefined  // false
null == undefined  // true
```

#### (===) examples:
```js
3 === 3   // true
3 === '3' // false
var object1 = {'key': 'value'}, object2 = {'key': 'value'};
object1 === object2 //false
```


# 3. ES6 Specific Syntax &amp; Modularization of React Components

## ES6 Useful Features for React-Native functionality
These are the ES6 features that I believe to be most important / relevant to this project:
Note: Some will look slightly different constructed using React's Components, but this will give you the initial idea

-   [Arrows](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
-   [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
-   [let + const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Declarations)
-   [Iterators + for..of](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of)
-   [Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)
### If you're too lazy to check the MDN docs here are some quick examples for you:

### Arrow Function Example:
```js
var materials = [
  'Hydrogen',
  'Helium',
  'Lithium',
  'Beryllium'
];
//this function returns the length of each material 
console.log(materials.map(element => element.length));
// expected output: Array [8, 6, 7, 9]
```
[Read More](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
# 
### Classes Example:
```js
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

  position(x, y) {
    this.x = x;
    this.y = y;
  }
}
```
[Read More](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
# 

### Let + Const:
Technically already reviewed, but

[`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var)
Declares a variable, optionally initializing it to a value.

[`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)
Declares a block-scoped, local variable, optionally initializing it to a value.

[`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const)
Declares a block-scoped, read-only named constant.

 [Read More](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Declarations)

#

### Iterators:

### Difference between  `for...of`  and  `for...in`

Both  `for...in`  and  `for...of`  statements iterate over something. The main difference between them is in what they iterate over.

The  [`for...in`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)  statement iterates over the  [enumerable properties](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Enumerability_and_ownership_of_properties)  of an object, in an arbitrary order.

The  `for...of`  statement iterates over data that [iterable object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Iterators_and_Generators#Iterables)  defines to be iterated over.

**Iterating over an array:**
```js
let iterable = [10, 20, 30];

for (let i of iterable) {
  i++;
  console.log(i);
}
// 11
// 21
// 31

for (let i in iterable){
 i++;
 console.log(i);
 }
 // 1
 // 2
 // 3
```

[Read More](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...of)



## Promises:
(I decided to give promises more room because they *rock*)

Unlike old-style passed-in callbacks, a promise comes with some guarantees:

-   Callbacks will never be called before the  [completion of the current run](https://developer.mozilla.org/en-US/docs/Web/JavaScript/EventLoop#Run-to-completion)  of the JavaScript event loop.
-   Callbacks added with [then()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/then)  even  _after_  the success or failure of the asynchronous operation, will be called, as above.
-   Multiple callbacks may be added by calling [then()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/then)  several times. Each callback is executed one after another, in the order in which they were inserted.

One of the great things about using promises is  **chaining**.
### Chaining:
```js
const Promise = doSomething();
const Promise_2 = promise.then(successCallback, failureCallback);
```
In the old days, doing several asynchronous operations in a row would lead to the classic callback "hell":

```js
doSomething(function(result) {
  doSomethingElse(result, function(newResult) {
    doThirdThing(newResult, function(finalResult) {
      console.log('Got the final result: ' + finalResult);
    }, failureCallback);
  }, failureCallback);
}, failureCallback);
```

With promises and arrow functions, promises now look like this:
```js
doSomething()
.then(result => doSomethingElse(result))
.then(newResult => doThirdThing(newResult))
.then(finalResult => {
  console.log(`Got the final result: ${finalResult}`);
})
.catch(failureCallback);
```
[Read More](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises)


## Modularizing the React Workspace
Sources:

[How to Better Organize React Apps](https://medium.com/@alexmngn/how-to-better-organize-your-react-applications-2fd3ea1920f1)

[Why React Devs should Modularize](https://medium.com/@alexmngn/why-react-developers-should-modularize-their-applications-d26d381854c1)

[JavaScript Module Pattern in depth](http://www.adequatelygood.com/JavaScript-Module-Pattern-In-Depth.html)

![Universal Components for a Modular App](https://i.imgur.com/2NLmj0W.png)


First, I want to provide an ideal / modular file base architecture:
```js
/src  
  /components   
    /Button   
    /Notifications  
      /components  
        /ButtonDismiss    
          /images  
          /locales  
          /specs   
          /index.js  
          /styles.scss  
      /index.js  
      /styles.scss

  /scenes  
    /Home   
      /components   
        /ButtonLike  
      /services  
        /processData  
      /index.js  
      /styles.scss

    /Sign   
      /components   
        /FormField  
      /scenes  
        /Login  
        /Register   
          /locales  
          /specs  
          /index.js  
          /styles.scss

  /services  
    /api  
    /geolocation  
    /session  
      /actions.js  
      /index.js  
      /reducer.js  
    /users  
      /actions.js  
      /api.js  
      /reducer.js

  index.js   
  store.js
  ```
In this example, you can see how each module is grouped with similar components. Part of Modular Design:
> each component, scene or service (a feature) has everything it needs to work on its own, such as its own styles, images, translations, set of actions as well as unit or integration tests. 

Grouping Components based on utilization will be huge. Keeping folders, components, and modules separate and with like-content is very important. 


# 4 Summary:

## Declarations:
### Variable Declarations:

[`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var) =  Declares a variable, optionally initializing it to a value.

[`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) = Declares a block-scoped, local variable, optionally initializing it to a value.

[`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const ) = Declares a block-scoped, read-only named constant.

### Declaring Objects in JavaScript
```js
var x1 = {}; // new object 
var x2 = ""; // new string 
var x3 = 0; // new number  
var x4 = false; // new boolean  
var x5 = []; // new array   
var x6 = /()/; // new regexp   
var x7 = function(){}; // new function
```
### Declaring a Function:
You can name a function
```js
function foo() {
firstName = "Rexxar";
  console.log(firstName);
}

var baz = function() {
	console.log("Me Go Face, Taunt is Cheat");
}

foo();
baz();
```

**Iterating over an array:**
```js
let iterable = [10, 20, 30];

for (let i of iterable) {
  i++;
  console.log(i);
}
// 11
// 21
// 31

for (let i in iterable){
 i++;
 console.log(i);
 }
 // 1
 // 2
 // 3
```

## React Specific:

The main piece of advice you will always hear when practicing React is to NEVER set the state directly.
There is a method in React that allows you to do that called ```setState()```

### React / Redux short read on importance:
[Source](https://pub.monospacelabs.com/react-native-developing-using-best-practices-part-1-9d6f3bd77a68)

#### What’s Redux?
As its documentation states, redux is a predictable state container for JavaScript applications. It’s both regular library and a data-flow architecture. A lot of people think that it comes with React Native and it is just another tool of it. That’s a big misunderstanding! It’s a framework-agnostic tool that fits with React Native really well but it still can be used with almost any JavaScript library or framework like jQuery, Angular, Ember, Meteor or even vanilla JavaScript.

#### Why should I use it?
React does not consider direct component-to-component communication as a good practice even if it has the ability to support it. An architecture like this, is going to lead to a poorly structured source code sooner or later which will be difficult to maintain and scale. Redux offers a way to store all of the application state in just one place with global scope. Then your React Native components dispatch actions that trigger changes to the store. Components that need to “know” about those changes should be connected to Redux state.

#### You may hear about Flux, but what is it? And how does it compare to my precious Redux?

Redux is not  _that_  different from Flux. Overall it has same architecture, but Redux is able to cut some complexity corners by using functional composition where Flux uses callback registration.

There is not a fundamental difference in Redux, but I find it makes certain abstractions easier, or at least possible to implement, that would be hard or impossible to implement in Flux.

[Read More on Stack Overflow](https://stackoverflow.com/questions/32461229/why-use-redux-over-facebook-flux)


# Bonus Section
If you made it this far, perhaps you like to read, or are maybe desperate. Anywho, here is compilation of common mistakes in JavaScript, an explanation of what went wrong, and how to fix it.

### [Read More](https://www.w3schools.com/js/js_mistakes.asp)

## First Lesson: Assignment Operator Mishap

 This if statement returns true (hopefully not as expected), because 10 is true:
```js
var x = 0;	// initializing x to 0
if (x = 10)	// setting it's value to 10, 
			// not comparing!
```
 
This *if* statement returns false (as expected) because x is not equal to 10:
```js
var x = 0; 	  // initializing x to 0
if (x == 10)  // Comparing it's value to 10
// or if (x === 10)
// This (===) would check type AND value.
```

## Using Strict Mode
`StrictMode`  currently helps with:

-   [Identifying components with unsafe lifecycles](https://reactjs.org/docs/strict-mode.html#identifying-unsafe-lifecycles)
-   [Warning about legacy string ref API usage](https://reactjs.org/docs/strict-mode.html#warning-about-legacy-string-ref-api-usage)
-   [Detecting unexpected side effects](https://reactjs.org/docs/strict-mode.html#detecting-unexpected-side-effects)
-   [Detecting legacy context API](https://reactjs.org/docs/strict-mode.html#detecting-legacy-context-api)

### Example:
```js
import React from 'react';

function ExampleApplication() {
  return (
    <View>
      <Header />
      <React.StrictMode>
        <View>
          <ComponentOne />
          <ComponentTwo />
        </View>
      </React.StrictMode>
      <Footer />
    </View>
  );
}
```
In the above example, strict mode checks will _not_ be run against the `Header` and `Footer`components. However, `ComponentOne` and `ComponentTwo`, as well as all of their descendants, will have the checks.

Read More on React Strict Mode
## Expecting Loose Comparison
In regular comparison, data type does not matter. This if statement returns true:
```js
var x = 10;
var y = "10";
if (x == y)
```
In strict comparison, data type does matter. This if statement returns false:

```js 
var x = 10;
var y = "10";
if (x === y)
```
#### Switches *Always* use strict typing

This case switch will display an alert:

```js
var x = 10;
switch(x) {
    case 10: alert("Hello");
}
```
This case switch will not display an alert:
```js
var x = 10;
switch(x) {
    case "10": alert("Hello");
}
```

## Confusing Addition & Concatenation

**Addition**  is about adding  **numbers**.

**Concatenation**  is about adding  **strings**.

In JavaScript both operations use the same + operator.

### Example Functions
```js
function(){
	console.log(4 + 4); // result: 8 as expected
}
```
Now let's take a look at if the number as been "type" changed on purpose or by accident into a string
```js
function(){
    console.log(4 + "4"); 
    // result: 44, most likely not intended
}
```

## Breaking a Return Statement

It is a default JavaScript behavior to close a statement automatically at the end of a line.

Because of this, these two examples will return the same result:

### Example 1
```js
function  myFunction(a) {  
    var  power =  10  
    return  a * power  
} 
```


### Example 2
```js
function  myFunction(a) {  
    var  power =  10;  
    return  a * power;  
}
```

## Accessing Arrays / Objects

Many programming languages support arrays with named indexes.

Arrays with named indexes are called associative arrays (or hashes).

JavaScript does  **not**  support arrays with named indexes.

In JavaScript,  **arrays**  use  **numbered indexes**:

#### Objects:
In JavaScript,  **objects**  use  **named indexes**.

If you use a named index, when accessing an array, JavaScript will redefine the array to a standard object.

After the automatic redefinition, array methods and properties will produce undefined or incorrect results:

## Undefined vs. Null. What's the big deal?

JavaScript objects, variables, properties, and methods can be  **undefined**.

In addition, empty JavaScript objects can have the value  **null**.

This can make it a little bit difficult to test if an object is empty.

You can test if an object exists by testing if the type is  **undefined**:

### Example:
```js
if  (typeof  myObj ===  "undefined")
```

But you cannot test if an object is  **null**, because this will throw an error if the object is undefined:

### Incorrect:
```js
if  (myObj ===  null)
```
To solve this problem, you must test if an object is not  **null**, and not  **undefined**.

 You must test for not  **undefined**  BEFORE you can test for not  **null**:

### Correct:
```js
if  (typeof  myObj !==  "undefined"  && myObj !==  null)
```

## Expecting Block Level Scope

JavaScript  **does not**  create a new scope for each code block.

It is true in many programming languages, but  **not true**  in JavaScript.

This code will display the value of i (10), even OUTSIDE the for loop block:

### Example
```js
for  (var  i =  0; i <  10; i++) {  
// some code  
}  
return  i;
```


## Updated React Preferences / Documentation:

### !Troubleshooting First couple vids!
First in the tutorial, you won't be able to get your native app up and running without adding :
```js
export default App;
```
at the bottom of your App.js file.
The author fails to mention this as this is a change from when the video was made.


### Styling Preferences:

In the tutorial videos Section 6 lecture 24, the author writes the styles for the ```<Header />``` component like so:
```js
const Header = () => {
  const { textStyle } = styles; // This will change
  return (
    <View>
      <Text style={styles.textStyle}>Test Application</Text>
    </View>
  );
};

```
We can just reference the style sheet in the "style" tag itself without the extra step of declaring it a const. This is how our new app begins, and this is how we should continue to code our projects.

```js
const Header = () => {

  return (
    <View>   // notice no const AND just appending
		    // styles.customStyle
      <Text style={styles.textStyle}>Test Application</Text>
    </View>
  );
};

```

So instead of having a file with 20 const stylings, each component should reference their own styles in line.

## Wrap up
That about wraps up all the quirks of JavaScript and es6 syntax that I believe will be relevant to the application. Hopefully this sort of guide can serve as a first place to search for answers and give good enough resources to grasp the concepts.

I will continue updating this project with more information as I progress through the app tutorial

Thanks!
-Ronnie Forcier

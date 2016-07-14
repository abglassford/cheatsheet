# JavaScript Cheatsheet

Last updated 07/14/2016

## Primitives
Primitives are JavaScript building blocks

- Boolean - `true` or `false`
- Numbers - `integers` or `floats` `NaN`
- Strings - text
- Undefined - value has not been defined
- Null - intentional absence of an object value
- Symbol - (ES6)

## Variables
Container to store data (values). Shortcuts for storing data

- Declared using `var`
- Naming - can`t start with Numbers, can`t have spaces, avoid symbols except `-`, `_`, `$` should be descriptive and camelCase

Arrays, Objects, methods, accessing data, etc.

## Data Structures
- Arrays: container for primitives (and there data structures), accessed via index, maintain order
- Objects: key/value pair, accessed via bracket or dot notation, not ordered

## Programming Paradigms
Procedural vs functional

- Procedural: JS renders commands in order (set of instructions)
- Functional: break apart code/problem logically, generally separate state from behavior, reusable

## Flow Control
Decides which things run based on specific conditions (order) or Loops

Conditionals control the flow of the program (if, if-else)

## Loops
Continue executing code for specified number of iterations

- infinite loop: loop that runs forever, stack overflow, no more memory :(

for, while, for...in, for...of, do...while

## Operators
Math: `+`, `-`, `*`, `/`, `%`, can combine (`++`, `+=`)
Logical: `&&`, `||`
Comparison: `===` (strict), `==` (loose), `>`, `!`, `<`, `>=`, `<=`

## Functions
Set of instructions that achieve a specific task defined by code block.
- Can be defined, and then invoked to return some output
- Can contain parameters (when defined) and arguments (passed in when called/invoked)

#### Methods vs Functions:
- Method: function that is contained within an Object
- Function: first class citizens and can be used as arguments (like primitives and data structures) in JS. Always return something. If not explicitly set, then return `undefined`
- can have optional (see HOF)
- expression vs declaration



## Scope
- the range in which something can be accessed
- global vs local(aka function/lexical)
- a variable declared in local scope will not be used in global scope
- a variable declared in global scope will be used in local scope
function foo(){
  function bar(){
    var taco = 'delicious'
    console.log(taco) //'delicious'
  }
  fuction foobar(){
    console.log(taco) //undefined
  }
}

## Hoisting
The process by which the computer moves all variable declarations to the top of the applicable scope, so that it never encounters a variable it is unaware of. It's important to note that it does not move the variable assignment to the top of the page.

`var foo = 'bar'`

moves declarations (`var foo;`) BUT NOT assignment (`var foo = bar`)

## HOF

Function that takes other functions; the function that's passed into the HOF is the callback

Asynchronous: different code can run at different times

## String concatenation
Used to join 2 or more strings (string.concat())
`'test'.concat('ing') // => testing`

## Computer science
#### BigO Notation
How developers discuss the complexity of an algorithm as a way to understand how fast a program will run given it's input
- Deals with the worst case scenario
- O(n) - Linear Time
  - Directly related to input size (longer input, longer runtime)
- O(1) - Constant Time
  - Bound by a constant number. Regardless of input time, the runtime remains the same.
- O(n^2) - Quadratic Time
  - A loop that iterates over all items nested within a loop that also iterates over all items

  The exponent grows based on the number of nested Loops

a 'flogarithm' of a positive number (n) represent by (log(n)) is the number of digits it has.
Factorials - way worse than quadratics... WAAAAAAYYYY WORSE.

[Big O Cheatsheet](http://bigocheatsheet.com/)

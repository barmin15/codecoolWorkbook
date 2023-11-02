# Programming Basics questions

## Data basics

- What are the differences between objects and arrays? What is the purpose of the object and what is the purpose of the array?
Both arrays and objects are collections of data, and data structures, however objects store data in key value pairs, while arrays store them in a sequence (eg list). Both their puspose is to store data.

- How can you access a key's value in an object?
You can acces a objects key with the 'dot' notation (eg. Object.key()), and with the bracket notation (eg. Object["key's value"])

- How can you access the first and the last item of an array?
To access the first: arr[0], arr.shift()
To access the last: arr[length -1], arr.pop()

- Name all the primitive types in JavaScript.

There are seven primitive types in javascript: string, number, boolean, null, undefined, bigint, symbol.


## Algorithm basics

- What are the assignment operators? Name some of them.
Assignement operators assign the value of its right hand operator to its left hand operator.
exaples: a+=b, a -=b, a*=b, a**=b

- What are the arithmetic operators? Name some of them.
We can preform basic mathematical operations with them.
examples: +, -, *, %, ++

- What are the comparison operators? Name some of them.
We can preform basic comparisons between datas with them.
examples: ==, !=, <, ===

- What are the logical operators? Name some of them.
Logical operators can be a word or a symbol used to connect two or more expressions.
examples: ||, &&

- What is the difference between `for`, `for of` and `for in`?
'for': it iterates with index numbers. You can set the start and the end of the index.
'for of': iterates through elements in a data structure.
'for in': iterates throught keys in any key value pair style data structure. 

- How do you find the average of values in an array if you can’t use any built-in functions or methods?
You iterate through the array, add every element together and divide it with the length of the array. 

## Function basics

- What are the main parts of a function?
function [function keyword] addTwoNums [name] (numOne, numTwo) [parameters]{
    return numOne + numTwo [statement enclosed in braces]
}

- What is the difference between parameters and arguments?
Parameters are the names listed in the function, arguments are the real valeues.

- What are the differences between function expression and function statement?
Function expression is a function saved in a variable, while function statement decleares a function for later use.

## OOP Basics

- What is a method?
Methods are actions that can be preformed on objects. They are functions stored as object properties.

- Name 3 builtin functions (and/or methods) regarding strings.
    Examples: 
        string.toUpperCase(),
        string.split(),
        string.slice(),
        string.substring(),
        string.concat(),
        string.charAt(),
        string.repeat(),
        string.startsWith(),
        string.endsWith(),
        string.includes(),
        string.match(),
        "Number(string)"

- Name 3 builtin functions (and/or methods) regarding arrays.

    Examples:
        array.push(),
        array.join(),
        array.concat(),
        array.entries(),
        array.every(),
        array.from(),
        array.flatMap(),
        array.includes(),
        array.unshift(),
        array.reverse(),
        array.sort()

- Name 3 builtin functions (and/or methods) regarding numbers.

    Examples:
    number.toString(),
    number.isNaN()

## FP Basics

- What is a callback function?
A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

- What are the differences between `for` loops and `forEach`?
They are both used to iterate over data structures, however a forEach recieves a callback function to invoke on each element.  

## File basics

- What is the difference between JavaScript data structures and JSON data structures?
Json (javascript object notation) is derived from javascript, it is used to transport and store data. Typically, JSON is used when data is sent from a server to a web page (in a json file the objects key is in a string form). It's name can be misleading, since it is a "programming language independent" format, that many (including) javascript use.
    The main difference is that javascript has functions and can manipulate data.

- How do you create JavaScript data structure from a JSON file's data?
Use the JavaScript function JSON.parse() to convert text into a JavaScript object. And if you want to parse javascript object to Json, you can use the JSON.stringify(value, replacer, space) method to stringify a JavaScript object or value to a JSON string.

## View Basics

- What is the difference between JavaScript data structures and DOM (HTML document) data structures?
HTML is a standard markup language that provides the primary structure of a website. JavaScript simply adds dynamic content to websites to make them look good. HTML work on the look of the website without the interactive effects and all. HTML pages are static which means the content cannot be changed.
(note: HTML has a tree structure)

- What are the steps of changing a HTML element's content with JavaScript?

you get the element, with by its id or class, and you change its innerHTML
    Example: 
        document.getElementById("root").innerHTML = "<div>I'm inside the tags</div>"

## Event basics

- What is an event listener?
An event listener is a procedure in JavaScript that waits for an event to occur. A simple example of an event is a user clicking the mouse or pressing a key on the keyboard.

- What are the steps of changing a HTML element's content when the element clicked?
you get the html element by its id or class, add an event listener to it. The event listeners first parameter is "click" and the second is the function you call when its clicked. in the function you change what you want.

- Inside a `click` event listener, how can you access the element that has been clicked?
The 'this' keyword refers to the element that has been clicked, or you can pass the 'event' as an argument and call the 
event.target in the function

## Design Basics

- What are the differences between `display: block` and `display: inline` CSS properties?
Compared to display: inline, the major difference is that display: inline-block allows to set a width and height on the element.

- What are the differences between `position: relative` and `position: absolute` CSS properties?
Relative - the element is positioned relative to its normal position. Absolute - the element is positioned absolutely to its first positioned parent. 


- What is the box model, name the CSS properties connecting to it?
The CSS box model is a container that contains multiple properties including borders, margins, padding, and the content itself.
It is used to create the design and layout of web pages. 
It can be used as a toolkit for customizing the layout of different elements.

- What CSS properties affect font and text appearance?
font.family, font-size, font-weigh, text-allign, color, etc.

- What are the steps of adding or removing a HTML element's class name?
Get the element by its id or class. You can add class by the classList.add(), and remove it with the classList.remove()

## JavaScript - language specialties

- Is `null` an object or a primitive?
Null is a primitive.

- What is `undefined`?
When a data has not been initialized (no right hand operator was assigned) it will return as 'undefined'.

- What does it mean that a data type is mutable and what does it mean that it is immutable? Mention some examples.
Mutability refers to data types that can be accessed and changed after they've been created and stored in memory. Immutability, on the other hand, refers to data types that you can't change after creating them – but that you can still access in the memory.
    Mutable Examples:
        Object,
        Array
    Immutable Examples:
        all primitive types

- What does it mean that a data type is passed by value and what does it mean that it is passed by reference? Mention some examples.
In programming, the way a data type is passed to a function or method determines whether the original value is modified or whether a new value is created.
    Passed By Value Examples:
        all primitive types
    Passed By Reference Examples:
        Object,
        Array

- When to use `var`, `let`, and `const`?
With var, you can access the data anywhere (never use it) [function scope]
With let and const you can only access the value within its own scope [block scope]
Let data can be changed while const cannot

- What is hoisting?
Refers to the interpreter (machine), moving datas and codes to the top to read first.
Variables and functions can be hoisted depending on their scope.

## Git

- What are the advantages of using a version control system?
Multiple people can work on something together, you can you back in the evolution of the code, it is a safety net for your code(created a copy).

- What’s the difference between Git and GitHub?
Git is a version control system (follows the evolution of the code). While github is a webbased storing system (stores the evolution of the code).

- What are remote repositories in Git?
It is a version of a project, stored on a different servers, rather than your own local machine.

- Why does a merge conflict occur?
When Git sees different code on the same line in the same repository.

## Terminal

- How do you run a JavaScript file in the terminal?
Download node. run the node command and the file and it's extension (be in the same repository as the file, or add the absolute path of the file) you want to open.

- How do you stop a running a command in the terminal?
ctrl c sends a message and command z stops it

- How go you get the previous command in the terminal?
with the up arrow key

- How do you go to the current directory's parent directory in the terminal?
with the cd .. command

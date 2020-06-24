Using Let and const  keyword

Templates Literals

Destructuring

    Borrows inspiration from languages like [Perl](https://en.wikipedia.org/wiki/Perl) and [Python](https://en.wikipedia.org/wiki/Python_%28programming_language%29) . it allows you to specify an element you want to extract from an array or object on the side of an assisgment

Forexample

```
const marks = [ 10, 45, 78 ];
const [x, y, z] = marks;
console.log(marks)
```

Object literal shorthand

This ishelpful for intializing objects. its a way of avioding repetition and it improves on your  code quality

, If you have come  accross or written code like

```js
let name = "jane";
let color = "Red";
let xcode = 2340;
const person = {
    name : name,
    color :color,
    xcode:xcode
}
console .log(person);
```

With Object shorthand this can be improved like;

```js
let name = "jane";
let color = "Red";
let xcode = 2340;
const person = { name, color, xcode };
console.log(person)
```

An undestanding of iteration
This work with for loops and for ..of  looops, when looping through an arrays this for loopiterator works like an indexe in an array it lets you have access each  elements in the array one after the other. so the process of accessing each element or item in the array on after another is iteration.

Loops

In ES6 we have a new loop called for ..of loop. This is to loop over any type of data that is iterable. Its works in the same way the as the for in.. loop execpt that here you swap out the in  with of and the index too cn be left out. let look at thes two different example

for in loop 

```js
const digits = [0,1, 2, 4, 3, 6];
for (const digit in digits ){
    if (digit % 2 === 0){
    continue..,
}
console.log(digit);
}
```

For loop of

```js
const digits = [0,192,33,4,];
for (const digit of digits ){
    if(digit % 2 === 0){
    continue ....
}
console.log(digit);
}
```

Spread Operators

Example

```js
const fruits = ["mangoes", "apples", "pears"];
console.log(...fruits);
```

You can also use concat() this can be used when combining arrays.

Forexample

```js
const students = ["jane", "edna", "matthew", "Andrew" ];
const grade = [2, 3, 4, 5];
const classes = students.concat(grade);
console.log(classes);
```

Arrow Functions 

This  annew way fo writing fucntion in javascript following the ES6 syntax.The aresimliar to regular funcitons in behaviour but diffrerent syntaically.
Let have a look at the two

```js
const upperizedNames = ["Farrin", "Nats", "Kats"].map(function(name){
return name.toUpperCase();
});
```

With Arrow Functions

```js
const upperizedNames = ["Farrin", "Nats", "Kats"].map(
    name => name.toUpperCase() 
);
```

When converting an regular function to use Arrow Function ... Looking at the example above this is what you do;

    - Remove the `function` keyword
    - Remove the parethesis
    - Remove the `return` keyword
    - Remove the semi colon
    - And add the an arrow (=>) between the parameter list and the fucntion body.



Concise and block body syntax.

Arrow functions allows you write code with a short format called the concise and block body syntax, this format is;

- Has no curly braces surrounding the fucntion body.

- And it automatically returns  the expression.
  The block body syntax  can be used when you need more than one block of code forexample
  
  ```js
  const upperizedNames = ["Farrin", "Nats", "Kats"].map(
  name => name.toUpperCase()
  return `${name}has ${name.length}characters in their name`;
  );
  ```
  
  Important things to keep in mind with the block syntax:
  
  - it uses curly braces to wrap the function body
  - and a `return` statement needs to be used to actually return something from the function.

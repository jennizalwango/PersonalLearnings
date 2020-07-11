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
  
  Sets 
  
  A set is an object that holds unique values or items. Its a collection of distinct items there is a difference between a set and an array. You can add, remove, loop over items in a set.
  
  - Sets are not indexed-based meaning you donot refer to tems in a set by thier position
  
  - Items in a set cannot be accessed individually.
    
    An example of a set
    
    ```js
    const person = new Set();
    console.log(person)
    ```
    
    Output
    
    ```js
    set{}
    ```
    
    The above code will give you an empty set becasue there are no items in the above set.
    
    Sets automatically remove duplication, Forexample;
    
    ```js
    const person = new Set("person1", "person2", "person3", "person2")
    console.log(person)
    ```
    
    Output
    
    ```js
    Set{"person1", "person2", "person3"}
    ```
    
    You can also check of the length of  a set using the `.size` property. This will return the number of items in a set. Forexample;
    
    ```js
    const person = new Set("person1", "person2", "person3", "person9")
    console.log(person.size);
    
    ///output
    4
    ```
    
    Since sets can not be accesses through indexing we w use the `.size` instead of the `.length`  property.  To check if an item exists in a ste we we use the `.has()` which returns either `false` or` true `depending if the item exists or not.
    
    Looping through sets
    
    Whn you sue the `.values`property it returns a new iterable object aclled `SetIterator` you can stor that iterator object in a variable and loop through each item using `.next()` 
    
    An example
    
    ```js
    const daysOftheWeek = new Set(["Monday", "Tuesday", "Wednseday", "Thursday", "Friday", "Sunday"
    ])
    const iterator = daysOftheWeek.values()
    iterator.next()
    
    ///output 
    object{value: "Monday", done: false}
    ```
    
    And if you run the `.next()`  again 
    
    ```js
    iterator.next()
    //output
    object{value: "Tuesday", done: false}
    ```
    
    And until the `done` equals `true` which marks the end of the set.
    
    However the easiet way to loop through a set is the `for ...of` Loop 
    
    eg 
    
    ```js
    const weekDays = new Set(["Monday", "Tuesday", "Wednseday", "Thursday", "Friday", "Sunday"
    ])
    for (const day of weekDays){
        console.log(weekDays);
    }
    ```

Maps

 Maps are collections of key values pairs, They hold unquies key values pairs.You could say sets are to arrays while maps are to objects. Maps are iterables which maens you can loop through them. Essentially a map is an object that lets you store key-value pairs where both keys and values can be objects.

```
Maps are to objects
Sets are to arrays
```

To create a Map you use the new keyword just like you do with sets 

```js
const animal = new Map();
console.log(animal);

///output its creates a new empty map with no key-value pairs
Map{}
```

Modifying Maps

Unlike sets you cannot create Maps from a list of values instead you add key values by using the Maps `.set()` method. forexample

```js
const animals = new Map()
animal.set('dog', {
    color: 'black',
    type: 'German shephard',
    name: 'pety'
},
'cat', {
    color: 'black and white',
    type: 'italians',
    name: 'savage');
console.log(animals);
```

The `.set()` method takes two arguments The first agruments is the key which is reference  to the second argument,  the value.  to remove key-value pairs use the `.delete()` Note that sets use `.clear()` to remove items from it while Maps use `.delete()` to remove items.

**TIP**

If you `.set()` a key-value pair to a Map that already uses the same key, you won’t receive an error, but the key-value pair will overwrite what currently exists in the Map. Also, if you try to `.delete()` a key-value that is not in a Map, you won’t receive an error, and the Map will remain unchanged.

The `.delete()` method returns `true` if a key-value pair is successfully deleted from the `Map` object, and `false` if unsuccessful. The return value of `.set()` is the `Map` object itself if successful.

Looping through Maps;

You can loop through a set in 3 different ways; 

1. Step through each key or value using the Map’s default iterator
   
       Using both the `.keys()` and the `.values() `helps you create a newiterator object called `MapIterator` You can store that iterator object in a new variable and use `.next()` to loop through  each key-value.

```js
   let iteratorObjForKeys = animals.keys();
   iteratorObjForKeys.next();


   ///output///

   object {value 'dog', done false}
```

   So you use the `.next()` to get the next value. And so on..

   On the other side use the `.vlaues` to access the   Map values , its the same process like for th `.keys()`

2. Loop through each key-value pair using the new `for...of` loop
3. Loop through each key-value pair using the Map’s `.forEach()` method

   Example

```js
animals.forEach((value, key)) => console.log(key, value);
```

Generators;

When a functoion is invoked the javascript function willl run everyline of code from  top to bottom. It doesnot stop untill the excution is done.This run time is called `run-to-completion`. Example

```js
function getEmployee(){
    console.log('the function has state');
const names = ['Amanda', 'Diego', 'Farrin']
for (const name of names){
    console.log(name);
}
console.log('the function has ended');
}
getEmployee();
```

Complier  is  acomputer program that changes source code into machince code, Running code through a complier changes its level of Abstraction. Transpling is also a grogram that runs to take your source of code into a target code, Just like a complier howvr jehere the source code and the target code are at the same level of Abstraction.
NB. the Babelrc file holds which presets {Preset are a number of plugins that are buldled togther } to be used and the  package.json file list all the dependenices that are to be installed.

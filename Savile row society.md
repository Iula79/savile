# Interview questions:

## What is the difference between classes and ID's in CSS?

The ID selector is unique while the class selector can be applied to many HTML elements

## What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

Resetting removes all styling from very elements, while normalizing means that elements should render consistently across browsers.

## Describe Floats and how they work.
Floats move an element to the side of the parent element. The elements that surround the float will wrap around it.

## What tools would you use to test your code's functionality?
 I would use unit tests and integration tests. Manual tests are also useful.

## What is the difference between a unit test and a functional/integration test?
Unit test  are specific for each language they are useful for example to get the data without making multiple calls to an API and making sure your code behaves the way you want, integration tests are made to interact with outside systems.

## What is the purpose of a code style linting tool?
It reduces syntax mistakes.

# Coding Questions:

## What is the value of foo?

var foo = 10 + '20';
This foo would be a string: '1020'. Javascript addition operator becomes a concatenation tool when used with strings. When combining numbers and strings it automatically treats numbers as strings.

## How would you make this work?

```
add(2, 5); // 7
add(2)(5); // 7
```

```
//creating a function that will take an array and perform a sum operation to all the elements of the array:

var sum = function(arr) {
    return arr.reduce(function(a,b) {
        return a+b;
        }
    );
};
}


var addingElements = function() {
    // arguments is an object, Array.from returns arrays from array like elements
    var arg = Array.from(arguments)
    // testing limit case in which the first argument is not defined
    if (arg.length === 0) {
         arg = [0]
    }
    // creating an inner function that will take a second argument and add it to the sum of the arguments of the main one
    var inner = function(b) {
        //testing limit case in which the second argument is not defined
        if (b !== undefined){
          return sum(arg) + b
      }
    }
    return inner
}
```
## What value is returned from the following statement?

`"i'm a lasagna hog".split("").reverse().join("");`

It would return `"goh angasal a m/'i"`. This is javascript reverse method that is used on strings, by transforming the characters into elements of an array, reversing them and joining them back into strings

## What is the value of window.foo?

`( window.foo || ( window.foo = "bar" ) );`
The value is "bar" because the variable foo is not defined therefore window.foo is false.

## What is the outcome of the two alerts below?
```
var foo = "Hello";
(function() {
  var bar = " World";
  alert(foo + bar);
})();
alert(foo + bar);
```

The first alert returns Hello World.
The second one returns "ReferenceError: bar is not defined" because the second alert does not have access to the value bar as it lives only in the scope of the function above

## What is the value of foo.length?

```
var foo = [];
foo.push(1);
foo.push(2);
```
`foo.length = 2`, because arrays in Javascript are flexible elements that can be expanded (or reduced) by pushing elements to it. This is not true for every language.

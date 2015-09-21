
-- JavaScript Basics --

So you want to start with JQuery?  Since Jquery is build on top of JavaScript (i.e., JS), it is important to review some of the basic components of JS.

Variable --
JS is built up of variables.  Variables are ways to store values.  Think of them as containers, that we can store many types of values into - text (strings), numbers, and more complex data.

  To create a variable, we use the key work 'var' and declare it in a statement, such as
    var myFood = 'pizza';
  You can call your variable pretty much anything, as long as it doesn't start with a number or have a hyphen in it.

  Whenever you want to use that function, you have to 'call' or 'invoke' it.
    console.log( myFood ); // would produce 'pizza'

Functions --
Functions are another piece that makes of JS. They give life and functionality to JS programs.

  Functions are created different ways.  One of the simplest is to just use the key word 'function' followed by the code.  In order to use the function, we can put it in a variable.
    Sample -
      var multiplyTwoNumbers = function (x, y) {
        return x * y;
      }
  In the above examples, x and y are known as arguments.  This function multiples the 2 arguments that are passed into it.  To do that, we can do
    console.log( multiplyTwoNumbers(2, 8) );  // 16

  Another way to created the function is to use a function declaration.
    function multiplyTwoNumbers(x,y) { return x*y };}

  Of the two ways, the first can help avoid problems with scope and hoisting.

  Scoping -
  When you create variable inside a function, it is only available inside of that function.  This is usually preferred to than to create a variable outside a function, where it is considered global.
    * It is important to note that variables created inside of a function without a var statement are considered global -- this is generally frowned upon.

Objects --
Objects are everywhere in JS.  The things that aren't objects are considered primitive values -- strings, booleans, numbers, undefined and null.
Objects have properties, and properties have values.  This is known as key-value pairs.  Objects are created with {} surrounding the key-value pairs.
  Example, -- this is object literal notation/syntax
    var monster = {
      firstName : 'Cookie',
      faveFood : 'cookies'
    };

To access the properties inside the object, we can use dot or bracket notation.
  monster.firstName
  monster['faveFood']

Object properties can also be modified very easily.
  monster.firstName = 'Dracula';
  monster.faveFood = 'blood';

Object methods --
Methods are properties inside objects that are functions.

this --
'this' is a special keyword.  Inside any function or method, it refers to the object in the context in which it was used.

  'This' can be very confusing. Since it refers to the context in which it is used, that context can change depending on where the function is being called.
    * the .call() and .apply() method are used when changing contexts to the window object to keep the 'this' inside a function intact.

Objects in jQuery --
When using jQuery, 'this' refers to the element on which you bind an event handler; or the current element in an iteration of a set of elements.

Array --
Arrays are a type of object to store a set of values.  Arrays are created usually by the array literal.
  sample:
    var myArray = [1, 2, 3];

  They are indexed with bracket notation, starting at zero.
  So, myArray[0] = 1
  Arrays have a length property.
  myArray.length = 3

  Looping over Arrays - the For loop
    for (i = 0; i < myArray.length; i++) {
      log ( 'item at index ' + i + ' is ' myArray[i]');
    }

Logic / Truthiness --

If / Else / Ternary operators: In JS, we can use these statements to see if something is true or false.  This refers to 'truthy' or 'falsy' values. When you want to test to see if a value is 'falsy', you can use the ! operator.

Logical Operators --
  These operators evaluate statements.
  && - this operator checks to see that both sides are true
  || - this operator checks to see that either side is true

  This operator can be used to control code execution.  They will short circuit the statement if the first operation breaks the statement.

Ternary Operator -- (?)
  These oprators allow you to set a value depending on which condition is true in a statement.

  Sample:
    var propertyName = (dim === 'width') ? 'clientWidth' : clientHeight''
      > here if the statement is true, then the first value is used, however, if not, then the second value is used for propertyName

Gotchas -
  There a few things to keep in mind.  First, beware of reserved words for naming conventions.  Using $ typically refers to jQuery names, and using _ to start usually refers to a private name.

  Typing - JS is loosely typed. This means that working with numbers and strings can cause some issues when doing math operations.  Be aware if getting strange results that you may have a typing error.






























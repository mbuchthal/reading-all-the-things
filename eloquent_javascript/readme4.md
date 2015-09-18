Chapter 4 - Data Structures: Objects and Arrays

Arrays - data sets that are created for storing sequences of values.
  * Arrays are created with []
  * They are zero indexed - i.e, the first value is array[0]

Properties - all JS values have properties.
  * The 2 most common ways to access JS are with dot or square brackets
    > Using [], the expression is evaluated to get the property name.
      - may need to use quotes when getting a string
    > using dot, the value is 'fetched' and uses the result as a property name

Thus, to get the property of .length, you could obtain that by using value.length (dot notation).

Methods - both string and array objects contain a number of other properties that refer to function values (in addition to length).
  * toUpperCase(), toLowerCase()
  * arrays have methods such as push(), pop(), - add/remove elements from the end of arrays.
     > shift(), unshift() - for removing and adding things to the start of an array
     > indexOf(), lastIndexOf()
     > slice(), concat()
  * values of string, number, Boolean - are not objects and new properties cannot be create don them

Objects - arbitrary collections of properties that can be added or removed.
  * Different ways to create an object.  One way is {} notation.
    - var day1 = {
        squirrel: false,
        event: ["work", "touched tree"]
  };
  * Arrays are a specializedkind of object for storing sequences of things. typeof array = object.

Mutability -
Values such as numbers, strings, and Booleans are immutable - impossible to change an existing value of those types.
Objects are mutable - they can be changed.

Objects as Maps:
A way to store correlations in an array, using objects with name/value properties. A Map is a way to go from values in one domain to corresponding values in another domain.

Arguments Object:
Whenever a function is called, a special variable named 'arguments' is added to the environment in which the function body runs
  * arguments object has a length property
  * is not an array (no other array methods)

Math Object:
There are number of utiliy functions
  * Math.max, Math.min, Math.sqrt, others...
  * only one Math object

Global Object:
The space in which global variables live.  Each global variable is present of the property of this object.  in browsers, the global scope object is stored in the 'window' variable.


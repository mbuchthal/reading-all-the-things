Chapter 5 - Higher Order Functions

Abstraction -
Sometimes a function can be written in different ways.  Sometimes it's easier to write a function in a much shorter way.  This can also help prevent making mistakes by having to write less code.

Higher Order Functions -
Functions that take other functions as arguments or return other functions are higher order functions.

  example:
  functions greaterThan(n) {
    return function(m) { return m > 3; }
  }
  var greaterThan10 = greaterThan(10);
  console.log(greaterThan10(11)); --> true

This function is actually returning a new function.

the apply method - javascript allows you to use the apply method.  when passing it an array of arguments, it will call the function with those arguments.

JSON - JavaScript Object Notation
  * This is a way similar to the notation of JS array and objects with a few restrictions.
    - all property names have to be surrounded by double quotes and only simple data expressions allowed.

  * There are 2 functions JSON.stringify and JSON.parse that transform data to and from this notation
    - .stringify takes a JS value and returns JSON
    - .parse is the opposite - it changes a JSON object into a string

Filter --
This explanation seems to complicate the arr.filter method on MDN.
But basically, if the array being passed as an argument passes the test(function) it will be pushed to a new array, thus filtering the previous array.  The original array is not mutated and left intact.

  function filter(array, test) {
    var passed = [];
    for (var i = 0; i < array.length; i++) {
      if (test(array[i]))
        passed.push(array[i]);
    }
    return passed;

Transforming with Map --
Map trafnsformd an array by applying a function to all elements of the array and building a new array from the new value - hence, mapping the array through the function.

  function map(array, transform) {
    var mapped = [];
      for (var i = 0; i < array.length; i++)
        mapped.push(transform(array[i]));
      return mapped;
    }
  var overNinety = ancestry.filter(function(person) {
    return person.died - person.born > 90;
  });
  console.log(map(overNinety, function(person) {
    return person.name;
  }));

Summarizing with Reduce --
Reduce computes a single value from an array
  function reduce(array, combine, start) {
  var current = start;
  for (var i = 0; i < array.length; i++)
    current = combine(current, array[i]);
  return current;
  }
  console.log(reduce([1, 2, 3, 4], function(a, b) {
    return a + b;
  }, 0));
  // → 10

Using these higher order functions can make writing new functions much easier, especially when you have to use multiple methods to find a return value.

Bind --
All functions have a bind method - which creates a new function that will call the original function but with some of the arguments fixed.
  * Common use - Bind can be used to make a function that has a particular this value.
  * Common use - can be used to make functions with pre-specified specific arguments






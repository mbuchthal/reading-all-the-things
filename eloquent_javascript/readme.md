
Chapter 1 - Values, Types, and Operators

There are 6 basic types of values in JS - numbers, strings, Booleans, objects, functions, and undefined values.

Numbers -- JS can store a number value up to 9 quadrillion (15 zeroes)!
  * Special numbers --> Infinity, -Infinity, NaN (not a number but number type)

Strings - used to represent text and written by enclosing in quotes
  * escaping a character ( by using a \ ) will exclude the next letter in the quote
    > followed by a 'n' newline
    > followed by a 't' tab
  * unary operators - such as 'typeof' - produce string values

Boolean Values - true/false
  * strings/numbers can be compared to result in boolean
  * NaN != NaN
  * logical operators -- && (and), || (or)
  * (!) is a unary operator for 'not'
  * ternary operators (conditional operator)- written with a ? and a :
    > (true ? 1 : 2); --> 1
    > (false ? 1 : 2); --> 2

Undefined Values -- null, undefined.  They are used to represent the absence of meaningful value.

Type Conversion/Coercion - JS will go out of its way to change the type of value to a correct type in order to complete a comparison or computation.
  * For example, substracting the number 1 from the string "5" --> will result in the number 4.
  * addition operators, === and !==, will compare precise values without type coercion

Short-Circuiting of Operators -- operators && and || can be used to 'short-circuit'.
  * In &&, if the left hand equation is false, then the right hand equation would not even be processed.
  * In ||, if the left hand question is true, likewise.




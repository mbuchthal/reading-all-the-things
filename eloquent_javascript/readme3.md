
Chapter 3 - Functions

Defining Functions:
  Functions can be defined similarly to a variable; however, the value given would be a function instead - i.e., starts with the key work 'function'.
  Functions take parameters - like variables, where the initial values are given by the call of the function.
    i.e., var xyz = function () {...}

  Variables declared inside a function are 'local' rather than 'global.'  This means they are accessible only to the function in which they are called.  This same rule is applied to functions nested within other functions.

  Functions can also be declared without the 'var' keyword.  This is a function declaration
    i.e., function xyz() = {...}

Call Stack - The control flow of the program is called the call stack.  When a function is run, it is on the top of the call stack, and when it returns a value it is removed from the stack.

Optional Arguments - Extra arguments that are passed into a function are ignored.  It is not required to have the exact number of arguments matching the parameters.

These next 2 concepts need to be re-read several times to undersant.

Closure:
  The ability to reference a specific instance of a local variable in an enclosing function.  It 'closes over' some local variable.

    Example of this --

      function multiplier(factor) {
        return function(number) {
          return number * factor;
        };
      }
      var twice = multipler(2);
      console.log(twice(5));  ---> 10

Recursion:
  A recursive function is one that calls itself

    Example --

    function power (base, exponent) {
      if (exponenent == 0)
        return 1;
      else
        return base * power(base, exponent-1);
    }
    console.log(power(2,3)); ---> 8

Recursion can be more 'elegant' but can create performance concerns, when having to repeatedly call function many times over (vs. looping).  If too slow, may need to exchange elegance for efficiently

Growing Functions:
  *  Keep your code DRY - dont repeat yourself; if you are repeating your code, there may be an opportunity to create a function.
  *  Sometimes, you want to build functionality from the start.

Functions and Side Effects:
  * A pure function - one that has no side effects and does not rely on the side effects from other code.  It would always produce the same value if called with the same arguments










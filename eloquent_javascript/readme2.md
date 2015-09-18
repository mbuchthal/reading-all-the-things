Chapter 2 - Program Structure

Expressions - fragment of code that produces value
Statements - stands on its own and amounts to something only if it affects the world

Variables
  * valid names can be any word not Reserved Words
    - no need to memorize all reserved words but be aware that they might be a problem if variable definition does not work
  * may not include spaces
  * not start witha  digit
  * punctuation okay except for $ and _

The Environment - the collection of variables and their values that exist a at given time.

Function - a piece of program wrapped in a value
  * executing a function -- invoking, calling, applying

Console.log
Return values -- anytime a function produces a value
Prompt - returns a string/Confirm - returns boolean

Control Flow - statements are executed top to bottom.

  * Conditional Execution, different routes based on a boolean value

  * While and Do Loops - A do loop always ezecutes its body at least once and then starts testing the conditional.  A while loop tests the conditional prior to executing the body.

  For Loops -
    var result = 1;
    for (var counter = 0; counter < 10; counter = counter + 1)
    result = result * 2;
    console.log(result);
    // → 1024

  Breaking Out of a Loop -
    * have the condition produce 'false'
    * use a 'break' statement

  Updating variable
    * (counter = counter + 1) is the same as (counter += 1)

Switch statements - sometimes used instead of multiple 'if' statements; remember to use 'break'


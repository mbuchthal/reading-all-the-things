
-- Javascript: The Good Parts --

Inheritance: JS is a protypal language - objects inherit directly from other objects.

Pseudoclassical: Every function gets a prototype object because the language does not provide a way of determining which functions are intended to be used as constructors.

  'method' method: (this allows an object to be created in a cascading style)
    Function.method('inherits', function (Parent) {
      this.prototype = new Parent();
      return this;
    });
    ex.:
    var Cat = function (name) {
      this.name = name;
      this.saying = 'meow';
    }.
      inherits(Mammal). // inheriting through the 'method' method.
      method('purr', function (n) {
        // DO SOMETHING
      }).
      method('get_name', function () {
        // DO SOMETHING
      }).

  Convention has all constructor functions named with a capital letter.  Forgetting to use the 'new' keyword will cause problems.  Suggestion - avoid using the new keyword altogether.

Prototypal: a new object can inherit the properties of an old object.
  var myMammal = {...};
  var myCat = Object.create(myMammal) {...};

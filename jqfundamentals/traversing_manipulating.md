
-- Traversing & Manipulating --

Traversing refers to moving through the HTML elements on the DOM page.  We can replace or edit the original content by adding or substracting the content.

Filtering --

Some useful methods to use while traversing the DOM include .filter(), .not(), .has().

  .filter() -- this filters through the variable and returns only those that have filtered selection.

  .not() -- filters only items that dont have the filtered element.

  .has() -- filters only items that contain the certain criteria

You can also find elements that relate to the initial selection:

  .first() - would return the first selected item on the page.

  .sibling() - would return the siblings of the selected items on the page.

  .parent() - would return the selected item's parent.

  .children() - selected the immediate children of the selected item.

  .find() - finds all the criteria in the selection including any nested ones.

  .parents() - finds all ancestors of the selected item's criteria

  .closest() - finds the closest ancestor that has the criteria

  .add() - you can add to the existing selectino by passing it a selector an array of elements, a string, or a jquery object


When you are traversing elements, sometimes you will want to go back to the original element that was selected.

  .end() - will stop the traversing and go back to the original selection in the statement.
    * Using this might indicate too long of a chain however.

  .addback() - this method allows you to work with the original selection AND the selected element.

Manipulation -- jQuery is magical. It allows you change the DOM much easier than native JS.  All of these methods return the same jQuery object on which they were called.  They can be chained/combined with the above methods as well.

  Altering --

    Classes - You can add or remove classes with jQuery.
      .addClass()
      .removeClass()
      .toggleClass() - adds if not there, or removes if it is present

    Style - While using CSS directly is preferable, you can style using jquery as well.
      .css() -- You can style the page directly with this method, but should mostly be used for styles that hve to be calculated.

    Changing form values - With jQuery, you can also change the values of form elements using the .val()
      .val() - can alter form elements such as select and input.
      .prop() - can alter the checkbox on an input
        * $('input[type="checkbox"]').prop('checked', 'checked');

    Changing other attributes
      .attr() - This method is used to change other attributes (i.e., href)
        Example:
          $('a').attr('href', function(index, value) {
              return value = '?special=true';
            });
      .removeAttr() - This will remove an attribue all together.

    Getting information from elements -- Both the .val() and .css() methods can be used to get and set the values of the elements.
      It is important to note that when you get the value, only the first element is effected.


    Placing items in the document -- Once selected, you can move it in the document.

    These are all methods to move items into a place on the DOM

      appendTo(). - takes an item and appends a place
      append(). - takes a place and appends an item to it

      insertAfter(). - inserts after the selected item
      .after().

    It is important to note that there are many ways to place an element, and it is the context of the code which will determine which one you use.

    Copying Elements -- You can use the .clone() method to copy an element.
      * if the element has an id, the clones will also have an id unless you remove it.

    Removing Elements -- There are a few ways to remove elements with jQuery.
      .remove() - This method removes an element permanently.
      .detach() - Unlike .remove(), this method will allow an element to retain it's event handlers if re-added later
      .replaceWith() - This method replaces an element with an element or HTML passed to it.  Does not retain anything form the replaced element.






























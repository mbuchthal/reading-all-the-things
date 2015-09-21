
-- jQuery Basics --

jQuery makes it easier to manipulate a page of HTML.

- $ -
the $ is a short notation for 'jQuery' when selecting DOM items.  Using $ creates a jQuery object.

$(document).ready()
  An anonymous function that creates a jQuery object from the page 'document', and then passing the .ready() function.  This allows the page to be manipulated by jQuery.

  * shorthand version --
    $(function() {});

Getting Elements --

The easiest task to do with jQuery.  You can use CSS selectors to pick an object from the page.
  $('#header') -- will get element with ID of header.
  $('.classOne') -- will pick element with class of classOne
You can create variables to hold these elements just by making a variable declaration.  var myElem = $('li');

Other ways to create jQuery object --
There are other ways to create jquery object other than passing a selector.
  * You can create an object from the DOM
    $(document.body.children[0]);
  * From a list of DOM elements
    $([window, document]);
  * From the context of a DOM element
    var firstBodyChild = document.body.children[0];
    $( 'li', firstBodyChild)
  * From a previous selection
    var para = $('p');
    $( 'a', para);

Objects are created by jQuery regardless of whether the selection is found. You can use a truthy test to see if there is an element.
  if ( $( '#nonexistent' ).length ) {};

In order to select a single item from a group of elements:
.eq() - This method allows you to select a single element from passing it an index.
  var listItems = $( 'li' );
  var secondListItem = listItems.eq( 1 );
  secondListItem.remove();

Creating new Elements --

In jQuery, you can also create elements with $ - by passing it an html snippet.
  For example, $('<p>'), would create a new <p> element.  You can also use this to create the content and give classes.
  Not only that, but you can create it like an object:
    $('<p>', {
      html: 'Hello!',
      'class': 'greet'
    });

Working with selections -

Once you select an object, you can test the selection.  The most common method is to use .is().

Getters and setters:
  Getters get information from a selection, and setters will alter them.
  Getters will usually only operate on the first item in a selection and setters typically change all elements ina  selection through implicit iteration.
    * Implicit iteration is where jQuery automatically iterates over all elements.

  Explicit iteration - You can use the .each() method to explicitly iterate over a selection.
    sample:
      $('li').each(function(index,elem) {
        $(elem).prepend('<b>' + index + ': </b>')
      });

Chaining --
jQuery allows you to chain multple methods together without having to repeat the selector. Chaining is very useful be careful about chaing so much that the code becomes difficult to read.









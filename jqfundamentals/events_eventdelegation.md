
-- Events and Event Delegation --

jQuery makes event handling much easier than native JS.
There are many methods that bind events to a native event.
Most of these are shorthand for the .on() method.

Using the .trigger() method, you can trigger an event that is already bound with an event handler.

.off() - This method will unbind an event and any event handlers.

Namespacing Events - Using .on() allows you to use namespaced events.
  $('li').on('click.logging', function() {
    console.log('...');
  })
  $('li').off('click.logging')...

This is useful when you don't want to unbind ALL events that are linked to an element.

Binding multiple events --
Using .on() also allows you to bind multiple events on the same element.

Passing named functions as event handlers - You can create a function outside the event handler and then pass it in and tie it to the event.

Event object -
Every event that is created actually creates an object which has properties.

Preventing Default --
event.preventDefault()
This is to be used to prevent events to be called when doing a behavior.

Event Bubbling -
When you click on an element that's nested inside other elements, the event is actually being clicked on all those elements.
  To stop this from happening, you can use the .stopPropagation() on the event object.

Event Delegation - This allows us to bind events to high-level elements and through bubbling, reach low-level elements.
  Example,
    $('#my-ul').on('click', 'li', function(e) {
      console.log( this ); // logs the li that was clicked
    });
    $('<li>a new list item</li>').appendTo('#my-ul');

  This allows us to bind fewer events than if we had to bind low-level elements, and also bind higher level events even if the higher level event changges.

























-- Effects --

jQuery can be used to add effects to your page and create custom animations of arbitrary CSS elements.
  * That beind said, it usually is more efficient to create animations with CSS than JS.
    jQuery.fx.off - for low res devices, this turns off the animations and set them to the end state.

Here are some of the more common effects built into jQuery. Most of these are self-explanatory.

  .show()
  .hide()
  .fadeIn()
  .fadeOut()
  .slideDown()
  .slideUp()
  .slideToggle() - This method shows or hides

You can specify the time of effect in milliseconds or use a predefined speed.
  $('hidden').show(300) or $('hidden').show('slow')
    * Note: the predefined speeds can be reset with the .jQuery.fx.speeds method
      - jQuery.fx.speeds.turtle = 3000;

Using a callback function, you can specify an action for the animation to take once it is complete.

Customer effects with .animate()

.animate() takes 3 arguments.
  * defined object to be animated
  * duration
  * callback function

  Example -

    $('.funtimes').animate({
      left: '+=50',  // increase by 50
      opacisty: 0.25,
      fontSize: '12px'
      },
      300,
      function() {
        // executes when animation is done
      }
    );

Managing Animations - These methods are used to manage animations.

  .stop() - will stop animations of selected element
  .delay() - This method causes the animation to wait before acting.





















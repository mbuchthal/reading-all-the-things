
-- AJAX & Deferreds --

Ajax - 'asynchronous JS and XML' - basically means that you can load information from a server without having to restart or reload the browser.

jQuery has an $.ajax method.

Two ways to use $.ajax()

FIRST METHOD --

  * We can pass a configuration object as an argument

// these creat 'callback functions' that will be invoked when...
// ... the AJAX request is successful
    var updatePage = function(res) {
      $('#target').html(res.people[0].name);
    };

//... the AJAX request fails
    var printError = function(req, status, err) {
      console.log('something went wrong', status, err);
    };

//  Create an object to describe the AJAX request
    var ajaxOptions = {
      url: '/data/people.json',
      dataType: 'json',
      success: updatePage,
      error: printError
    };

//  Initiate the request
    $.ajax(ajaxOptions);

SIMPLIFIED into an object literal --

$.ajax({
  url: '/data/people.json',
  dataType: 'json',
  success: function(resp) {
    $('#target').html(resp.people[0].name);
  },
  error: function(req, status, err) {
    console.log*('something went wrong', status, err);
  }
});

SECOND METHOD --

  * We can pass a URL and an optional configuration object.
      This is most useful if you want to use default configuration or if you want to use the same configuration for several URLs.

  $.ajax('/data/people.json', {
    type: 'GET',
    dataType: 'json',
    success: function( resp ) {
      console.log( resp.people );
    },
    error: function( req, status, err ) {
      console.log( 'something went wrong', status, err );
    }
  });

Asynchronous -

JSON - JSON is a string representation of data that appears like a JS object.  JSON cant represent function or date objects.
  * it must be parsed into a JS object before working with it -- JSON.parse().


Convenience - if you dont care about errors, jquery offers some basic methods for convenience

  $.get( '/data/people.html', function( html ){
    $( '#target' ).html( html );
  });

  $.post( '/data/save', { name: 'Rebecca' }, function( resp ) {
    console.log( resp );
  });

Sending date / Working with forms -

  $( 'form' ).submit(function( event ) {
    event.preventDefault();

    var form = $( this );

    $.ajax({
      type: 'POST',
      url: '/data/save',
      data: form.serialize(),
      dataType: 'json',
      success: function( resp ) {
        console.log( resp );
      }
    });
  });

  * the .serialize() method is for taking form input and converting it into a string format

jsXHR -- jquery XML HTTP Request -- are return from .ajax().  They can be captured in a variable.

  .then() - this method makes use of the jqXHR object to attach success and error callbacks.

  .always() - method will run on success or failure of the request object

JSONP - (json with padding) - allows you to use data even if hosted on another server.  Browsers often block XHR's to other domains for security reasons.
  * jQuery lets you make JSONP request with $.ajax() by specifiying 'jsonp' as the dataType
    $.ajax({
      url: '/data/search.jsonp',
      data: { q: 'a' },
      dataType: 'jsonp',
      success: function( resp ) {
        $( '#target' ).html( 'Results: ' + resp.results.length );
      }
    });

  $.getJSON() - can be used to make a JSONP request


Deferreds --
  Deferreds allow you to manage asynchronous code.
  You can make your own deferreds by using $.Deferred().

  These are methods that can be attached to success/error handlers on a promise.
    .then()
    .done()
    .fail()
    .always()

  .pipe() - this method reacts to resolution of asynchronous operation by manipulation of value it returns and creating a new deferred.

    function doSomethingLater( fn, time ) {
      var dfd = $.Deferred();

      setTimeout(function() {
        dfd.resolve( fn() );
      }, time || 0);

      return dfd.promise();
    }

    var dfd = doSomethingLater(function() { return 1; }, 100);

    dfd
      .pipe(function(resp) { return resp + ' ' + resp; })
      .done(function(upperCaseResp) {
        $( '#target' ).html( upperCaseResp );
      });

  .when() - if we don't know if an operation will be asynchronous, we can use this method to react to either case
    * can take more than one argument.
    * when a jqXHR is one of the arguments, we get an array of arguments passed to our callback.









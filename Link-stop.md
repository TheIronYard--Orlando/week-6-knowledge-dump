How can you make clicking a link do something other than take the user to
another page, or keep a form from being submitted to a server?

Options that surround the click event is:
1. One way to use a link is inside of a page. By putting: <a name="top"></a>
in your HTML at the top of the body.
Then, placing: <a href="#top">Back to top of page</a> at the bottom
will then call back to the top page without the need to scroll or re-load.

2. clicking on a link that has the "hover" element will then call
the "hidden" object to become visible. All of this can be done in CSS.

3. The example below shows how you can prevent a
link from doing it's default work. In this case, it
prevents it and logs it below the link with a message.
This will also prevent the form it may be attached to from
being passed to the server.


<script>
$( "a" ).click(function( event ) {
  event.preventDefault();
  $( "<div>" )
    .append( "default " + event.type + " prevented" )
    .appendTo( "#log" );
});
</script>

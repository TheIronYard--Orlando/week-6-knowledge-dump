How do we make things "pretty"?

There are millions of different combinations of how to make "things" pretty.
A list of css properties can quickly get overwhelming:
color
opacity
background(color/blend/position)
border(size/color/radius)
display
padding

Most (if not all) of these can also be passed through in Javascript.

 But, there are other methods of making a site look better. One JS method
 involves taking objects that are set (in CSS) to a relative position,
 then writing JS code similar to this:

 function myMove() {
    var elem = document.getElementById("myAnimation");
    var pos = 0;
    var id = setInterval(frame, 10);
    function frame() {
        if (pos == 350) {
            clearInterval(id);
        } else {
            pos++;
            elem.style.top = pos + 'px';
            elem.style.left = pos + 'px';
        }
    }
}
This moves the object across the page slowly, making it look "animated".

Masonry is a grid layout library that is based on available vertical space.
You feed it into JS and also into HTML, set some parameters,
and it feeds into the grid.      (http://masonry.desandro.com/)

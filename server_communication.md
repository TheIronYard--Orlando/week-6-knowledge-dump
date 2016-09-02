#Server Communication

I believe our first interaction with AJAX (Asynchronous JavaScript And XML) was during our Etsy Search Page Assignment. We had to create our own API token by signing up as an Etsy developer. Next, we created a function that made an AJAX request to the Etsy API. Once that was finished, we could search for whatever we wanted and results would come back. It was pretty cool!

AJAX allows the user to load data in the background and display it on a webpage, without refreshing the page. Web applications, using AJAX, can send data to and retrieve from a server asynchronously without interfering with the display and behavior of the page. As a result, the user can create websites with much richer functionality. Web applications like Gmail and Google Maps uses AJAX extensively. Modern implementations commonly substitute JSON for XML due to the advantages of being native to JavaScript. Ajax requests are triggered by JavaScript code.

There are some drawbacks to AJAX, but jQuery fortunately helps out. Different browsers implement AJAX API differently. Normally, that would mean developers would have to account for all the different browsers to ensure AJAX works universally. Luckily, jQuery provides support that abstracts away the browser differences. $.ajax() is a full-featured method, and convenience methods such as $.get(), $.getJSON(), and $.post().

The conventional model for a Web Application versus an application using Ajax:

![Image of AJAX_graph]
(http://i65.tinypic.com/350weie.png)

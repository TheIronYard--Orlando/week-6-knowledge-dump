A closure is a function with access to its own private variables. No other function is aware of these variables and cannot access them. A closure has access not only to its own local variables but to globals as well.

Because functions create a local scope by their nature, we can use that to create closures.

Here's an example.

  function makeBirdCounter() {
    var count = 0;
    return function() {
      count ++;
      return `${count} birds`
    }
  }

Now we can access the anonymous function within makeBirdCounter() by assigning a variable to the outer function.

  var birdCounter = makeBirdCounter();

The reason I assigned a variable instead of just invoking the outer function whenever needed is because the latter would reset count to 0 every time.


Now I don't need to use a global variable to track the count. This helps to reduce clutter in the global namespace as well as preventing some other part of my application from using the global count variable and screwing up my birds count.

Here's another useful feature:

  var birdCounter2 = makeBirdCounter();

The above code won't break my application. That's because every time the outer function is invoked, a new scope is created. Now I can track birds by type or color or whatever and not run into interference among the different counters.

Where are closures used in the real world?

* jQuery
* Moment.js
* Underscore.js

Many languages and libraries use closures to prevent variable conflict.

Here's an example of how "pollution" of the global namespace can lead to problems in your code:

  var buttons = document.getElementsByTagName('button');

  for (var i = 0; i < buttons.length; i ++) {
    var buttons = buttons[i];
    var buttonName = button.innerHTML;
    button.addEventListener('click', createHandler(buttonName));
  }

This will attach a listener to each button but it will assign the last button name to each button. That's because 'i' is hoisted to the global scope right away. This particular problem can be solved by using let instead of var in the for loop declaration of 'i'.

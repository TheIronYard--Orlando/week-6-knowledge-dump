#Asynchronous Programming

What is Asynchronous Programming you might ask? It is a means of parallel programming in which a unit of work runs separately from the main application thread and notifies the calling thread of it's completion, failure or progress. I'm not sure about you, but that is confusing to me. Let's first explain synchronous and then asynchronous.

Synchronous programming is a bunch of statements in a sequence. Each statement in your code is executed one after other. Coding this way has the potential to block further execution until it has finished. Long running JS functions can make the UI or server unresponsive until the function has returned. As a result, this can cause a horrible user experience.  Asynchronous code takes statements outside of the main program flow, allowing the code after the asynchronous call to be executed immediately.

Summary: Synchronous code is executed in sequence, each statement waits for the previous statement to finish before executing. Asynchronous code doesn’t have to wait, your program can continue to run. You do this to keep your site or app responsive, reducing waiting time for the user.

Synchronous vs Asynchronous

![Image of Synchronous_vs_Asynchronous]
(http://i68.tinypic.com/2jdy7c.png)

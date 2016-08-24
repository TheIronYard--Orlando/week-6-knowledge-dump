Using a css preprocessor is a good way to keep your style code maintainable and to easily "create" a css file for production. What I mean by "create" is that you will basically turn a bunch of css and css-related language code into one css file.

That is useful because it prevents the browser from having to load multiple style files. Sass and Less are two of the most popular processors currently in use. They are not just useful because of their code compilation. They have several tools to help keep code readable and maintainable. These include:

* variables
* mixins
* functions
* 'extends' syntax

These allow a user to write less code by reusing features and attaching new styles to existing content by using it as a starting point. It's also easy to keep multiple style files because you can import them into one another.

To manage all of this and keep it automated, these preprocessors have a watch capability, meaning they can automatically compile your code into usable css every time you save a change.

For example, when using sass you can run:

  sass -w <scss file(s)> <css file to write to>

And that will give me a useable css file. So I started with a bunch of scss files that depend on one another and are written in a language that, although it resembles css, is not recognizable by the browser. And I ended with one css file that perfectly implements the logic I wrote in my sass files. And it will recompile every time I make a change and save it. Pretty cool!

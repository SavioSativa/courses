<section class="module-section" name="Functions With Multiple Parameters">&nbsp;</section>

##  Functions With Multiple Parameters

_What if we needed to pass in multiple values to a function?_

We can do this simply by declaring a function that has multiple parameters, each with a unique descriptive name.

    function sayGreeting(greeting, name) {
        // Add a space between greeting and name.
        console.log(greeting + " " + name + "!");
    };

    sayGreeting("Hello there", "Tom");

It is as simple as that! What if we don't pass one of the parameters an argument? Try it for yourself and reflect on the result.

_What order does the function accept arguments? Try `sayGreeting("Tom")` and `sayGreeting("Hello there")`._


<section class="module-section" name="Anonymous Functions">&nbsp;</section>

## Anonymous Functions

We can declare **anonymous functions** without giving them a name. These functions are not called immediately by default and must be saved somehow for later use or passed through to be used as an argument for another function.

    (function(a, b) {
    	// Add a space between greeting and name.
    	var formattedGreeting = a + " " + b + "!";
    	console.log(formattedGreeting);
    });

Saved as a variable for later use:

    var a = (function(a, b) {
    	// Add a space between greeting and name.
    	var formattedGreeting = a + " " + b + "!";
    	console.log(formattedGreeting);
    });

    a("Hello", "Tom");

or

    var a = function(a, b) {
    	// Add a space between greeting and name.
    	var formattedGreeting = a + " " + b + "!";
    	console.log(formattedGreeting);
    };

    a("Hello", "Tom");

> Anonymous functions can be self executing!

    (function(a, b) {
    	// Add a space between greeting and name.
    	var formattedGreeting = a + " " + b + "!";
    	console.log(formattedGreeting);
    })();

> There is an issue here! The variables a and b do not have any values! Why do you think this happened?

    (function(a, b) {
    	// Add a space between greeting and name.
    	var formattedGreeting = a + " " + b + "!";
    	console.log(formattedGreeting);
    })("Hello", "Tom");


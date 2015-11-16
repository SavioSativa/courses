<section class="module-section" name="Functions as Arguments">&nbsp;</section>

## Functions as Arguments

As mentioned before, functions can be passed as an *argument to another function*! The function that gets passed in is a local version of the function that can be used just like a regular function.

    function createGreeting(greeting, name) {
    	// Add a space between greeting and name.
    	var formattedGreeting = greeting + " " + name + "!";
        return formattedGreeting;
    };

    function sayGreeting(greetingCreator) {
        console.log(greetingCreator);
    };

    sayGreeting(createGreeting("Hello", "Tom"));
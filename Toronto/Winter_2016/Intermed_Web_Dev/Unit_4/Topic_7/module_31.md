<section class="module-section" name="Scope">&nbsp;</section>

## Scope

There are cases in some languages where **scope** can be figured out dynamically. JavaScript is one of those languages!

_Let's look at a quick example!_

    function createGreeting(greeting, name) {
    	// Add a space between greeting and name.
    	formattedGreeting = greeting + " " + name + "!";
    	return formattedGreeting;
    };

    var greeting = createGreeting("Hello", "Tom");

    console.log(greeting);
    console.log(formattedGreeting);

This looks very similar to the old example we had where we tried to access a variable created in a function with **local scope**, which gave a reference error when trying to log it outside of the function.

However, in this example we can see no keyword `var` was used! When JavaScript comes across this situation, it will look back through the different layers of scope until it finds an instance of that variable. If it does not find one, it will create one with **global scope** dynamically.


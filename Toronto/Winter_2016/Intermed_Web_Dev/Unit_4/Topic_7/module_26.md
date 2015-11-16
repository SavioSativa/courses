<section class="module-section" name="Return Functions">&nbsp;</section>

##  Return Functions

Using the `console.log()` function is useful for debugging, but we don't always want to print out a value, instead we want to compute or format some data within a function to use later.

We noticed when learning about scope that we could create a variable within a function, but could not access the value of it outside of the scope of that function. So how could we get the value from _inside_ the scope of one function to _outside_ of it?

We can use what is called a **return value** to achieve this.

    function createGreeting(greeting, name) {
        // Add a space between greeting and name.
        var formattedGreeting = greeting + " " + name + "!";
        return formattedGreeting;
    };

The **return** keyword in this function allows the function to then hand off the value of `formattedGreeting` to a variable that can recieve it.

<div class="alert alert-info" role="alert">It may be useful to think of this concept in terms of the function now containing the value of what it is returning, and therefore it must be stored in a variable to be used somewhere else.</div>

    function createGreeting(greeting, name) {
        // Add a space between greeting and name.
        var formattedGreeting = greeting + " " + name + "!";
        return formattedGreeting;
    };

    var greeting = createGreeting("Hello", "Tom");

    console.log(greeting);

This this code block we are declaring our function and then calling it. When we call it, we know the function is returning a value, therefore we must store that value somewhere. We create a variable `greeting` which gets assigned the returned value from the `createGreeting()` function and we later pass it to the `console.log()` function to be printed in the console.

<div class="alert alert-info" role="alert">We can return any type, even functions... but more about that later.</div>



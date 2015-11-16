<section class="module-section" name="Introducing Functions">&nbsp;</section>

##  Introducing Functions

_"A function is a named block of code that performs a distinct service."_

We have already looked at some simple operations using strings in our **Intro to JavaScript** module. We looked at formulating a greeting by adding two `string` values together to make a new `string` that says hello to a person.

Every time we wish to write code to do this, we must assign the variable `name` the string value of the person's name we wish to say hello to, add that to the `String` "Hello ", and finally output this in an alert box.

    var name = "Tom";
    var greeting = "Hello " + name;
    alert(greeting);

There are two problems here! The first being that we have to write this code every time we want to perform this operation. The second being that we cannot change `name` unless we re-define the variable name with a new `string`.

We can't waste our time re-writing this code every time... we are too busy for this.

Also, what if we want to change the greeting to say "Good day" instead of "Hello"? We would need to find all instances of the code and update the second line.

We can easily write a greeting function to simplify this work!

To define a function, we must write the **keyword** `function`. Next, we need a name for our function followed by open and closed brackets `function functionName()`. Finally, we follow the function declaration with `{};`, where the `{};` will contain the code we wish to execute.

This may be a lot to take in, so let's look at our greeting example.

    function greeting() {
        // Code that executes when function is called.
    };

We can print our greeting to the console we used before by writing `console.log("Some greeting")`. This function is useful for debugging our code in the browser. We will see more on this later.

    function greeting() {
        var name = "Tom";
        var greeting = "Hello " + name;
        console.log(greeting);
    };

We have placed the code we want to run into the "greeting" function. The _curly braces_ that surround the code in our function is referred to as our function **closure**.

We can make this code execute by typing the name portion of the function below it and pressing run.

    function greeting() {
        var name = "Tom";
        var greeting = "Hello " + name;
        console.log(greeting);
    };

    greeting();

We still haven't solved the name changing issue! We can solve this problem and make our code more reusable by _passing a value_ to the function with the name we wish to greet. Then, the name can easily be added to the greeting and logged in the console using `console.log()`.

We can explore this more in the next section.



<section class="module-section" name="Functions and Reusable Code">&nbsp;</section>

##  Functions and Reusable Code

In the last section, we mentioned we could make our code more reusable by making it so that we can pass a "name" into the greeting function. How do we do that?

We pass values to a function by declaring the function with **formal parameters**. A formal parameter is a value that can optionally be passed into the function. When we pass a value into a function, the value is called an **argument**.

The argument we pass in becomes a variable we can use within the `{};` portion of the function. We can say this variable now exists in the **scope** of the function. Let's implement passing a value into a function before we dive into the topic of scope.

    function greeting(name) {
        var greeting = "Hello " + name;
        console.log(greeting);
    };

    greeting("Tom");

What should we take away from this? The function `greeting(name)` can take an argument in which it will create a variable called `name`. The `name` variable is assigned the value which we pass into the function ("Tom").

_So what is scope?_

When we declare some variable in our code, we give all of our code access to that variable.

For example:

    var greet = "Hello "

    function greeting(name) {
        var greeting = greet + name;
        console.log(greeting);
    };

    greeting("Tom");
    console.log(greet);

The function has access to the variable `greet` because everything in this **scope** does. We can say "The variable greet has _scope_ of this file."

If we declare a variable inside of a function, we should assume the scope of this variable is restricted to the contents of the `{}` block.

_However, in JavaScript this principle is slightly different and will be outlined in advanced topics. For now, just follow the information presented above._

    function greeting(name) {
        var greet = "Hello ";
        var greeting = greet + name;
        console.log(greeting);
    };

    greeting("Tom");
    console.log(greet);

When running this code, we will see an error telling us greet is not defined! This is because we defined it in the function `greeting(name)` and therefore `greet` has scope of our function and can not be referenced outside of the function.



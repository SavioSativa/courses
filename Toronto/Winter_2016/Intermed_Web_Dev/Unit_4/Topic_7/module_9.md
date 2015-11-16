<section class="module-section" name="Variables, Constants, &amp; Keywords">&nbsp;</section>

## Variables, Constants, & Keywords

### Variables & Assignment Operators

Often in mathematics, we don't like to work with numbers. Instead, what we do is assign a step we are at to a "variable" to be used later in another more complicated operation. ex. `x = 10` where `x` contains the value of `10`.

In JavaScript (and many other programming languages), we do the same thing! We call the `x` a **variable**, which we declare as `var x`. To put a **value** into the variable, we use **assignment**:

ex. 1

    var x = 10;

We see that in order to create the variable to contain the integer value `10`, we must use the "keyword" `var`. To assign a value to a variable, we use the **=**.

We can store _all data types_ in variables.

ex. 2 (Strings)

    var name = "Shawn";

ex. 3 (Booleans)

    var success = true;

ex. 3 (Operations)

    var answer = 2 + 2;
    -> answer: 4

    var greeting = "Hello " + name;
    -> answer: "Hello Shawn"

Notice we end everything with a semicolon `;`. It is best practice in JavaScript to end every statement with a semicolon. The actual line `var answer = 2 + 2;` is called an **Expression**. An expression is any combination of different values, constants, variables, etc. used to compute and produce another value.

What if we don't assign anything to a variable we create?

ex.

    var name;

In order to explain the contents of the variable "name", we need to add one more type to our earlier defined list of JavaScript types.

### Undefined

**Undefined** is a JavaScript value given to a variable that has yet to be assigned a value.

ex. answer

    var name;
    -> name: undefined

### Constants

In many languages, we can assign values to special variables called **constants**. These variables _cannot be changed once assigned a value_. However, in JavaScript nothing is constant! 

In order to keep JavaScript developers happy, the community decided to set a standard to define a "constant", even though constants are really variables!

A constant is written as a normal variable, because it is a normal variable. However, when a variable is written in ALL CAPITAL LETTERS, it is a signal to the developer that this variable is a constant and should not be changed.

ex. 1

    var PI = 3.142;

We can define a constant early on and use it later.

ex. 2

    var PI = 3.142;

    var radius = 2;
    var circleArea = PI*radius*radius;
    -> circle: 12.568

### Keywords (reserved words)

We mentioned **keywords** quickly above when using the keyword "var". Keywords are simply words *reserved* by JavaScript that cannot be used by developers to name variables (or functions, which we will get to later). 

We can see a list of more [keywords](http://www.w3schools.com/js/js_reserved.asp) here, and we will see more of them as we continue learning about JavaScript.


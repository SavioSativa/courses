<section class="module-section" name="Comments">&nbsp;</section>

## Comments

When a developer takes on a large project, they are often working with a huge code base and with other developers. It is important to understand code when you come back to it or when other developers need to use it. One way we can achieve this is through **comments**.

There are many ways of commenting your code. It is often best to find what works for you and your team. Generally, there are two basic types of comments. **Single line comments** start with `//` followed by the description of the portion of code you would like to document. You MUST start every line of the comment with a new `//`. Next, **multi-line comments** can be used for longer descriptions. All text must be encapsulated within `/*` and `*/`.

ex. Circle Area Commented

    /*
     This program calculates the area of a circle with 
     a radius of 2 units.
    */

    var PI = 3.142; // Constant.

    var radius = 2; // Radius of the circle.

    // Calculation of circle area
    // (Using PI constant):
    var circleArea = PI*radius*radius; 

    -> circle: 12.568



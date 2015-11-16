<section class="module-section" name="Switch Statements">&nbsp;</section>

## Switch

**If Else** statements are great when we need to evaluate a complex expression and then execute some code based on the result. Switch statements are better when there are no ranges for the conditions.

### Syntax

    switch(expression) {
        case 0:
            // Code block
            break;
        // Any number of cases...
        case n:
            // Code block
            break;
        default:
            // Default code block
    }

We pass in some expression that will match one of the "n" cases we have. Otherwise, it will result in our default answer. The expression can be of any type!

We can look at a simple example.

    function giveMeThePrice(item) {
    	switch (item) {
    	  case "Oranges":
    	    console.log("Oranges are $0.59 a pound.");
    	    break;
    	  case "Apples":
    	    console.log("Apples are $0.32 a pound.");
    	    break;
    	  case "Bananas":
    	    console.log("Bananas are $0.48 a pound.");
    	    break;
    	  case "Cherries":
    	    console.log("Cherries are $3.00 a pound.");
    	    break;
    	  case "Mangoes":
    	  case "Papayas":
    	    console.log("Mangoes and papayas are $2.79 a pound.");
    	    break;
    	  default:
    	    console.log("Sorry, we are out of " + item + ".");
    	}

    	console.log("Is there any other price you'd like to know?");
    };

In this case we give our `switch` expression a string. If the string matches a `case` we have, it will tell us the price. Otherwise, the function will tell us that item is sold out.

### If / else vs. Switch

It is good to know when to use `If Else` and when to use `Switch` statements.

Use the if statement when:

*   There are values that must be evaluated as a boolean operation.
*   There are a large number of values that can be easily separated into ranges.

Use the switch statement when:

*   There is a pattern of picking an option based on a variable's value.
*   There are no ranges for conditions because the values are nonlinear.



<section class="module-section" name="If / Else">&nbsp;</section>

## If / Else

We often in every day situations need to make decisions based on whether something is true. We can use **if statements** for this.

### Syntax

    if (condition) {
    	// Code to run if condition is met.
    }

For example, you might say, "If I am hungry, I will have something to eat". We could write this in code as:

    if (hungry) {
    	eatFood();
    }

Often we'll need to express the idea that if a condition is met, do something, and if not, we should do something else. Javascript can do that!

### Syntax

    if (condition) {
    	// Code to run if condition is met.
    }
    else {
    	// Fall back code.
    }

For example, you might say, "If I am hungry, I will have something to eat, otherwise, I will write code". We could write this in JavaScript as:

    if (hungry) {
    	eatFood();
    }
    else {
    	writeCode();
    }

The condition can be any combination of values that JavaScript will evaluate to a boolean. We use concepts like this in all kinds of operations to help our code be "smarter" than the average code.

Let's look at a simple example.

    function shouldWePartyTonight(dayOfTheWeek) {
    	if (dayOfTheWeek == "Monday" || dayOfTheWeek == "Tuesday" || dayOfTheWeek == "Wednesday" || dayOfTheWeek == "Thursday" || dayOfTheWeek == "Saturday" || dayOfTheWeek == "Sunday") {
    		console.log("NO WAY! You should be coding...");
    	}
    	else {
    		console.log("Yeah... I guess if you need a break.");
    	}

    };

Now you never have to think about whether or not you can go out tonight with your friends! Run this code and pass in a `string` as the day of the week and find out!

Small issue: if we don't enter a string value that matches a day of the week, it will always tell us "Yeah... I guess if you need a break.", which is not what we would want.

_Additionally, what if we need more than two options? Do we just write `if` every time?_

We can use `else if` to cover our other cases.

    function shouldWePartyTonight(dayOfTheWeek) {
    	if (dayOfTheWeek == "Monday" || dayOfTheWeek == "Tuesday" || dayOfTheWeek == "Wednesday") {
    		console.log("NO WAY! You should be coding...");
    	}
    	else if (dayOfTheWeek == "Thursday") {
    		console.log("Depends! Is there a special on wings today?")
    	}
    	else if (dayOfTheWeek == "Friday") {
    		console.log("Yeah... I guess if you need a break.");
    	}
    	else if (dayOfTheWeek == "Saturday" || dayOfTheWeek == "Sunday") {
    		console.log("I don't know, seems like a good day to read about JavaScript.");
    	}
    	else {
    		console.log("That is not a valid day of the week... have you already been partying?");
    	}

    };

Now we have some of the tools to write some pretty smart code!



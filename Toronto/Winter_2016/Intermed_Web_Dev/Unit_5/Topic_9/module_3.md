<!-- Importing Angular into each module until changes to portal have been made -->
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.0/angular.js"></script>


<section class="module-section" name="What is Angular?">&nbsp;</section>

## What is Angular?

Angular is an framework for building dynamic web applications. It gives us the capability to expand the limits of HTML and create highly-responsive single-page applications with expressive, readable code.

#### Why Angular?

HTML was not designed for dynamic websites. It's great for declaring static documents, but was never intended to be used in the way users expect web apps to work today.

Many frameworks and libraries have been written to solve this problem. jQuery, for example, allows developers to manipulate the DOM directly, but really only makes JavaScript easier to use - it abstracts away code to simplify common tasks. With libraries like jQuery, you still have to tell the browser, explicitly, what you want it to do.

#### Imperative vs. Declarative

One of Angular's core principles is that user interface programming should be accomplished using **declarative** programming - we should be able to tell the browser _what_ we want to happen, and it should figure out _how_ to do it. Contrast this with **imperative** programming, where we know _what_ we want to accomplish, but have to tell the browser _how_ to do it.

Let's look at a simple comparison between jQuery and Angular. We want to populate a list with an Array of names.

With jQuery:

    <ul id="friendList">
    </ul>

    <script>
    	$(document).ready(function() {
    		var friends = ['Mike', 'John', 'Jeremy', 'Mongbok'];

    		for (var i = 0; i < friends.length; i++) {
    			$('#friendList').append("<li>" + friends[i] + "</li>")
    		}
    	});
    </script>


Here we're **imperatively** telling jQuery exactly what to do: loop through our friend list; for each of our friends, create a new `li` element and append it to the end of the `#friendList` element.

Now, let's see how we'd accomplish the same thing in Angular:
    
    <ul ng-app="myApp" ng-controller="myCtrl as ctrl">
    	<li ng-repeat="friend in ctrl.friendList">{{ friend }}</li>
    </ul>

    <script>
    	angular.module('myApp').controller('myCtrl', function() {
    		this.friendList = ['Mike', 'John', 'Jeremy', 'Mongbok'];
    	});
    </script>


In this Angular code, we don't give explicit instructions on how to build our list - we're just telling Angular that we'd like this element to repeat, and it figures out the rest.

We're also declaring our intention directly in our HTML code. In the jQuery example, if you only looked at the HTML, you'd have no idea that jQuery was going to be performing an action on the `#friendList` element. In our Angular example, we've weaved our intentions directly into our HTML. Angular lets us _extend_ our HTML, making it more expressive and letting us define the dynamic elements right in the markup.



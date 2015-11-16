<section class="module-section" name="Controllers">&nbsp;</section>

## Controllers

Controllers in Angular are used to set up the initial state of our `$scope` object. The first thing we need to do is tell our **View** to use our controller. We'll do this by using the `ng-controller` directive.

    <body ng-app="myApp" ng-controller="MyController as ctrl">

Now everything in our `body` tag will fall under the scope of our controller. When Angular encounters this directive, it will assign the "MyController" controller to the body tag.

Note the code in our `ng-controller` directive: we're telling Angular to use the MyController controller, and assigning it an alias we've arbitrarily named "ctrl". You'll usually want to give your controller alias a more meaningful name.

In _app.js_, we've already defined our module, so let's start defining our controller. In Angular, controllers are just JavaScript constructor functions:

    // app.js
    var myApp = angular.module("myApp", []);

    function MyController() {
        this.greeting = "Well, hello ";
    }

We've defined our controller function and given it a property named "greeting". Now, we'll tell Angular to use this function as our Controller:

    // app.js
    var myApp = angular.module("myApp", []);

    function MyController() {
        this.greeting = "Well, hello!";
    }

    myApp.controller("MyController", MyController);


Now that our view has a controller associated with it, we're able to bind data from the model (the data defined in our controller) to our HTML.  Let's change our View to show the greeting we defined in our controller:

    <body ng-app="myApp" ng-controller="MyController as ctrl">
        <h1> {{ ctrl.greeting }} </h1>
    </body>


Great! We can also add functions to our controller using the prototyping method you've used in previous modules:

    // app.js
    var myApp = angular.module("myApp", []);

    function MyController() {
        this.greeting = "Well, hello!";
    }

    myApp.controller("MyController", MyController);

    MyController.prototype.changeGreeting = function() {
        this.greeting = "Top of the morning to you!";
    };


A function isn't much good to us, however, if we can't use it! Let's add a button to our page that will call our function when it's clicked.

    <body ng-app="myApp" ng-controller="MyController as ctrl">
        <h1> {{ ctrl.greeting }} </h1>
        <button ng-click="ctrl.changeGreeting()">Do it!</button>
    </body>

Voila! The `ng-click` directive will, as you may have guessed, perform an action when its element is clicked.

<div class="alert alert-info">
We've used a number of Angular <strong>directives</strong> but haven't really discussed what they are - don't worry! We'll be covering directives in-depth in the next module.
</div>

We've now configured a basic controller for our application. Next, we'll look over a different approach to controller configuration and look deeper into Angular `$scope` objects.




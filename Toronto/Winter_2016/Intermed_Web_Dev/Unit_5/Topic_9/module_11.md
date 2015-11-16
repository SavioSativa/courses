<section class="module-section" name="Multiple Controllers">&nbsp;</section>

## Multiple Controllers

As we've seen, an Angular controller is associated with, and controls, a specific HTML view. As we'll see, you can have multiple controllers on a page controlling different views, and controllers can be nested within other controllers.

Let's take a look at a simple example of two controllers on the same page, both using the `controller as` syntax:

    <body ng-app="myApp">
        <div ng-controller="CtrlOne as ctrlOne">
            {{ ctrlOne.greeting }}
        </div>

        <div ng-controller="CtrlTwo as ctrlTwo">
            {{ ctrlTwo.greeting }}
        </div>
    </body>

Nothing too complicated here. Each controller has it's own alias, and we're displaying the `greeting` property of each controller, using the alias we defined in our `ng-controller` directives. In our app.js, we'll define both of our controllers:

    // app.js
    var myApp = angular.module("myApp", []);

    function CtrlOne() {
        this.greeting = 'Hello from CtrlOne!';
    }

    function CtrlTwo() {
        this.greeting = 'Hello from CtrlTwo!';
    }

    myApp.controller('CtrlOne', CtrlOne);
    myApp.controller('CtrlTwo', CtrlTwo);


We've defined two separate controllers, each with their own properties, and we can access these in our views in an explicit way.

#### `$scope` inheritance and Nested Controllers

Controllers can also be nested inside one another:

    <body ng-app="myApp">
        <div ng-controller="CtrlOne as ctrlOne">
            {{ ctrlOne.greeting }}

            <div ng-controller="CtrlTwo as ctrlTwo">
                {{ ctrlTwo.greeting }}
            </div>
        </div>  
    </body>


Using the `controller as` syntax, it's clear what controller we're referencing when we display our `greeting` property. But what if we used the `$scope` method? Let's take a look:

    <body ng-app="myApp">
        <div ng-controller="CtrlOne">
            {{ greeting }}

            <div ng-controller="CtrlTwo">
                {{ greeting }}
            </div>
        </div>  
    </body>

This markup will do the same thing as our `controller as` syntax did, but it's much less clear what we're trying to accomplish when we look at the code. Is `{{ greeting }}` in our nested controller meant to print the greeting from `CtrlOne` or `CtrlTwo`?

This problem is better explained in the context of `$scope` inheritance.

#### `$scope` inheritance

When a controller is nested inside of another (using `$scope` syntax, instead of `controller as`), each **child** controller has access to the properties of its **parents**. We say that the child controller **inherits** properties from its' parents.

<div class="alert alert-info">
    Controller One (Parent)
    <ul>
        <li>parentGreeting = 'Hello from Parent!';</li>
        <li>parentProperty = 'Parent Property';</li>
    </ul>
    <div class="alert alert-warning">
        Controller Two (Child)
        <!-- <div class="alert alert-success">
        Controller Three
        </div> -->
        <ul>
            <li>childGreeting = 'Hello from Child!';</li>
            <li>childProperty = 'Child Property';</li>
        </ul>
    </div>
</div>



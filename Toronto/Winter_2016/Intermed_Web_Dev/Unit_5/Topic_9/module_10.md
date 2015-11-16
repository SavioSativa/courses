<section class="module-section" name="<code>$scope</code>">&nbsp;</section>

## Angular `$scope`

In the previous section, we configured our controller using what's known as the `controller as` syntax. We built our controller as we would build any other JavaScript object, using `this` to assign properties to the object and `prototype` to assign functions.

This is a relatively new approach to controller configuration, only recently introduced to Angular. It allows us to approach controllers as we would any other JavaScript object, and let's us explicitly bind properties and functions. However, the more commonly used approach (that you'll probably see a lot of across the plethora of Angular documentation) is somewhat different. Before we dive in, let's take a moment to talk about `$scope`.

#### What is it?

`$scope` is an object associated with every Angular controller - every controller has its own `$scope`. It is a JavaScript object that holds all the properties and functions that belong to a controller. Let's compare the two declarations for assigning a controller to a view and displaying a property defined within that controller:

    // 'controller as' syntax
    <body ng-app="myApp" ng-controller="MyController as ctrl">
    {{ ctrl.greeting }}

    // 'controller' syntax
    <body ng-app="myApp" ng-controller="MyController">
    {{ greeting }}

Using the second approach, Angular will invoke our controller function, but will now pass in the `$scope` object as an argument. Now, instead of declaring properties and functions with `this` and `prototype`, we'll attach them to the `$scope` object.

    // app.js
    var myApp = angular.module("myApp", []);

    function MyController($scope) {
        $scope.greeting = "Well, hello!";

        $scope.changeGreeting = function() {
            $scope.greeting = "Top of the morning to you!";
        };
    }

    myApp.controller("MyController", MyController);

As you can see, we're setting our properties and functions on the `$scope` object. When we want to use these in our view, we're not required to prefix them with the controller alias as we did using the `controller as` syntax:

    <body ng-app="myApp" ng-controller="MyController">
        {{ greeting }}
        <button ng-click="changeGreeting()">
    </body>

We'll explore the advantages of the `controller as` method in the next section when we deal with multiple controllers and scope inheritance. You can read more about scopes at <a href="https://docs.angularjs.org/guide/scope" target="_blank">AngularJS Developer Guide: Scopes</a>



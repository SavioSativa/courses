<!-- Importing Angular into each module until changes to portal have been made -->
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.0/angular.js"></script>




<section class="module-section" name="Modules">&nbsp;</section>

## Modules

Modules can be thought of as containers for different parts of an application. They are responsible for loading dependencies (things our app needs to function like additional files and code) and for "bootstrapping" (automatically initializing) an Angular app.

In a new file called _app.js_, we'll define our module. (Don't forget to include this file in your `head` tag after/below the `script` tag pointing to your AngularJS file!) The syntax for defining a module is as follows:

    var myApp = angular.module("myApp", []);


We use the Angular `module` function to construct our module. This function takes two arguments:

1.  A string referring to the app name we defined in the `ng-app` directive
2.  An array of module dependencies (Empty in our example, as our module has no dependencies)

Also take note of the fact that we're storing our module in a variable. We'll later use this variable to reference the module when we add directives, services, and various other awesomeness.



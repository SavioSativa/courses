<!-- Importing Angular into each module until changes to portal have been made -->
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.0/angular.js"></script>







<section class="module-section" name="Setting Up Angular">&nbsp;</section>

## Setting up Angular

It's relatively simple to get started with Angular. The first thing we need to do is download AngularJS from <a href="https://angularjs.org" target="_blank">https://angularjs.org/</a> and include the AngularJS code in the `head` tag on our page:

    <head>
    	<script src="js/angular.js"></script>
    </head>


<div class="alert alert-info">
Ensure that the file name you download matches the file name you reference in your HTML document. If you download <code>angular.min.js</code> and include it in your <em>js</em> directory, it should be referenced using <code class="html">&lt;script src="js/angular.min.js"&gt;&lt;/script&gt;</code>
</div>

Alternatively, we can include AngularJS using Google's CDN, much like we did with Bootstrap:

    <head>
    	<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.3.16/angular.min.js"></script>
    </head>


Now that the Angular framework is loaded and ready to go, we can begin writing our Angular code.

The first thing we'll do is use the `ng-app` directive to tell Angular where our app begins (**Directives** are a core component of Angular apps - more on those later)

    <body ng-app="myApp">


This small piece of code tells Angular that our `body` tag is the root element of our Angular application, and as such, all of the HTML within the `body` tag will be evaluated by Angular. We've also given our application a name `myApp` that we'll reference when we construct an Angular **module**.



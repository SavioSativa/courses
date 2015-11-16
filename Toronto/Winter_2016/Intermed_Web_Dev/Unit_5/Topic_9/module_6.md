<!-- Importing Angular into each module until changes to portal have been made -->
<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.4.0/angular.js"></script>



<section class="module-section" name="Data Binding">&nbsp;</section>

## Data Binding

One of Angular's defining features is **two-way data binding**. This is essentially a two-way street between the view (what the user sees and interacts with on the client-side) and the model (where the data is stored on the server-side) that keeps data consistent between the two. When the view or model is changed, the other changes as well. You can read more about data binding as it applies to Angular <a href="https://docs.angularjs.org/guide/databinding" target="_blank">here</a>.

Let's take a look at a working example:

    <body ng-app>
    	<input ng-model="name">
    	{{ name }}
    <body>


Let's quickly review this code:

*   We've added `ng-app` to our body tag to identify it as an Angular app
*   We bound a model called "name" to a text box using the `ng-model` directive
*   We're displaying the value of our model using double curly braces that tell Angular to evaluate the expression between the braces

You can see the live code below. Try typing in the textbox, and you'll see how Angular's data binding updates the model in real time.

<pre ng-app>
<input type="text" ng-model="name"><br/>
{{name}}
</pre>


For a more detailed look at data binding, you can check out this Angular quiz app <a href="http://plnkr.co/edit/iyLcFueqEefkkDxEdzuR?p=preview" target="_blank">here</a>.


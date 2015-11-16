##The jQuery Selector Engine

Prior to jQuery, there were only three ways to target elements: by tag, by class, and by id. These functions were written as follows:

```javascript
var tag = document.getElementsByTagName('p');
var id = document.getElementById('container');
var class = document.getElementsByClassName('alert');
```

The `document` object is available in every browser and contains the information for all elements, their contents, styles, and attributes. It also contains additional methods for altering these properties. The value stored in each variable represents an object of that element (or array of element objects) that provides access to its properties.

jQuery broadened the power of DOM manipulation by allowing for a universal targeting syntax that used CSS selector rules for targeting elements. It looked like so:

```javascript
var tag = $('p');
var id = $('#container');
var class = $('.alert');
```

The values stored in the variables are also objects representing that element and its properties. You can view also this information with `console.log`.

In this module we will look at four ways to interact with the DOM;

* Altering element content
* Changing styles
* Adding and removing elements
* Binding events

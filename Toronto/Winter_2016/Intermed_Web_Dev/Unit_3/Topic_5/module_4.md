##Changing Element Styles

Using jQuery for style augmenting is like having a dynamic style sheet that is responsive to specific events. There are three ways to alter an element's style.

**The CSS method**  
This method allows you to directly override your style sheet by applying an inline style to your element.

```javascript
//you can alter one property at a time
$('h1').css('color','red');

//or chain them 
$('h1').css({'color':'red','font-size':'10px'});
```

**Adding Classes**  
You can also use the `addClass()` method to add classes to an element. This is useful for hover events or when an element in a list becomes the selected element (or element in focus). You can alter the element's appearance by adding an entire class from your style sheet.


```javascript
/* you can alter one property at a time */
$('input[name="email"]').addClass('inValid');
```

**Removing Classes**  
You can also do the exact opposite with the `removeClass()` method.

```javascript
/* you can alter one property at a time */
$('input[name="email"]').removeClass('inValid');
```

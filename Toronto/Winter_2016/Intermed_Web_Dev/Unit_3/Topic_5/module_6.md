##Binding Events

Binding events is a very common part of interacting with elements in the DOM. To do so, you would select the behaviour you want bind to the element. For example, for a button you may want to bind a click event that is triggered every time you click the button.

```javascript
$('#myButton').click(function(){
  alert('You clicked the button');
});
```

There are many different event types you can bind and you find this information on the [jQuery API website](http://api.jquery.com). You can bind events for mouse events that include clicking, hovering, scrolling etc. You can also bind events for keyboard interactions such as pressing a keydown, holding a key, pressing a specific key etc. The most important understanding is that this event is forever bound to that element.

You remove a binding from an element with the following JavaScript code.

```
$('#myButton').unbind('click');
```

The parameter in the unbind function would be the name of the event you originally bound to the element.

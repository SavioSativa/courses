##Adding and Removing Elements

The `html()` method is only useful for interacting with an element's inner content. Using this method you must alter all of the content at once, this can be inconvenient if you only need to make minor changes to the inner content. This is where the following set of methods become useful.

**Appending Elements**  
This is a very useful method for adding content to a list dynamically.

```javascript
$('.mylist').append('<li>John Doe : 123.456.7890</li>');
```

**Prepending Elements**  
Prepending works similarly to appending except that this method adds your content starting right after the opening tag.

```markup
<pre>
<code>
&lt;div id="login"&gt;
  &lt;form&gt;
    &lt;input type="email" name="email"&gt;
    &lt;input type="password" name="password"&gt;
  &lt;/form&gt;
&lt;/div&gt;
</code>
</pre>
```

```javascript
$('#login').prepend('<p>Incorrect User Name</p>');
```

**Removing Elements**  
Removing elements requires the jQuery `remove()` method. The method deletes the HTML element completely from the DOM. It is written like so:

```javascript
$('#login').remove();
```

##Altering Element Content

Altering the content of an element can mean a few things. For one, it could be just changing the text inside an `<h1>` tag. It could also mean adding or replacing HTML within a tag. Both these objectives can be fulfilled with the `.html()` method.

**Altering Content**

```javascript
$('h1').html('Goodbye, World');
$('#err-msg').html('<p>Your Credit Card has been declined </p>');
```

**Gathering Content**  
You can also use the same method to grab the inner content of HTML, you only need to leave the method parameter empty.

```javascript
var h1 = $('h1').html();
console.log(h1);
var err = $('#err-msg').html();
console.log(err);
```

Many jQuery methods have this duplicitous use.
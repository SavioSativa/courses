<section class="module-section" name="Adding plugins">&nbsp;</section>

## Adding plugins

Some plugins can be complex to add as they may include `.js`, `.html`, and `.css` files.

[Backstretch](http://srobbin.com/jquery-plugins/backstretch/) is a very simple plugin that allows you to add an image as a dynamically sized background image for any element.

We will add this plugin to our code.

Simply grab the code from [GitHub](https://raw.githubusercontent.com/srobbin/jquery-backstretch/master/jquery.backstretch.min.js), save it in a file called backstretch.js, and add it as resource to your page with the following script tag _after_ your `jquery.min.js` script:

		<script type="text/javascript" src="js/backstretch.js"></script>

With the plugin installed, you can use it to add a background slide show to your body with the following statement:

		$.backstretch([
		      "http://dl.dropbox.com/u/515046/www/outside.jpg", 
		      "http://dl.dropbox.com/u/515046/www/garfield-interior.jpg", 
		      "http://dl.dropbox.com/u/515046/www/cheers.jpg"
		], {duration: 3000, fade: 750}); 
	


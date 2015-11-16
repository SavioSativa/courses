<section class="module-section" name="Adding a plugin from GitHub">&nbsp;</section>

## Adding a plugin from GitHub

Many developers store their plugins on Github. This is useful for allowing open source collaboration on the plugin so that other developers can contribute and improve the plugin should they like. The original author would then have the power to accept or reject the suggested changes.

The next plugin will add a very unique way to display alert messages to a user:

![example of a git repository on GitHub](http://174.129.248.23/brainstation/images/gitrepo.png)

At first, this page can look intimidating if you are new to GitHub. If you read through the documentation, you will see that you only need to add a JavaScript file and a CSS file. You can either clone the repository to your computer or you can just navigate the repository to find the files the are discussing. You will see the first file in the main directory, `jquery.avgrund.js` and the second is in the style folder `avgrund.css`.

If you have followed the process just like in the previous slide, you can read the documentation to see how you can use this plugin to alter cookie data.

		$('element').avgrund();
		
		// or with options
		$('element').avgrund({
		  width: 380, // max is 640px
		  height: 280, // max is 350px
		  showClose: false, 
		  showCloseText: '', 
		  closeByEscape: true, 
		  closeByDocument: true, 
		  holderClass: '', 
		  overlayClass: '', 
		  enableStackAnimation: false,
		  onBlurContainer: '', 
		  openOnEvent: true, 
		  setEvent: 'click', 
		  onLoad: function (elem) { ... }, 
		  onUnload: function (elem) { ... }, 
		  template: 'Your content goes here..'
		});
		

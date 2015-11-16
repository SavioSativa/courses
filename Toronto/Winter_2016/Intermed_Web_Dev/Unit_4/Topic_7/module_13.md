<section class="module-section" name="Installing JavaScript in Sublime">&nbsp;</section>

## Installing JavaScript in Sublime

Follow these simple steps to install a JavaScript interpreter in Sublime text so you can run your code using Command + B (⌘ + B).

*   Install Node.js from [here](http://nodejs.org/dist/v0.12.4/node-v0.12.4.pkg)
*   Open Terminal.app and type `node`. If you see a prompt (`>`), it is installed!
*   Open Sublime Text
*   Navigate to *Tools > Build System > New Build System...*
*   Delete the content that appears. Paste the following code:

        {
        	"cmd": ["/usr/local/bin/node", "$file"],
        	"selector": "*.js"
        }

*   When saving this, rename it to `JavaScript.sublime-build`
*   Close all Sublime windows and then reopen Sublime 
*   Create a file with the following code and save it as `test.js`:

		var x = 1;
		console.log(x);
		console.log(x + 1);

* Use the hotkey (⌘ + B) or (Ctrl + B) to run a console window. You should see a window below your code that displays:

		1
		2
		[Finished in 0.1s]

*   If you do not see that, go to *Tools > Build System* and look for a checkmark beside JavaScript.


<section class="module-section" name="Conditionals">&nbsp;</section>

## Conditionals

Conditionals are **expressions** that evaluate to `true` or `false`.

We combine values, variables, and boolean operators in the form of an expression and evaluate the resulting value.

    var loginSuccessful = true;
    var fileDownloadSuccessful = true;
    console.log(loginSuccesful && fileDownloadSuccessful);

    -> true

Using this simple concept, we have the power to make "smart" code!

In the above example, we can dictate if we should continue with a specific operation based on the success of the user logging in to their account (`loginSuccessful`) and the success of the user downloading the necessary files (`fileDownloadSuccessful`) to continue. If either is false, then the expression `loginSuccesful && fileDownloadSuccessful` will evaluate to `false`.



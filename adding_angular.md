# Adding Angular
Before we start, create a new file called portfolio.controller.js in the directory containing the boilerplate/template code.

Now that you have that, let's make sure out html can find it.  To do so, add the following to index.html:
`<script src="portfolio.controller.js"></script>`
This is usually included within the head tags in the html.  

Yay!  So now our html can find our Javascript file.  Let's go back to portfolio.controller.js and actually add some code.  
Add the following:
`var portfolioApp = angular.module('portfolioApp',[]);`

Now go back to index.html…
Add the following: 
`<html ng-app='portfolioApp’>`

Now we're going to do some experimenting...
Go back to Chrome or whatever internet browser of your choosing and reload the page.  Open up the inspector console to show the following error:
"Uncaught ReferenceError: angular is not defined"

The reason we are getting this error message is because we have some Angular specific code in our html (ng-app) but we don't have Angular itself in the directory...That's awkward.  We told our HTML and Javascript to find something without telling it the location...In order to fix this, go back to index.html…
Add the following:
`<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.25/angular.min.js"></script>`

Now to double check that the following told our html a valid location to find Angular, let's go back to Chrome (or whatever internet browser of your liking), reload the page, and then open up inspector to the console section to see that error message is gone.  Yay!  You just fixed your first error dealing with Angular! :)

Now let's go onto actually making our controller file (portfolio.controller.js) an actual controller...
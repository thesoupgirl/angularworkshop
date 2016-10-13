# Controller Fundamentals

Okay now let's make our controller file, portfolio.controller.js, an actual controller!  Inside that file, add the following to the end of it:  
```
portfolioApp.controller("Portfolio",["$scope", function($scope) {
    //controller code goes here

}]);
```

This creates a controller hung off of our Angular module, portfolioApp.  You can have more than controller or in our case, we'll only have one, but Angular is very flexible with how many controllers you can have.

Now that we have made our controller file a controller that Angular will recognize, let's make sure our html can find it as well.
Go to index.html.
Replace the body tag or `<body>` with
`<body ng-controller="Portfolio”>`
This allows us to use functions and variables within our portfolio.controller.js within our body tags in the html.

Yay!  Now let's start on making our navigation work...
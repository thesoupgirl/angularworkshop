# Adding Angular

First:

-Download repo
-open in Finder
-navigate to repo in command line
-start local server by entering:  python -m SimpleHTTPServer 8000

and then going to chrome and entering in: localhost:8000

tah dah!

create new file called
portfolio.controller.js

add the following to index.html:
`<script src="portfolio.controller.js"></script>`

Now go back to portfolio.controller.js…
add the following:
`var portfolioApp = angular.module('portfolioApp',[]);`

Go back to index.html…
add the following: 
`<html ng-app='portfolioApp’>`

go back to chrome, reload the page.  Open up the inspector console to show:
"Uncaught ReferenceError: angular is not defined"

Go back to index.html…
add the following:
`<script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.25/angular.min.js"></script>`

go back to chrome, reload the page, open up inspector to see that error message is gone

go to portfolio.controller.js…
add:  
`portfolioApp.controller("Portfolio",["$scope", function($scope) {


}]);`

go to index.html…
replace body tag with…
`<body ng-controller="Portfolio”>`

go to portfolio.controller.js…
add: 
`$scope.name = "Lisa";
$scope.universityMajor = "Purdue Computer Science";
$scope.passion = "Student and Web Developer”;`

go to index.html…
add:
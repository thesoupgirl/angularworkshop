# Tab Navigation

There are many ways to do tab navigation, especially with Angular, but I personally think the easiest is by using ```ng-show```.

About ```ng-show```:  It takes a function or boolean and if it is true, then it'll show whatever is in the tags of whatever the ng-show attribute is hung off of.  If it's false, it won't be shown to the user.

In order to be able to use ng-show, we're going to need to create a variable for each tab in our application.  To start off, let's just do 2.  One for the Home page and one for the About Me page.  In the controller (portfolio.controller.js) add a variable hung off of scope ($scope) for Home and one for About Me.  The home one should be true and the about me one should be set to false.  In the end, your portfolio.controller.js should look something like this:

```
var portfolioApp = angular.module('portfolioApp',[]);

portfolioApp.controller("Portfolio",["$scope", function($scope) {
    $scope.isHome = true;
	$scope.isAboutMe = false;
    
}]);
```
# Tab Navigation

There are many ways to do tab navigation, especially with Angular, but I personally think the easiest is by using ```ng-show```.

About ```ng-show```:  It takes a function or boolean and if it is true, then it'll show whatever is in the tags of whatever the ng-show attribute is hung off of.  If it's false, it won't be shown to the user.

In order to be able to use ng-show, we're going to need to create a variable for each tab in our application.  To start off, let's just do 2.  One for the Home page and one for the About Me page.  In the controller (portfolio.controller.js) add a variable hung off of scope ($scope) for Home and one for About Me.  The home one should be true and the about me one should be set to false.  In the end, your portfolio.controller.js should look something like this:

```javascript
var portfolioApp = angular.module('portfolioApp',[]);

portfolioApp.controller("Portfolio",["$scope", function($scope) {
    $scope.isHome = true;
	$scope.isAboutMe = false;
    
}]);
```

Great!  Now we have two booleans for two of our tabs in the application.  Now let's actually use the ng-show attribute.  In your index.html file, we will need to add the ng-show attribute to a tag (could be a div tag, body tag, etc.) that contains all of the home page and none of the other pages/tabs.  However, we want the navigation bar to show up in all of our pages, so we will need to be very careful to not add the ng-show attribute to a tag that contains our navigation bar.  To find out which tag we should add ng-show to, let's go back to our browser and open up the inspector once more.
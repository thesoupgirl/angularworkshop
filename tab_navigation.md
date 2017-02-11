# Tab Navigation

There are many ways to do tab navigation, especially with Angular, but I personally think the easiest is by using `ng-show`.

About `ng-show`:  It takes a function or boolean and if it is true, then it'll show whatever is in the tags of whatever the ng-show attribute is hung off of.  If it's false, it won't be shown to the user.

In order to be able to use ng-show, we're going to need to create a variable for each tab in our application.  To start off, let's just do 2.  One for the Home page and one for the About Me page.  In the controller \(portfolio.controller.js\) add a variable hung off of scope \($scope\) for Home and one for About Me.  The home one should be true and the about me one should be set to false.  In the end, your portfolio.controller.js should look something like this:

```javascript
var portfolioApp = angular.module('portfolioApp',[]);

portfolioApp.controller("Portfolio",["$scope", function($scope) {
    $scope.isHome = true;
    $scope.isAboutMe = false;

}]);
```

Great!  Now we have two booleans for two of our tabs in the application.  Now let's actually use the ng-show attribute.  In your index.html file, we will need to add the ng-show attribute to a tag \(could be a div tag, body tag, etc.\) that contains all of the home page and none of the other pages/tabs.  However, we want the navigation bar to show up in all of our pages, so we will need to be very careful to not add the ng-show attribute to a tag that contains our navigation bar.  To find out which tag we should add ng-show to, let's go back to our browser and open up the inspector once more.

You'll see that in the inspector, there's a nav tag.  Inside the nav tag, you should see the following:

```
<!-- main nav -->
    <nav class="collapse navbar-collapse navbar-right" role="navigation">
        <ul id="nav" class="nav navbar-nav">
            <li class="current"><a href="#body">Home</a></li>
```

The\_ li \_tag that contains home is the one that belongs to the home page.  This is the one where we are going to start making the magic happen.  However, before we can do anything, we want to make sure angular only changes tabs whenever the user clicks the tab.  In order to make this work, we need to go back to our controller file, which is portfolio.controller.js

Inside our controller, below the variables we added earlier such as $scope.isAboutMe, we are going to create a function called clickedHome.

```
$scope.clickedHome = function() {
    //clicked home function code here
}
```

Whenever someone clicks home, we want to make the booleans for all the other tabs false.  To do this, we add code to clickedHome:

```
$scope.clickedHome = function() {
    $scope.isAboutMe = false; //we don't want to show about me page
    $scope.isHome = true; //this is what we want to show
}
```

While we're at it, let's make another function for whether they clicked the About Me tab.  Let's call this one clickedAbout me.  It'll look like this:

```
$scope.clickedAboutMe = function() {
    //clicked about me function code here
}
```

Whenever someone clicks About Me, we want to make the booleans for all the other tabs false.  To do this, we add code to clickedAboutMe:

```
$scope.clickedAboutMe = function() {
    $scope.isAboutMe = true; //we want to show this
    $scope.isHome = false; //we don't want to show this after the user clicks about me tab
}
```

Now to let our HTML know about these fabulous new functions...Let's go back to our index.html where our nav is.  We're going to modify the line that contains our home navigation tab.

```
<li class="current"><a href="#body" ng-click="clickedHome()"> Home </a></li>
```

Now we've just added the angular attribute tag, ng-click.  Ng-click will only call the function clickedHome\(\) in our controller if the home navigation tab is clicked.

Let's do that for the other tab, About Me.

```
<li><a href="#aboutme" ng-click="clickedAboutMe()">About Me</a></li>
```

Even after you do all this, you might notice that nothing will happen.  That's because we haven't added our ng-show attribute tags anywhere!

As far as our ng-show attribute tags go, it's very important where we put them.  We want to put it around all the html code that we want to show if they clicked our home page.  I'm going to add a div right after the header closing tag.

```
</header>
<!-- End Fixed Navigation -->

<!-- Home Slider -->
<div ng-show="isHome">
<section id="slider">
```

Since I added a new div tag, I now need to close it.  I'm going to add a closing div tag after the closing section tag.

```
    </section>
</div>
```

Now we have the newly created div showing only if the user clicked home.


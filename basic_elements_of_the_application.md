# Basic Elements of The Application

As far as AngularJS goes, it is a front-end, or UI framework for Javascript.  Basically this means that while it makes your webapp look fantastic, you will need some sort of backend to actually be able to deploy the app.  For this tutorial, we will be using Node.js.  

*Disclaimer:  This tutorial will not go over Node.js, since it is only being used for deployment purposes and nothing else.  Everything important is on the front-end.*

Okay now to make our webapp actually appear, we need our index.html file.  At the very top of it, you'll see 
```<!-- index.html -->
    <!DOCTYPE html>
    <html>```
    
If you're seeing that, then you're in the right file!  Congrats! :) Now let's get to the importance of our index.html file...

<!-- load bootstrap and fontawesome via CDN -->
      <link rel="stylesheet" href="//netdna.bootstrapcdn.com/bootstrap/3.0.0/css/bootstrap.min.css" />
      <link rel="stylesheet" href="//netdna.bootstrapcdn.com/font-awesome/4.0.0/css/font-awesome.css" />

      <!-- CSS
    ================================================== -->
    <!-- Fontawesome Icon font -->
        <link rel="stylesheet" href="css/font-awesome.min.css">
    <!-- Twitter Bootstrap css -->
        <link rel="stylesheet" href="css/bootstrap.min.css">
    <!-- jquery.fancybox  -->
        <link rel="stylesheet" href="css/jquery.fancybox.css">
    <!-- animate -->
        <link rel="stylesheet" href="css/animate.css">
    <!-- Main Stylesheet -->
        <link rel="stylesheet" href="css/main.css">
    <!-- media-queries -->
        <link rel="stylesheet" href="css/media-queries.css">


      <!-- load angular and angular route via CDN -->
      <script src="http://code.jquery.com/jquery-latest.min.js" type="text/javascript"></script>
      <script src="jquery.singlePageNav.min.js"></script>
      <script src="jquery.mixitup.min.js"></script>
      <script src="jquery.fancybox.pack.js"></script>
      <script src="jquery.parallax-1.1.3.js"></script>
      <script src="jquery.appear.js"></script>
      <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.2.25/angular.min.js"></script>
      <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.2.25/angular-route.js"></script>
      <script src="portfolio.controller.js"></script>
    </head>
    
 
# Imports
Above are all the files needed to make our wonderful webapp look how it is.  The first series of links give us Bootstrap styling without actually having to ever download it!  Nifty, huh?


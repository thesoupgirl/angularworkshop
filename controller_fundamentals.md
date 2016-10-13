# Controller Fundamentals

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
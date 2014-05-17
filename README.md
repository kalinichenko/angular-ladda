# angular-ladda

AngularJS directive for Ladda

## Get Started

(1) Get angular-ladda via [Bower](http://bower.io/)

```sh
$ bower install angular-ladda
```
or add bower.json
```sh
$ bower install angular-ladda --save
```

(2) add css & javascript link to html

```html
...
<link rel="stylesheet" href="bower_components/ladda/dist/ladda-themeless.min.css">
...
<script src="bower_components/ladda/js/spin.js"></script>
<script src="bower_components/ladda/js/ladda.js"></script>
<script src="bower_components/angular-ladda/dist/angular-ladda.js"></script>
...
```

(3) add `'angular-ladda'` to your main module's list of dependencies

```javascript
var myApp = angular.module('myApp', ['angular-ladda']);
```

(4) enjoy!

## Quick example

### controller

```javascript
  $scope.login = function() {
    // start loading
    $scope.loginLoading = true;
    loginService.login(function() {
      // stop loading
      $scope.loginLoading = false;
    });
  }
```

### view

```html
<button ladda="loginLoading" ng-click="login()">
  Login
</button>
```

## Links

* [ladda](http://lab.hakim.se/ladda/)

## Contributing

1. Fork it ( https://github.com/remotty/angular-ladda/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

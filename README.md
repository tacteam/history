### TAC Development Guide

# tac-history

This repo is for distribution on `bower`. The source for this module is in the
[main TacTeam repo](https://github.com/tacteam/history).
Please file issues and pull requests against that repo.

## Install

You can install this package with `bower`.

### bower

```shell
bower install tac-history
```

Optionally you can add --save prefix to add package to bower.js

```shell
bower install tac-history --save
```

Then add a `<script>` to your `index.html`:

```html
<script src="/bower_components/tac-history/dist/history.js"></script>
```

## Documentation

##### Initialize component

```js
angular.module('main-application')
.run([
  'tac.history', 
  function(history) {
    history.initialize();
  }
])
```

Additionally you can pass regular expressions as argument on the 'initialize' method to add skippable patterns


##### Using

```js
angular.module('main-application')
.controller('some.controller', [
  '$scope',
  'tac.history', 
  function($scope, history) {
    $scope.go_back_button = function(){
      history.go_back();
    };
  }
])
```


## License

License is not available yet
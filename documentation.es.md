### guia de desarrollo TAC

# tac-history

Este repositorio de distribuye a travez del administrador `bower`. Los fuentes de este módulo se pueden encontrar en el
[repositorio general TacTeam](https://github.com/tacteam/history).
Sientase a gusto de reportar problemas o proponer nuevas *features* en este repositorio

## Install

Este módulo puede ser intalado con `bower`.

### bower

```shell
bower install tac-history
```

Opcionalmente puede agregar el prefijo --save para agregar la dependencia al archivo bower.js

```shell
bower install tac-history --save
```

Luego agregue el correpondiente tag `<script>` a su `index.html`:

```html
<script src="/bower_components/tac-history/dist/history.js"></script>
```

## Documentación

##### Inicialización del componente

```js
angular.module('main-application')
.run([
  'tac.history', 
  function(history) {
    history.initialize();
  }
])
```

Adicionalmente se pueden pasar expresiones regulares como argumento del método 'initialize' para agregar patrones omitibles.

##### Uso

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


## Licensia

No disponible aún.
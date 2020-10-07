# Hello World
Keeping up with programming world tradition, here it is my "Hello World" at GitHub and a few "HelloWorld" code snippet from programming languages I worked with at some point of time.

## JavaScript
```JavaScript
(function(){
  'use strict';
  console.log('Hello World!');
})();
```

## PHP
```php
<html>
<head>
  <title>PHP</title>
</head>
<body>
  <?php echo '<p>Hello World!</p>'; ?> 
</body>
</html>
```

## Java
```java
public class HelloWorld {
    public static void main(String[] args) {
      System.out.println("Hello World!");
    }
}
```

## HTML
```html
<html>
<head>
    <title>Hello World Page</title>
</head>
<body>
<p>Hello World!</p>
</body>
</html>
```

## C++
```c++
#include 
int main(){
    std::cout << "Hello, World!";
    return 0;
}
```
## AngularJS 1.6

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <script src="https://unpkg.com/angular@1.6.3/angular.min.js"></script>
</head>
<body>
    <main-comp></main-comp>
    <script>
        (function(angular){
            'use script';
            angular
                .module('myApp', [])
                .component('mainComp', {
                    template: '<h1>Hello World!</h1>'
                });

            //bootstrap the application
            angular.bootstrap(document.body, ['myApp'], {strictDi:true});
        })(window.angular);
    </script>
</body>
</html>
```

## React 

With plain ES2015+ Syntax.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hello World</title>
  <script crossorigin src="https://unpkg.com/react@16/umd/react.development.js"></script>
  <script crossorigin src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
</head>

<body>
  <div id="root"></div>
  <script type="module">
    // Bootstrap React app with ReactDOM.render
    ReactDOM.render(
      React.createElement('h1', null, 'Hello World!'),
      document.getElementById('root')
    );
  </script>
</body>

</html>
```
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
```
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
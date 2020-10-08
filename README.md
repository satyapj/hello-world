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

## Angular 

With plaing ES2015+ Syntax. This is just to show how internals of Angular works. For real-world projects it's better to stick to Angular CLI and TypeScript.

```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hello World</title>

  <!-- Load Angular depdendency as UMD modules from unpkg.com -->
  <script src="https://unpkg.com/rxjs@6.2.0/bundles/rxjs.umd.js"></script>
  <script src="https://unpkg.com/@angular/core@10.1.4/bundles/core.umd.js"></script>
  <script src="https://unpkg.com/@angular/common@10.1.4/bundles/common.umd.js"></script>
  <script src="https://unpkg.com/@angular/compiler@10.1.4/bundles/compiler.umd.js"></script>
  <script src="https://unpkg.com/@angular/platform-browser@10.1.4/bundles/platform-browser.umd.js"></script>
  <script
    src="https://unpkg.com/@angular/platform-browser-dynamic@10.1.4/bundles/platform-browser-dynamic.umd.js"></script>
  <script src="https://unpkg.com/zone.js@0.11.1/bundles/zone.umd.js"></script>
</head>

<body>
  <app-root></app-root>

  <script>
    /**
     * 
     * This is just to show how internals of Angular works. For real-world projects it's better to stick to Angular CLI and TypeScript.
     *
     * A note about @Component and other Classs decorators: Internally, Angular calls ng.core.ɵsetClassMetadata that
     * either adds a static variable 'decorators' to the Class if it doesn't exists (it shall be there in case Class is extended) 
     * and pushes metadata objects to static variable 'decorators'.
     */

    // AppComponent: Root component for the application.
    class AppComponent {
      constructor() {
        this.title = 'Hello World!';
      }
    }

    // Add decorators metadata to the AppComponent
    AppComponent.decorators = [{
      type: ng.core.Component,
      args: [{
        selector: 'app-root',
        template: `<h1>{{title}}</h1>`,
        styles: ['']
      }]
    }];

    // AppModule: Root Module for the Application
    class AppModule { }

    // Rgister AppModule as Angular Module
    AppModule.ɵmod = ng.core.ɵɵdefineNgModule({
      type: AppModule,
      bootstrap: [AppComponent]
    });

    // provide class metadata, typically done via Class decorator in TypeScript.
    ng.core.ɵsetClassMetadata(AppModule, [{
      type: ng.core.NgModule,
      args: [{
        declarations: [
          AppComponent
        ],
        imports: [
          ng.platformBrowser.BrowserModule
        ],
        providers: [],
        bootstrap: [AppComponent]
      }]
    }], null, null);

    // Bootstrap root moule
    ng.platformBrowserDynamic.platformBrowserDynamic()
      .bootstrapModule(AppModule)
      .catch(err => console.error(err));
  </script>
</body>

</html>
```

## [Vue.js](https://vuejs.org/)

A JavaScript framework for building user interface.

- [Example-01](vue-01.html)

## [Node.js](https://nodejs.org/)

Node.js is a JavaScript runtime, that means pretty much any JavaScript file can be a Node.js application. 

> To run this Node.js application make sure you have installed latest version from their [download](https://nodejs.org/en/download/) page.

A bare baone example:

```js
// app.js
console.log(`Hello World!`);
```

Save the code in app.js and then run it from command line as `node app.js`.

- [Another Example](node-app-01.js): A basic http server

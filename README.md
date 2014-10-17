# Angular Codemirror Dictionary Hint

This directive allows you to add hint support for your Codemirror instance based on a custom dictionary.

## Requirements
- [Angular UI Codemirror](https://github.com/angular-ui/ui-codemirror)

## Usage

Load the script files into your application. Note that you need to load the 
[CodeMirror hint addon](http://codemirror.net/doc/manual.html#addons) as well.

```html
<link rel="stylesheet" type="text/css" href="bower_components/codemirror/lib/codemirror.css">
<link type="text/css" rel="stylesheet" href="bower_components/codemirror/addon/hint/show-hint.css" />
<script type="text/javascript" src="bower_components/codemirror/lib/codemirror.js"></script>
<script src="bower_components/codemirror/addon/hint/show-hint.js"></script>
<script type="text/javascript" src="bower_components/angular/angular.js"></script>
<script type="text/javascript" src="bower_components/angular-ui-codemirror/ui-codemirror.js"></script>
<script type="text/javascript" src="ng-codemirror-dictionary-hint.js"></script>
```

Add this module as a dependency to your AngularJS app:

    angular.module('MyApp', [ 'ui.codemirror', 'ng.codemirror.dictionary.hint' ]);

Finally, add the directive to your HTML as an attribute.

- You can bind a scope variable (whose value must be an array) and optionally change it over time.

```html
<div ui-codemirror ng-codemirror-dictionary-hint="tags"></div>
```

- You can bind an static array inline as well.

```html
<div ui-codemirror ng-codemirror-dictionary-hint="[ 'Soccer', 'Cricket', 'Baseball', 'Kho Kho' ]"></div>
```
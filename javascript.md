javascript.js


## Multiple ways to concat a file
1. The addition operator ( + )
```javascript
    var text = 'Hello' + ' world';
    alert(text);
``` 

2. The assignment operator ( += )
```javascript
    var text = 'Hello';
    text +=  + ' world'
    alert(text);
```

3. The array join( array.join('') )
```javascript
    var text = [];
    text.push('hello');
    text.push(' world');
    alert(text.join('');
```
or
```javascript
    var text = ['hello', ' ', 'world'];
    alert(text.join('');
```

4. The built-in concat method
```javascript
    var text = '';
    text.concat('Hellow',' ','world');
```

## How to include a non-javascript file using require.js (handlebars template in this case)
This requires the text plugin for require.js [Text Plugin](http://requirejs.org/docs/api.html#text)
```javascript
define([
    'jquery',
    'underscore',
    'backbone',
    'app',
    'text!app/templates/header_template.hb'
], function ($, _, Backbone, App, headerTemplate ) {
    // Do something
});
```

## Videos
[https://www.youtube.com/watch?v=i_qE1iAmjFg&feature=player_detailpage](10 Things I Learned from the jQuery Source - Paul Irish)

## Frameworks
* Backbone.js

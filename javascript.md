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



## How to get a clean array from one that has duplicate values
```javascript
uniqueArrayItems: function( originalArray ) {
    var newArray = [],
        originalArrayLength = originalArray.length,
        found,
        x, y;

    for ( x = 0; x < originalArray; x++ ) {
        found = false;
        for ( y = 0; y < newArray.length; y++ ) {
            if ( originalArray[x] === newArray[y] ) {
              found = true;
              break;
            }
        }

        if ( !found ) {
            newArray.push( originalArray[x] );
        }
    }

    return newArray;
}
```


## Compare two arrays together to see if they match
```javascript
compareArrays: function( array1, array2) {
    var i = array1.length;

    if (i != array2.length) {
        return false;
    }

    while ( i-- ) {
        if ( array1[i] !== array2[i]) {
            return false;
        }
    }

    return true;
}
```

## How to stop the browser debugger at a specific location in your code
```javascript
debugger;
```

## The best way to create a for loop
```
var increment;
var itemLength = items.length;

for ( increment = 0, ; increment < itemLength; increment += 1 ) {  
    // do some stuff here  
}
```

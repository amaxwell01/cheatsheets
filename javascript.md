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

## Videos
[https://www.youtube.com/watch?v=i_qE1iAmjFg&feature=player_detailpage](10 Things I Learned from the jQuery Source - Paul Irish)

## Frameworks
* Backbone.js

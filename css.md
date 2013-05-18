## CSS Shim's / Shiv's
- [CSS3 Pie](http://css3pie.com/documentation/product-comparison)

## CSS Transitions
```
transition-duration: .5s;
transition-property: background, color;
transition-timing-function: ease-in;
-moz-transition-duration: .5s;
-moz-transition-property: background, color;
-moz-transition-timing-function: ease-in;
-ms-transition-duration: .5s;
-ms-transition-property: background, color;
-ms-transition-timing-function: ease-in;
-webkit-transition-duration: .5s;
-webkit-transition-property: background, color;
-webkit-transition-timing-function: ease-in;
```


## Clear Floats:
```css
// SASS CODE
.clearfix {
    *zoom: 1;
    &:before,
    &:after {
        content: "";
        display: table;
        line-height: 0;
    }
    &:after {
        clear: both;
    }
}
 
// CSS ONLY CODE BELOW
.clearfix {
    *zoom: 1;
}
.clearfix:before,
.clearfix:after
{
    content: "";
    display: table;
    line-height: 0;
}
.clearfix:after {
    clear: both;
}
```

## CSS Hacks
```
// Opacity
-ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=50)";

/***** Selector Hacks ******/

/* IE6 and below */
* html #uno  { color: red }
 
/* IE7 */
*:first-child+html #dos { color: red } 
 
/* IE7, FF, Saf, Opera  */
html>body #tres { color: red }
 
/* IE8, FF, Saf, Opera (Everything but IE 6,7) */
html>/**/body #cuatro { color: red }
 
/* Safari 2 - 3.1 */
html[xmlns*=""]:root #trece  { color: red  }
 
/* Safari 2 - 3.1, Opera 9.25 */
*|html[xmlns*=""] #catorce { color: red  }
 
/* Everything but IE6-8 */
:root *> #quince { color: red  }
 
/* IE7 */
*+html #dieciocho {  color: red }


/* IE6 */
#once { _color: blue }
 
/* IE6, IE7 */
#doce { *color: blue; /* or #color: blue */ }
 
/* Everything but IE6 */
#diecisiete { color/**/: blue }
 
/* IE6, IE7, IE8 */
#diecinueve { color: blue\9; }
 
/* IE7, IE8 */
#veinte { color/*\**/: blue\9; }
 
/* IE6, IE7 -- acts as an !important */
#veintesiete { color: blue !ie; } /* string after !
``

## How to target just mailto: links
```css
a[href^="mailto"] {
    text-decoration: underline !important;
}
```

## Important Tools / Ideas
* [http://inuitcss.com](Inuit CSS)
* [http://twitter.github.com/bootstrap](Twitter Bootstrap)
* [http://html5please.com](HTML5 Please, Browser feature support)
* [http://caniuse.com](Can I use, Browser feature support)
* 960 Grids


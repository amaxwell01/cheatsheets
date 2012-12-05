## Set the character set to UTF-8
```
<meta charset="utf-8" />
```

## Set the website viewport to work on mobile
```
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

##iPhone viewport
```
<meta name="viewport" content="width=320; initial-scale=1.0; maximum-scale=1.0; user-scalable=0;"/>
```

## IE conditionals for CSS
```
<!--[if lt IE 7 ]> <html class="ie6"> <![endif]-->
<!--[if IE 7 ]>    <html class="ie7"> <![endif]-->
<!--[if IE 8 ]>    <html class="ie8"> <![endif]-->
<!--[if IE 9 ]>    <html class="ie9"> <![endif]-->
<!--[if (gt IE 9)|!(IE)]><!--> <html class=""> <!--<![endif]-->
```

## IE Conditionals for code
```
<!--[if IE]>      I'm IE      <![endif]-->
<!--[if !IE]> --> Not IE <!-- <![endif]-->
```

#Chrome Frame
```
<!--[if lt IE 8]>
<div class="upgrade-banner">
  You are using an <strong>outdated</strong> browser.  Please <a 
  href="http://browsehappy.com/">
  upgrade your browser</a> or <a 
  href="http://www.google.com/chromeframe/?redirect=true">activate Google 
  Chrome Frame</a> to improve your experience.
</div>
<![endif]-->
```

* CSS3中的渐变  
Gradient分别为linear-gradient和radial-gradient.  
浏览器内核:  
Mozilla(Firefox, Flock)  
Webkit(Safari, Chrome)  
Opera(Opera)  
Trident(IE)  
语法：  
```
// Mozilla:
-moz-linear-gradient([<point> || <angle>, ] ? <stop>, <stop>[, <stop>]*)
// Webkit:  
-webkit-linear-gradient([<point> || <angle>, ] ? <stop>, <stop>[, <stop>]*)  //新
-webkit-linear(<type>, <point>[, <radius>] ? , <point>[, <radius>] ? [, <stop>]*)  //旧  
// Opera:
-o-linear-gradient([<point> || <angle>, ] ? <stop>, <stop>[, <stop>]*)  
// Trident:  
filter:progid:DxImageTransform.Microsoft.gradient(GradientType=0, startColorStr=#1471da, endColor=#1c85fb)  //IE9  
-ms-filter:progid:DxImageTransform.Microsoft.gradient(GradientType=0, startColorStr=#1471da, endColor=#1c85fb)  //IE8+*
```  
           
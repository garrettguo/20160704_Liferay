* $("p").live("click", data, function(){...});  
绑定一个或多个事件，可以绑定由代码生成的元素。
***
* $("p").unbind("click").on("click",function(){...});  
解除绑定后绑定单击事件。
***
* p:nth-child(n)  
```
<div>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
    <p></p>
</div>
```
(1) p:nth-child(3) means you have choose the third `<p>` element in parent element `<div>`.  
(2) p:nth-child(3n+1) the parameter n will increase start with 0.  
***
* function `prop()` in jQuery.  
(1) .prop(propertyName)  
This function means getting the property of the first element in matched list.  
(2) .prop(propertyName, value), .prop(map)  
Setting one or more attributes to the matched elements in list.  
(3) differences between `attr()` and `prop()`  
```
if ( elem.checked ) 
if ( $(elem).prop("checked") ) 
if ( $(elem).is(":checked") ) 
```
These three sentences will return value which type is boolean.  
```
        .attr()                Proper.prop() usage
   $(window).attr...          $(window).prop...
   $(document).attr..         $(document).prop...
```
If window or document use .attr() in jQuery1.6, it will doesn't work, because window and document can't have attributes. In jQuery1.6.1, when window or document use .attr(), it will change to .prop() automatically.  
![](../images/201311151723484.png)  
***
* `disabled` attribute in jQuery.  
The function of `disabled` is to avoid using a certain element.  

**Conclusion**  
When we want to change the inherent quality of HTML element, we always use `attr()`.  
When we want to change the custom DOM attributes of HTML element, we always use `prop()`.  
*For example:*  
(1) example 1  
```
<a href="http://www.baidu.com" target="_self" class="btn">百度</a>
```
In this `<a>` tag, it has "href", "target" and "class" attributes. These attributes are the inherent attributes of `<a>` tag. So we will use `prop()`.  
```
<a href="#" id="link1" action="delete">删除</a>
```
In this `<a>` tag. Inherent attributes are "href" and "id". Custom attribute is "action". So we use `attr()` for attribute "action".  
(2) example 2  
```
<input id="chk1" type="checkbox" />是否可见
<input id="chk2" type="checkbox" checked="checked" />是否可见
```
Some elements in HTML like "checkbox" and "select" have their inherent attributes such as "checked" and "selected". So we always use `prop()`.  
```
$("#chk1").prop("checked") == false
$("#chk2").prop("checked") == true
``` 
If we use `attr()`.  
```
$("#chk1").attr("checked") == undefined
$("#chk2").attr("checked") == "checked"
```
***
* `disabled` attribute in jQuery.  
The function of `disabled` is to avoid using a certain element.  
***
* selector `>` in CSS  
It means the first generation child elements. 
***
* `<script>`的defer属性：  
```
<script type="text/javascript" defer="defer" src="..."></script>
```
告诉浏览器在整个页面都解析完毕后再执行脚本
注：  
(1) 只适用于外部脚本文件
***
* `<script>`的async属性：  
```
<script type="text/javascript" async src="example1.js"></script>
<script type="text/javascript" async src="example2.js"></script>
```
不让页面等待两个脚本下载和执行，从而异步加载页面其他内容。
注：  
(1) 一定会再页面load前执行
(2) 只适用于外部脚本文件
(3) 异步脚本不要再加载期间修改DOM
***
* XHTML中的`<script>`  
```
<script type="text/javascript">
    function compare(a, b) {
        if (a < b) {
            ...
        }
    }
</script>
```
"<"在XHTML中被当作一个新标签的开始来解析，而作为一个标签来讲，小于号后面不能有空格，所以会导致语法错误。
解决办法：  
(1) `if (a &lt; b)`  
(2)  
```
<script type="text/javascript"><![CDATA[
    function compare(a, b) {
        if (a < b) {
            ...
        }
    }
]]></script>
```
***
* 文档模式：  
混杂模式和标准模式  
***
* `<noscript>`标签  
触发条件：  
(1) 浏览器不支持脚本  
(2) 脚本被禁用  
能够包含`<body>`中的任何HTML元素  
```
<html>
    <head>
        ...
    </head>
    <body>
        <noscript>
            <p>...</p>
        </noscript>
    </body>
</html>
```

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
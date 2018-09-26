 appendChild()和 insertBefore()



//取得文档标题 var originalTitle = document.title; 

//设置文档标题 document.title = "New page title"; 



//取得完整的 URL var url = document.URL; 

//取得域名	var domain = document.domain; 

//取得来源页面的 URL var referrer = document.referrer; 



## 改变 HTML 输出流

在 JavaScript 中，document.write() 可用于直接向 HTML 输出流写内容。

提示：绝不要使用在文档加载之后使用 document.write()。这会覆盖该文档。

## 改变 HTML 内容

修改 HTML 内容的最简单的方法时使用 innerHTML 属性。

如需改变 HTML 元素的内容，请使用这个语法：

```
document.getElementById(id).innerHTML=new HTML
```

## 改变 HTML 属性

如需改变 HTML 元素的属性，请使用这个语法：

```
document.getElementById(id).attribute=new value
```





## HTML 事件

```
<script>
document.getElementById("myBtn").onclick=function(){displayDate()};
</script>
```

onclick 

## onload 和 onunload 事件

onload 和 onunload 事件会在用户进入或离开页面时被触发。

onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。

onload 和 onunload 事件可用于处理 cookie。



## onchange 事件

onchange 事件常结合对输入字段的验证来使用。

## onmouseover 和 onmouseout 事件

onmouseover 和 onmouseout 事件可用于在用户的鼠标移至 HTML 元素上方或移出元素时触发函数。



# input 识别回车键

```
window.document.onkeypress = ``function``(e){
    ``// 获取事件
    ``e = e || window.event; 
    ``// 获取按键编码
    ``var` `key = e.whick || e.keyCode; 
    ``// 检测是否为回车键
    ``if``(key == 13){
        ``alert(``'按下回车键'``);
    ``}
}
```

# 通用的按键监听方式

    document.addEventListener("keydown",OMG,true)
      function OMG(e){
        // 获取事件
        e = e || window.event; 
        // 获取按键编码
        var key = e.whick || e.keyCode; 
        // 检测是否为ESC键
        if(key == 27){
            alert('按下ESC键');
        }
      }
# HTML DOM 事件

http://www.runoob.com/jsref/dom-obj-event.html





**cssText 本质是什么？**

cssText 的本质就是设置 HTML 元素的 style 属性值。

 ***感觉像一个全局变量***

**cssText 怎么用？**

```
document.getElementById("d1").style.cssText = "color:red; font-size:13px;";
```
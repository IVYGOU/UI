## DOM(Document Object Model)
解析器的输出“解析树”是由 DOM 元素和属性节点构成的树结构。     

它是 HTML 文档的对象表示，同时是外部内容（例如 JavaScript）与 HTML 元素之间的接口。    

解析树的根节点是“Document”对象。

DOM 与标记之间几乎是一一对应的关系。比如：   

```html
<html>
  <body>
    <p>
      Hello World
    </p>
    <div> <img src="example.png"/></div>
  </body>
</html>
```
翻译成如下的DOM树：   

 ![DOM树](http://www.html5rocks.com/zh/tutorials/internals/howbrowserswork/image015.png)      
 
* “D”(document)   
 
* “O”(object)   
 
javascript中有三种对象：    

1.用户定义对象(user-defined object)  

2.内建对象(naive object)   

内建于JS中的对象，如Array，Math和Date等   

3.宿主对象(host object)    

由浏览器提供的对象（BOM），最基础的对象是window，它表示浏览器的一个实例。

window：既是通过Javascript访问浏览器的一个接口，又是ECMAScript规定的Global对象。

window对象对应着浏览器本身，它的属性和方法统称为BOM(浏览器对象模型)

* “M”(Model)   

```html
<!DOCTYPE html>
<html lang="en">

  <head>
    <meta charset="utf-8">
    <title>Shopping list</title>
  </head>
  <h1> what to buy  </h1>
  <p title ="a gentle reminder"> Don't forget!</p>
  <ul id ="purchases"> 
  <li> beans</li>
  </ul>
  <body>
  </body>

</html>

```

## 节点
元素节点   

文本节点   

属性节点


## DOM操作  

DOM就是浏览器为JavaScript提供的一系列接口（通过window.documnet提供的），通过这些接口我们可以操作web页面。

注意：但DOM并不是编程语言，它是文档对象的模型，该模型是独立于编程语言的。也可以在Pyhton中操作。

可以在任意元素上应用class属性和id属性，用于区分
* 获取元素节点     

getElementById(id) 通过元素ID    
`document.getElementById("purchases");`   

getElementsByTagName(tag) 通过标签名字   
`document.getElementsByTagName("li");`     

getElementsByClassName() 通过类名字   
`document.getElementsByClassName("sale")`     


* 获取和设置属性    


object.getAttribute(attribute) 查询节点属性   

```javascript
var paras = document.getElementsByTagName("p")
for (var i = 0; i < paras.length; i++) {
  alert(paras[i].getAttribute("title"));
}
```  

object.setAttribute(attribute,value)  修改节点属性    
```javascript
var shopping = document.getElementById("purchases");
shopping.getAttribute("title", "a list of goods");
```



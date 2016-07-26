## html标签

* 标题   

HTML 标题（Heading）是通过` <h1> - <h6>` 等标签进行定义的。

```html
<h1>This is a heading</h1>
<h2>This is a heading</h2>
<h3>This is a heading</h3>
```
* 段落   

HTML 段落是通过 <p> 标签进行定义的。
```html
<p>This is a paragraph.</p>
<p>This is another paragraph.</p>
```
* 链接     

HTML 链接是通过 <a> 标签进行定义的。
```html
<a href="http://www.w3school.com.cn">This is a link</a>
```
* 图像   

HTML 图像是通过 <img> 标签进行定义的。。
```html
<img src="w3school.jpg" width="104" height="142" />
```
* 无序列表     

<ul> 标签定义无序列表。  

 ```html
<ul>
   <li>Coffee</li>
   <li>Tea</li>
</ul>
```

* 有序列表     

<ol> 标签定义无序列表。  

 ```html
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```  

* 列表项目   

`<li>` 标签定义列表项目。   

`<li>` 标签可用在有序列表 (<ol>) 和无序列表 (<ul>) 中。  

```html
<ol>
   <li>Coffee</li>
   <li>Tea</li>
   <li>Milk</li>
</ol>

<ul>
   <li>Coffee</li>
   <li>Tea</li>
   <li>Milk</li>
</ul>
```

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8"/>
    <title>Shopping list</title>
  </head>
  <h1> what to buy  </h1>
  <p title ="a gentle reminder"> Don't forget!</p>
  <ul id ="purchases"> 
  <li> beans</li>
  <li class="sale"> Milk</li>
  <li class="sale important"> Cheese</li>
  </ul>
  <body>
  </body>

</html>
```

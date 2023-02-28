# API作用和分类

作用：使用JS去操作html和浏览器

分类：DOM（文档对象模型）、BOM（浏览器对象模型）

# 什么是DOM

### 定义

> DOM（Document Object Model）是用来呈现以及与任意HTML或XML文档交互的API

简单来说：DOM是浏览器提供的一套专门用来**<font color="#dd0g0g">操作页面内容</font>**的功能

### 作用

开发网页内容特效和实现用户交互

# DOM树

- 将 HTML 文档以树状结构直观的表现出来，我们称之为文档树或 DOM 树
- 描述网页内容关系的名词
- 作用：文档树直观的体现了**标签与标签**之间的关系

https://github-js-study-1316943030.cos.ap-beijing.myqcloud.com/DOMtree.jpg

# DOM对象

### 定义

浏览器根据html标签生成的 **<font color="#dd0g0g">JS对象</font>**

（在html中称为标签，把标签获取到js中称为对象）

- 所有的标签属性都可以在这个对象上面找到
- 修改这个对象的属性会自动映射到标签身上

### DMO核心思想

把网页内容当做**对象**来处理

### document对象

- 他是dom里面最大的对象

- 所以它提供的属性和方法都是**用来访问和操作网页内容的**

  - document.write()

- 网页所有内容都在document里面

  https://github-js-study-1316943030.cos.ap-beijing.myqcloud.com/DOMobject.png
根据css选择器获取DOM元素

# 根据匹配的第一个元素

### 语法

~~~javascript
document.querySelector('css选择器')
~~~

### 参数

包含一个或多个有效的css选择器**<font color="#dd0g0g">字符串</font>**

### 返回值

css选择器匹配的**第一个元素**，一个HTMLElement**对象**

### 可以对其直接操作修改：

~~~JavaScript
nav.style.color = 'red'
~~~

### 例子：

~~~JavaScript
<body>
    <div class="box"></div>
    <span id = "nav">导航栏</span>
    <ul>
        <li>测试</li>
        <li>测试</li>
        <li>测试</li>
    </ul>
    <script>
        const box =  document.querySelector('div')
        const box1 = document.querySelector('.box')

        const nav = document.querySelector('#nav')
        const span1 = document.querySelector('span')

        // 获取第一个li
        const li = document.querySelector('ul li:first-child')
    </script>
</body>
~~~



# 选择匹配的多个元素

### 语法：

### 参数：

包含一个或多个有效的CSS选择器**<font color="#dd0g0g">字符串</font>**

### 返回值：

css选择器匹配的**NodeList 对象集合**（以**伪数组**的形式进行展示，没有push（）和pop（）方法）

### 不能直接对其进行修改

只能通过遍历的方式（for）一次给里面的元素做修改

### 例子：

~~~ JavaScript
<body>   
    <ul>
        <li>测试1</li>
        <li>测试2</li>
        <li>测试3</li>
    </ul>

    <script>
        const lis = document.querySelectorAll('ul li')
    </script>

</body>
~~~

### 获取每一个li的对象

~~~ JavaScript
<body>   
    <ul class = "nav">
        <li>测试1</li>
        <li>测试2</li>
        <li>测试3</li>
    </ul>

    <script>
        const lis = document.querySelectorAll('.nav li')
        console.log(lis);
        for(let i = 0; i < lis.length; i ++){
            console.log(lis[i]);
        }
    </script>

</body>
~~~




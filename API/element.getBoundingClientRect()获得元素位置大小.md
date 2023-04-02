# 作用

返回元素的大小及其相对于视口（可视化的窗口）的位置

# 例子

https://github-js-study-1316943030.cos.ap-beijing.myqcloud.com/getBoundingClientRect%28%29.PNG

### 代码

~~~css
div {
            width: 200px;
            height: 200px;
            background-color: pink;
            margin: 100px;
        }

~~~

~~~ JavaScript
<script>
        const div = document.querySelector('div')
        console.log(div.getBoundingClientRect());
</script>
~~~

当页面进行滚动之后，div对于窗口的高度变为负数

https://github-js-study-1316943030.cos.ap-beijing.myqcloud.com/getBoundingClientRect%28%291.PNG
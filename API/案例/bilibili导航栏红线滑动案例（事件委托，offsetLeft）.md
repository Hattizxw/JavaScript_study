# 需求

实现点击bilibili导航栏，使得红线跟随鼠标点击的部分进行移动

https://github-js-study-1316943030.cos.ap-beijing.myqcloud.com/%E6%A1%88%E4%BE%8B/anli11.jpg

# 分析

- 用到事件委托，不需要给每一个a注册事件了，我们只需要给a的父级（list）注册一个事件
- 点击链接得到当前元素的offsetLeft值
- 修改line颜色块的transform值 = 点击链接的offsetLeft
- 添加过度效果

# 代码

### JavaScript

~~~JavaScript
<script>
        //获取父元素，添加事件委托
        const list = document.querySelector('.tabs-list')
        //给a注册事件
        list.addEventListener('click', function(e){
            //判断点击的是不是a
            if (e.target.tagName === 'A'){
                //让line进行移动
                line.style.transform = `translateX(${e.target.offsetLeft}px)`
            }
</script>
~~~


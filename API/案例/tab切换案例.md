# 需求

鼠标经过不同的选项卡，底部可以显示不同的内容

# 用到的知识点

- 获取DOM对象
- 添加类
- this环境变量的使用

# 代码

### css

~~~css
<style>
        * {
            margin: 0;
            padding: 0;
        }

        .tab{
            width: 590px;
            height: 340px;
            margin: 20px;
            border: 1px solid #e4e4e4;
        }

        .tab-nav {
            width: 100%;
            height: 60px;
            line-height: 60px;
            display: flex;
            justify-content: space-between;
        }

        .tab-nav h3 {
            font-size: 24px;
            font-weight: normal;
            margin-left: 20px;
        }

        .tab-nav ul {
            list-style: none;
            display: flex;
            justify-content: flex-end;
        }

        .tab-nav ul li {
            margin: 0 20px;
            font-size: 14px;
        }

        .tab-nav ul li a {
            text-decoration: none;
            border-bottom: 2px solid transparent;
            color: #333;
        }

        .tab-nav ul li a.active {
            border-color: #e1251b;
            color: #e1251b;
        }
        
        .tab-content {
            padding: 0 16px;
        }

        .tab-content .item {
            display: none;
        }

        .tab-content .item.active {
            display: block;
        }

    </style>
~~~

### JavaScript

~~~JavaScript
<div class="tab">
        <div class="tab-nav">
            <h3>每日特价</h3>
            <ul>
                <li><a class="active" href="javascript:;">精选</a></li>
                <li><a href="javascript:;">美食</a></li>
                <li><a href="javascript:;">百货</a></li>
                <li><a href="javascript:;">个护</a></li>
                <li><a href="javascript:;">预告</a></li>
            </ul>
        </div>
        <div class="tab-content">
            <div class="item active"><img src="./images/tab00.png" alt="" /></div>
            <div class="item"><img src="./images/tab01.png" alt="" /></div>
            <div class="item"><img src="./images/tab02.png" alt="" /></div>
            <div class="item"><img src="./images/tab03.png" alt="" /></div>
            <div class="item"><img src="./images/tab04.png" alt="" /></div>
        </div>
</div>

<script>
        //先获取每一个a标签
        const as = document.querySelectorAll('.tab-nav a')
        //给每一个a标签添加鼠标移动事件
        for(let i = 0; i < as.length; i++){
            as[i].addEventListener('mouseenter', function(){
                //删除所有的active类，再给指定的a添加上
                document.querySelector('.tab-nav .active').classList.remove('active')
                this.classList.add('active')

                //再更换tab对应的内容
                document.querySelector('.tab-content .active').classList.remove('active')
                //这个就不能用this了，因为tab对应的内容不是在as数组中的（不是as[i]对象），而是，其他的对象
                document.querySelector(`.tab-content .item:nth-child(${i + 1})`).classList.add('active')
            })
        }
</script>
~~~

# 效果图

https://github-js-study-1316943030.cos.ap-beijing.myqcloud.com/%E6%A1%88%E4%BE%8B/anli9.PNG
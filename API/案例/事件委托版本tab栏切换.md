# 用到的知识点

- 事件委托
- 自定义属性

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

### html

~~~html
<div class="tab">
        <div class="tab-nav">
            <h3>每日特价</h3>
            <ul>
                <li><a class="active" href="javascript:;" data-id="0">精选</a></li>
                <li><a href="javascript:;"  data-id="1">美食</a></li>
                <li><a href="javascript:;"  data-id="2">百货</a></li>
                <li><a href="javascript:;" data-id="3">个护</a></li>
                <li><a href="javascript:;" data-id="4">预告</a></li>
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
~~~

### JavaScript

~~~JavaScript
<script>
        const ul = document.querySelector('.tab-nav ul')
        ul.addEventListener('mouseover', function(e){
            if(e.target.tagName === 'A'){
                //先删除
                document.querySelector('.tab-nav .active').classList.remove('active')
                e.target.classList.add('active')

                //由于没有用遍历数组的方法遍历li，所以没有数组的索引号来获取iteam了，所以此时我们可以用到自定义属性，自己给他们添加一个索引号
                //注意，这里e.target.dataset.id获取到的是字符串类型需要强转
                const id = +e.target.dataset.id
                document.querySelector('.tab-content .active').classList.remove('active')
                document.querySelector(`.tab-content .item:nth-child(${id + 1})`).classList.add('active')
            }
            
        })
</script>
~~~


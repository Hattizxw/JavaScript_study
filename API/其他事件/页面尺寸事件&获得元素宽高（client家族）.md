# resize

会在窗口尺寸改变的时候触发事件：

~~~JavaScript
window.addEventListener('resize', function(){
            
    //执行的代码
        })
~~~

# 检测屏幕宽度

~~~JavaScript
window.addEventListener('resize', function(){
            let w = document.documentElement.clientWidth
            console.log(w);
        })
~~~

# 获取元素宽高

- **获取元素可见部分的宽高（不包含边框，margin，滚动条等）**

### 关键字

**clientWidth和clientHeight**

他们俩是属性

通过js的方法检测宽度和高度

~~~css
div {
            display: inline-block;
            height: 200px;
            background-color: pink;
            padding: 10px;
        }
~~~

~~~JavaScript
<div>123123123123123123132</div>
    
    <script>

        const div = document.querySelector('div')
        console.log(div.clientWidth);

	</script>
~~~


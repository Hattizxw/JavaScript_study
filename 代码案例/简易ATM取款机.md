 # 写出下图代码

https://github-js-study-1316943030.cos.ap-beijing.myqcloud.com/jscode2.png

~~~javascript
<body>
    <script>
        let money = 1000
        while(true){
            let choise = +prompt(`
            请你选择操作：
            1. 存钱
            2. 取钱
            3. 查看余额
            4. 退出
            `)
            // 如果用户输入的是4，则退出循环
            if(choise === 4){
                break
            }

            switch(choise){
                case 1:
                    let cun = +prompt(`输入存钱金额:`)
                    money = money + cun
                    break
                case 2:
                    let qu = +prompt(`输入取钱金额:`)
                    money = money - qu
                    break
                case 3:
                    alert(`您的银行卡余额是${money}`)
                    break
            }
        }
    </script>
</body>
~~~


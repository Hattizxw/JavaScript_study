JavaScript中的正数，负数，小数统一称为数字类型

**<font color="#dd0g0g">注意</font><br/>**

JavaScript是弱数据类型，变量到底属于哪种类型，只有赋值之后，我们才能确认

let num = ‘hatti’

# 算术运算符

**<font color="#dd0g0g">+,-,\*,/,%</font><br/>**

### 顺序优先级

优先级越高越先被执行，优先级相同，从左到右

- 乘，除，取余优先级相同

- 加减优先级相同

# NaN (not a number)

代表一个计算错误，他是一个不正确的或者一个未定义的数学操作所得到的结果

eg

console.log(‘老师’ + 2） //NaN

NaN是黏性的，任何对NaN的操作都会返回NaN

eg

console.log(NaN + 2） //NaN
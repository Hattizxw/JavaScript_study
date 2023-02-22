# 隐式转换

- 有字符串的加法“” + 1， 结果是“1”
- 减法（像大多数数学运算一样）只能用于数字，它会使空字符串转换成0
- null 经过数字转换后会变为0
- undefined经过数字转换之后变成NaN

```JavaScript
 console.log('' - 1);  //-1
 console.log('pink老师' - 1);  //NaN
 console.log(null + 1);  //1
 console.log(undefined + 1);  //NaN
 console.log(NaN + 1);  //NaN
```

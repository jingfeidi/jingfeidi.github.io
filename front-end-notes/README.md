# 程序员心态和理论

## 浏览器函数
   alert() 弹出警示框<br>
   prompt() 弹出提示框(输入框)，需要使用变量保存输入的值；值的类型是字符串型
**示例：**<br>
```
   练习：两次弹出提示框，使用变量保存后，计算两个数字相加的和，并将和使用警示框弹出
    //弹出两次提示框，保存到两个变量中
    var num1=prompt('input first number');
    var num2=prompt('input second number');
    console.log(num1+num2);//12 字符串拼接

    //把输入的值转为数值型
    num1=parseFloat(num1);
    num2=parseFloat(num2);
    console.log(num1+num2);//3 加法运算
    //使用警示框弹出和
    alert(num1+num2);
```




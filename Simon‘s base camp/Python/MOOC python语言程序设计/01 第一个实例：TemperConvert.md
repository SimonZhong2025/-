```
#TemperConver.py 注释信息

TemperStr = input("输入带有符号的温度值：") # 命名规则：大小写敏感、首字符不能是数字、不与保留字相同
if TemperStr[-1] in ['F','f']: # 使用保留字in判断一个元素是否在列表中
    C = (eval(TemperStr[0:-1]) - 32)/1.8
    print("转换后的温度值是{:.2f}C".format(C)) # {:.2f}   .format(C) 这个事字符串格式化方法，此刻先记下来即可：
elif TemperStr[-1] in ['C','c']:
    F = (eval(TemperStr[0:-1]))*1.8 + 32
    print("转换后的温度是{:.2f}F".format(F))
else:
    print("格式错误")
```

#### 举一反三的改变

标识放在温度数值前面

标识字符改变为多个字符：82Ce等等

货币转换、长度转换、重量转换、面积转换......

多行注释`'''`

##### 保留字

|and|elif|import|**raise**|global|
|:---:|:---:|:---:|:---:|:---:|
|as|else|in|return|**nonlocal**|
|**assert**|except|**is**|try|True|
|break|finally|lambda|while|False|
|**class**|for|not|**with**|None|
|def|if|pass|del||
|continue|from|or|**yield**||

> 加粗代表没有涉及到

### 分析代码
#### 数据类型

整数类型：10011101

字符串："10,011,101"

列表类型：[10, 011, 101]

#### 字符串的符号

##### 正向递增序号 和 反向递减序号 （索引）

|-12|-11|-10|-9|-8|-7|-6|-5|-4|-3|-2|-1|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|请|输|入|带|有|符|号|的|温|度|值|：|
|0|1|2|3|4|5|6|7|8|9|10|11|

##### 索引和切片

索引：<字符串>[M]

`TemperStr[-1]`

切片：<字符串>[M:N]

`TemperStr[0:-1]`

##### 字符串的格式化

`print("转换后的温度值是{:.2f}C".format(C))`

`{}`代表槽，后续变量填充到槽中，`{:.2f}`表示将变量C填充到这个位置时取小数点后两位

#### 评估函数 eval()

去掉参数最外侧引号并执行余下语句的函数

```
>>> eval("1")
1
>>> eval("1+2")
3
>>> eval('"1+2"')
1+2
>>> eval('print("Hello World")')
Hello World
```

> 和Java不同，Java如果运行类似代码，则不需要用eval，思考一些为什么。详细参考[python中for和字符串的用法解释](https://github.com/SimonZhong2025/Waste-Self-Rescue-Scheme/blob/master/Simon%E2%80%98s%20base%20camp/Python/MOOC%20python%E8%AF%AD%E8%A8%80%E7%A8%8B%E5%BA%8F%E8%AE%BE%E8%AE%A1/01%20Python123%E7%AC%AC%E4%B8%80%E5%8D%95%E5%85%83%E7%BB%83%E4%B9%A0%E9%A2%98.md)。

在 Python 中# 後面接的就是註解。

https://docs.python.org/2/tutorial/introduction.html

```Python
# this is the first comment
spam = 1  # and this is the second comment
          # ... and now a third!
text = "# This is not a comment because it's inside quotes."
```

3.1 把 Python 當計算機用

叫出 interpreter 等待 >>> 出現

3.1.1 數字


直接輸入數學式(數字與加減乘除符號)，Python就可幫忙算囉～

```Python
>>> 2 + 2
4
>>> 50 - 5*6
20
>>> (50 - 5.0*6) / 4
5.0
>>> 8 / 5.0
1.6
```

整數 2, 4 的 type 就是 int。
5.0, 1.6 的 type 就是 float。

division `/` 如果分子分母都是 int，那結果就會是 int
如果分子分母之一是 float，那結果就會是 float
算餘數可以用 `%`
`//` 結果是整數，小數部分會拿掉

```Python
>>> 17 / 3  # int / int -> int
5
>>> 17 / 3.0  # int / float -> float
5.666666666666667
>>> 17 // 3.0  # explicit floor division discards the fractional part
5.0
>>> 17 % 3  # the % operator returns the remainder of the division
2
>>> 5 * 3 + 2  # result * divisor + remainder
17	
```

With Python, it is possible to use the ** operator to calculate powers [1]:

`**` 是次方的意思

```Python
>>> 5 ** 2  # 5 squared
25
>>> 2 ** 7  # 2 to the power of 7
128
```

`=` 是用來給變數值的

```Python
>>> width = 20
>>> height = 5 * 9
>>> width * height
900
```

如果有變數沒被 “defined" （也就是沒有被 assigned a value 的意思），硬要用就會出現：

```Python
>>> n  # try to access an undefined variable
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'n' is not defined
``` 

operands 如果參雜著 int 與 float
則 int 會被轉成 float

```Python
>>> 3 * 3.75 / 1.5
7.5
>>> 7.0 / 2
3.5
```

在互動模式下，最後一個printed expression會被 assigned 給 `_`這個變數。

```Python
>>> tax = 12.5 / 100
>>> price = 100.50
>>> price * tax
12.5625
>>> price + _
113.0625
>>> round(_, 2)
113.06
```

Python 也支援 Decimal, Fraction, complex numbers。

3.1.2. 字串

Python 也可用來處理字串。
字串就是('...') 單引號內文字或 ("...") 雙引號內文字。
\ 可用來跳脫引號。

```Python
>>> 'spam eggs'  # single quotes
'spam eggs'
>>> 'doesn\'t'  # use \' to escape the single quote...
"doesn't"
>>> "doesn't"  # ...or use double quotes instead
"doesn't"
>>> '"Yes," he said.'
'"Yes," he said.'
>>> "\"Yes,\" he said."
'"Yes," he said.'
>>> '"Isn\'t," she said.'
'"Isn\'t," she said.'
```

2.1. 把 Interpreter 叫出來！！

https://docs.python.org/2/tutorial/interpreter.html

Python interpreter 通常都被裝在 /usr/local/bin/python ;
請設定好環境變數，讓我們可以在指令列直接打

```bash
Python
```

就可以呼叫出 Interpreter 拉！

叫出來後，想跳出去呢？很簡單！打 Ctrl + D 就搞定拉～
如果跳不出去，那就打 quit() 就一定可以跳出去囉～


確認是否有 command line editing 功能呢，就是叫出 interpreter 後，打 Ctrl + P。
有逼逼叫，就表示有這個功能！


Interpreter 操作的方式就跟 Unix shell 一個樣！不要怕！

另外一種操作方式呢，就是

```bash
python -c "statement"
```

python module 可用下面指令來呼叫

```bash
python -m module [arg] 
```

用 -i 參數可進入 interactive mode

2.1.1. 參數傳遞

用 import sys，sys.argv[0] 值在不同使用時機，會被給予不同值。
沒有給腳本或參數，sys.argv[0] 是 empty string
腳本名如果是 - ，則 sys.argv[0] 是 -
當用了 -c ，sys.argv[0] 是 -c
當用了 -m ，sys.argv[0] 是 full name of the located module

2.1.2. 互動模式

When commands are read from a tty, the interpreter is said to be in interactive mode. In this mode it prompts for the next command with the primary prompt, usually three greater-than signs (>>>); for continuation lines it prompts with the secondary prompt, by default three dots (...). The interpreter prints a welcome message stating its version number and a copyright notice before printing the first prompt:

>>> 開頭就是互動模式的拉～
... 開頭就是接續上面的 prompts 。例如上面有 if statement。詳情看下例

```bash
>>> the_world_is_flat = 1
>>> if the_world_is_flat:
...     print "Be careful not to fall off!"
...
Be careful not to fall off!
```

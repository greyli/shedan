# 蛇蛋

Python 中隐藏的彩蛋和笑话列表。

> Python 比你想象中的更有趣。

### 1. Hello World

```py
>>> import __hello__
Hello World!
```

Note：在 Python 中打印「Hello, World!」最简单的方式。

### 2. Python 之禅

```
>>> import this

The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

Note：Python 设计哲学 & Python 代码风格指南。

### 3. 《Python 之禅》丢失的一行

《Python 之禅》在 [PEP 20](https://www.python.org/dev/peps/pep-0020/#id2) 中引入，它本应该是 20 条格言，但是最终只写了 19 条。

Note：也许只是为了说明在文件的结尾总是应该保留一个空行。

### 4. 一堂简单的人生课

```py
>>> import this
...
>>> love = this
>>> this is love
True
>>> love is True
False
>>> love is False
False
>>> love is not True or False
True
>>> love is not True or False; love is love  # FML
True
```

Note：不是彩蛋，只是一个解释器里的玩笑。

### 5. 反重力漫画

```py
>>> import antigravity
```
Note：这会打开这个 [xkcd 漫画](https://xkcd.com/353)，漫画展示了 Python 有多么简单易学。

### 6. 这不是一个选择，它定义了我们是谁

```py
>>> from __future__ import braces
  File "<stdin>", line 1
SyntaxError: not a chance
```

Note：这用来快速结束任何关于在 Python 中引入大括号的讨论——不可能！

### 7. 起源

「Python」这个名字和蛇的种类没有关系。

Note：实际的来源是 Guido van Rossum 喜欢的电视剧《[Monty Python's Flying Circus](https://en.wikipedia.org/wiki/Monty_Python%27s_Flying_Circus)》

### 8. 反差

下面是打印出《Python 之禅》的 `this.py` 模块的内容：

```py
s = """Gur Mra bs Clguba, ol Gvz Crgref

Ornhgvshy vf orggre guna htyl.
Rkcyvpvg vf orggre guna vzcyvpvg.
Fvzcyr vf orggre guna pbzcyrk.
Pbzcyrk vf orggre guna pbzcyvpngrq.
Syng vf orggre guna arfgrq.
Fcnefr vf orggre guna qrafr.
Ernqnovyvgl pbhagf.
Fcrpvny pnfrf nera'g fcrpvny rabhtu gb oernx gur ehyrf.
Nygubhtu cenpgvpnyvgl orngf chevgl.
Reebef fubhyq arire cnff fvyragyl.
Hayrff rkcyvpvgyl fvyraprq.
Va gur snpr bs nzovthvgl, ershfr gur grzcgngvba gb thrff.
Gurer fubhyq or bar-- naq cersrenoyl bayl bar --boivbhf jnl gb qb vg.
Nygubhtu gung jnl znl abg or boivbhf ng svefg hayrff lbh'er Qhgpu.
Abj vf orggre guna arire.
Nygubhtu arire vf bsgra orggre guna *evtug* abj.
Vs gur vzcyrzragngvba vf uneq gb rkcynva, vg'f n onq vqrn.
Vs gur vzcyrzragngvba vf rnfl gb rkcynva, vg znl or n tbbq vqrn.
Anzrfcnprf ner bar ubaxvat terng vqrn -- yrg'f qb zber bs gubfr!"""

d = {}
for c in (65, 97):
    for i in range(26):
        d[chr(i+c)] = chr((i+13) % 26 + c)

print("".join([d.get(c, c) for c in s]))
```
生成《Python 之禅》的代码本身违背了自己宣扬的风格建议。它丑陋而不美丽，隐式而不直观。

Note：使用了一种叫 [ROT13](https://en.wikipedia.org/wiki/ROT13) 的置换加密法。

### 9. 有没有 C/C++ 用户？

再次引用《Python 之禅》：
```
There should be one-- and preferably only one --obvious way to do it.
```

Note：在很多语言里常常有两种方法做同一件事，即 `--no` 和 `no--`。这一行包含了一个隐藏的示例。

### 10. 命名标识符可以非常酷

```py
>>> from math import pi
>>> π = pi
>>> area = π * r**2

>>> résumé = 'knows Python'
>>> 'Python' in résumé
True

>>> 我的英文名 = 'Grey Li'
>>> 我的英文名
'Grey Li'

>>> import webbrowser
>>> 我的网站 = 'http://greyli.com'
>>> webbrowser.open(我的网站)
```

Note：Python 3 中支持使用 Unicode 字符作为变量名。尽管如此，使用非英文字符作为变量名可能不是一个好主意，不过它确实会让处理科学公式的工作变得更有意思。

### 11. 选一个见面地点

```py
>>> from antigravity import geohash
>>> # Your location, a date and that date's (or most recent) DJIA opening.
>>> # 你的位置，一个日期和这个日期（或最近）对应的道琼斯工业指数。
>>> geohash(37.421542, -122.085589, b'2005-05-26-10458.68')
37.857713 -122.544543
```

这可以用来生成一个 GPS 定位，在基于你所在位置的一个 1 经度长和 1 纬度宽的区域里。

Note：这个函数的源码在 [这里](https://github.com/python/cpython/blob/master/Lib/antigravity.py)，工作原理解释可以在这个 [xkcd 漫画](https://xkcd.com/426/)看到，也许这就是为什么这个函数也放到了 `antigravity` 模块里。

### 12. The FLUFL - Friendly Language Uncle For Life from [PEP 401 -- BDFL Retirement](https://www.python.org/dev/peps/pep-0401)

```py
>>> from __future__ import barry_as_FLUFL
>>> 1 <> 2
True
>>> 1 != 2
  File "<stdin>", line 1
    1 != 2
       ^
SyntaxError: invalid syntax
```

在认识到 Python 3.0 的不等运算符（`!=`）非常糟糕，是手指疼痛导致的错误后，FLUFL（指 Uncle Barry）重新恢复钻石型操作符（`<>`）作为唯一的不等运算符拼写。

Note：[PEP 401](https://www.python.org/dev/peps/pep-0401/) 是一个愚人节玩笑（从编号可以看出来）。这个 PEP 声明 Guido van Rossum 要退休了。他会获得一个新的头衔，叫做「BDEVIL」（Benevolent Dictator Emeritus Vacationing Indefinitely from the Language，去度无限期语言假期的仁慈退休独裁者），接任者将会是 Barry Warsaw（即 Uncle Barry），Uncle Barry 的官方头衔是「FLUFL」（Friendly Language Uncle For Life，终生友好语言叔叔）。

### 13. InPynite?

```py
>>> infinity = float('infinity')
>>> hash(infinity)
314159
>>> hash(float('-inf'))
-314159
```

一个散列值是一个固定尺寸的整型，它会标识一个特定的值。仔细观察，你会发现散列值的无限大是 10^5 x π。有意思的是，在 Python3 中，`hash(float('-inf'))` 将会生成 -10^5 x π，而在 Python 2 中则是 -271828（即 10^5 x e）

Note：[来源](https://www.reddit.com/r/Python/comments/6wrd8t/nice_lil_easter_egg_i_suppose/).

### 14. types.CodeType -  Not for the faint of heart

如果你开始钻进 Python 的内部，你会在 `help` 输出看到一个关于 `types.CodeType` 的警告：不适合心脏脆弱者。

```py
>>> import types
>>> help(types.CodeType)
...
Help on class code in module builtins:                                                    
                                                                                          
class code(object)                                                                        
 |  code(argcount, kwonlyargcount, nlocals, stacksize, flags, codestring,                 
 |        constants, names, varnames, filename, name, firstlineno,                        
 |        lnotab[, freevars[, cellvars]])                                                 
 |                                                                                        
 |  Create a code object.  Not for the faint of heart.                                    
 |                                                                                        
 |  Methods defined here:                                                                 
 |                                                                                                                                       
 ...
 ```

## 贡献

欢迎创建 PR 来添加更多关于 Python 的彩蛋和玩笑。

## License

翻译自 https://github.com/OrkoHunter/python-easter-eggs 项目，原项目没有许可协议，已通过邮件申请获得翻译和发布许可。
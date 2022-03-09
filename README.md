# videodownloadergui

A program that uses Python and has a GUI interface to download web video

一个使用python且拥有GUI界面的可以下载网页视频的程序

## 如何使用？/How To Use?

```cmd
git clone https://github.com/billma007/videodownloadergui.git
cd videodownloadergui
pip install you-get
py video.py
```

## 如何编译？/How to compile it?

我在这一步上面，想我前面的大多数人一样，踩了无数次的坑，都没有成功编译使用you-get驱动的python文件。

经过了一年的探索，至少翻了2本书和数百个网页与维基百科，我找到了如何编译you-get 的python程序的方法。

我不希望再有人来埋这个埋不住的坑。

### 正确编译方式

```cmd
pyinstaller -F video.py  --hidden-import=you_get.cli_wrapper --hidden-import=you_get.processor --hidden-import=you_get.utl --hidden-import=you_get.extractors
```

### 这是什么

我相信大多数人和我一开始想的一样，使用了以下指令：

```cmd
pip install pyinstaller
pyinstaller -F video.pu
```

编译很顺利！我打开编译完的程序，发生了错误：

```cmd
you-get: [error] oops, something went wrong.
you-get: don't panic, c'est la vie. please try the following steps:
you-get:   (1) Rule out any network problem.
you-get:   (2) Make sure you-get is up-to-date.
you-get:   (3) Check if the issue is already known, on
you-get:         https://github.com/soimort/you-get/wiki/Known-Bugs
you-get:         https://github.com/soimort/you-get/issues
you-get:   (4) Run the command with '--debug' option,
you-get:       and report this issue with the full output.
```

#### 第一步

认为这是源代码没有被正确引用的问题~~（思路正确，解决办法错误）~~，于是将you-get的源代码拖到了目录底下。

再编译，没用。

#### 第二步

我发现在python第三方依赖库的目录下有一个已经编译完毕的you-get.exe,我在想，这玩意可不可以用？

把这玩意拖到了`video.exe`的同目录下，可以运行。

我很开心，便把you-get给删了！~~去你的you-get！~~

乐极生悲，删掉原本的you-get库后，youget.exe就不能运行了。。。

![](https://i.imgur.com/GfthFAz.png)

#### 第三步

由上面两步我们可以初步做出判断，这是由于you-get库中部分代码未被编译导致编译完成后的代码缺失，那么我们该怎么才能让这些代码补全到编译后的exe里面呢？

我在研究pyinstaller的文档时发现了这么一个参数：

```cmd
--hidden-import=xxx.xxx
```

~~虽然我英语不好但是~~看这个参数名称触动了我的神经：hidden-import！

我又查阅了~~纯英文的~~由大佬翻译的you-get文档,

**~~此处省略一个月的艰辛~~**

锁定了被“hidden”的文件：

- you_get.cli_wrapper
- you_get.processor
- you_get.utl
- you_get.extractors

加上--hidden-import函数，大功告成！

```cmd
pyinstaller -F video.py  --hidden-import=you_get.cli_wrapper --hidden-import=you_get.processor --hidden-import=you_get.utl --hidden-import=you_get.extractors
```

## 关于作者/About

江苏省苏州市的一个普通高中牲，一个~~因为玩电脑被学校处分~~在省赛就被刷下来的信息学奥林匹克竞赛选手，热爱编程，但不喜欢前端。

欢迎通过以下联系方式与我探讨信息竞赛、博客搭建、学术讨论以及扯皮：

- QQ:36937975
- Twitter:@billma6688
- Facebook/Instagram:billma007
- CodeForces/USACO/AtCoder:billma007(不常用/not use them usually)
- Email:maboning237103015@163.com
- 
## 推广：个人博客/Blog

[欢迎来到我的博客/Welcome Here!](https://billma.top)

## LICENSE

[GNU通用公共许可2.0（GNU/GPL2.0）](LICENSE)

针对采访部分人(全是编程小白)提出的一些问题，在这里进行解答。

**本页面仅适用于编程小白~~和无基础人员~~，有一定基础的请[移步这里](README.md)了解更多 。~~大佬别来~~

## 为什么不能复制粘贴?

~~或许你可以试试看Windows系统自带的快捷键Ctrl+V~~1.1版本将会设计一个快捷按钮直接读取剪贴板内容。

## 为什么我下载以后会显示"用其他应用打开"或者"不支持打开此文件？

~~你特么看看这是什么文件这是exe文件啊~~EXE文件，全名可执行文件，只能在受支持的Windows系统中使用。

## 为什么有两个窗口？黑色窗口能关掉吗？

黑色窗口是主窗口，**是所有软件都有的**，是不能关掉的。程序的一切命令（包括创建窗口等等），都是通过这个黑窗口来实现的(这是让大部分人懂什么意思，**~~如果你懂DOS请略过~~**).具体为什么大部分程序没有是因为他们在编译的时候添加了一条命令隐藏了这个窗口。我是因为为了让大家看到输出的下载进度才没隐藏。

## 弹出窗口"该版本的.exe 与你运行的 Windows 版本不兼容。请查看计算机的系统信息，然后联系软件发布者"或类似问题

该软件是在64位系统的环境编译的。如果你的系统是32位的，那么这个软件就无法使用了。

如果你的系统是64位的，请尝试~~卸载腾讯电脑管家/360~~在杀毒软件中添加该软件的白名单。**如果杀毒软件报毒也是这么处理的**

## 这个软件支持下载哪些？

支持下载部分网站的视频、图片和音乐。BiliBili同时支持下载弹幕。对于拥有反爬虫机制(就是不让你直接获取视频音乐下载地址）的网站（通俗地讲就是我们常说的大网站），支持且**仅支持**[这些网站](https://github.com/billma007/videodownloadergui#%E6%94%AF%E6%8C%81%E7%9A%84%E7%BD%91%E9%A1%B5supported-sites).对于不在列表里但是没有反爬机制的网站，同样支持下载。但是如果该网站反爬且不在列表，我也无能为力。

![](https://i.imgur.com/GfthFAz.png)

## 我能下载VIP视频/大会员番剧/超前点播/付费观看视频/会员专属音乐吗？

由于浏览器cookie的限制，没有登录会员的设备是没法直接获取地址的。但是部分网站可以通过登录有会员的账号来进行爬取：

- 全程**不要使用**无痕浏览/强制刷新/禁用缓存/清除缓存
- 登录**带有会员**的账号，并且勾选“自动登录/记住我”
- 在该会员账号在线的同时复制视频网址到程序里面，部分网站可以下载。

 ## 如果还有问题？
 
 [欢迎联系我](https://github.com/billma007/videodownloadergui#%E5%85%B3%E4%BA%8E%E4%BD%9C%E8%80%85about)
 
 ## 推广：我的博客
 
 [欢迎来访](https://billma.top)

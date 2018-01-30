title: Electron 桌面开发
speaker: zhangyin08
url: https://github.com/ksky521/nodeppt
transition: slide3
theme: moon
files: /js/demo.js,/css/demo.css
date: 2018年01月26日

[slide data-transition='vertical3d']

# Electron
![](/img/electron/logo.jpeg)

<div align=right>
  </br>
  Javascript进行桌面软件开发
</div>

[slide]


# Content

- 什么是electron
- 为什么要使用electron
- electron开发的优点
- 应用场景
- 开发的相关流程
- 一个Demo

[slide]

## 什么是electron ?
----

<img src="/img/electron/components.jpeg" width="600" height="200" background-color:#fff/>

- 构建跨平台桌面应用程序的一个库 {:&.fadeIn}
- HTML + CSS + JavaScript
- Chromium + Node.js ==> Mac && Win && Linux && APP Store

- 不要考虑兼容性，更多最新的chrome特性

    ①Chromium :1-2周

    ②Node.js :1个月



[slide]

## 为什么要使用electron

- 与web开发、原生本地软件开发的区别 {:&.flexbox.vleft}

|| 技术栈|优点 |开发成本|设备访问能力|系统依赖|浏览器依赖|维护性|特点 |
|---|---|---  |:-----:|:---:|---|---   |---|----|---|
| Web |Ng、Vue、React|轻客户端、网页应用|低|低|NO|YES|依赖团队人员技术栈|传统网站开发技术，不依赖系统平台；需考虑个浏览器的差异性；集中部署更新|
| PWA |H5、SW|可靠、快速、粘性|低|低|NO|YES|依赖技术栈|前端技术开发、轻客户端，各浏览器及版本差异较大，支持性逐渐增高；发展前景好|
| 桌面应用 |electron、NW|本地应用、web技术|低|高 |NO|NO|一套技术站、维护性较高|前端开发技术 、不依赖系统平台、无需考虑浏览器及版本差异性，一个内核封装|
| Native |RN、IONIC、Swift...|移动端|高|高|YES|NO|不同技术栈、开发人员少|移动端、不同移动端框架技术栈 不同的系统对各种不同的框架支持个不相同，更新升级复杂|

[slide]
[note]

[PWA官网](https://developers.google.com/web/progressive-web-apps/)、
[PWA相关资料](https://lavas.baidu.com/mip/doc/README)
[/note]

## 为什么要使用electron
----

<img src="/img/electron/compare.png" width="1000" height="1400" background-color:#fff/>

[slide]

# electron应用程序优点
----

- <span class="text-warning">用户体验</span>：客户端独立、本地安装、启动加载时间短、综合体验比网站好、特定人群的使用习惯、

- <span class="text-warning">用户粘性</span>：是另一种产品形式，服务更可靠，入口常住，易触达，用户留存;

- <span class="text-warning">开发角度</span>：技术栈统一(JS+nodeJS)、独立桌面应用、原生系统API、程序崩溃报告

- <span class="text-warning">系统无差异</span>：客户端系统平台差异、不用考虑浏览器的兼容、支持后台热更新

<span class="red">PS:桌面应用的时间要比使用web版平均多34%</span>  {:&.flexbox.vleft}


[slide]

# electron部分概念
----
<div align=left>
Chrome内核封装应用程序
</div>

- 两个进程：
    - <span class="text-warning">主进程main</span>：每个Electron应用的入口，控制应用程序的声名周期；可调用原生系统API,内置Node API
    - <span class="text-warning">渲染进程renderer</span>：应用程序的窗口，无本地资源访问权限
- 通讯机制：
    - 主进程、渲染进程两者之间是通过ipc进行通讯。main端有ipcMain， 渲染进程端有 ipcRenderer，分别用于通讯
-

<div class="columns3">
    <div align="center">
       <img src="/img/electron/msg1.png" width="400" height="200" background-color:#fff/>
    </div>
    <div align="center">
        <img src="/img/electron/msg2.png" width="400" height="200" background-color:#fff/>
     </div>
</div>

[slide]


# 主要概念

-----
<img src="/img/electron/concept.png" width="1200" height="1000" background-color:#fff/>


[note]
app:应用程序模块，常用生命周期钩子①will-finish-lanuching；②ready；③will-all-closed；④before-quit；⑤will-quit；⑥quit
BrowserWindow：事件钩子：①closed；②focus；③show；④hide；⑤maxmize；⑥minimize；…

[/note]
[slide]


# 应用场景

-----

- 聊天应用、开发工具、应用程序
- VScode skype、网易云音乐、Atom、GraphiQL、钉钉、微信开发者平台......
<img src="/img/electron/electron-demo.png" width="1200" height="1000" background-color:#fff/>

[slide]

# 开发的相关流程

[magic data-trasition="slide3"]

<img src="/img/electron/devFlow.png" width="1600" height="1400" background-color:#fff/>

[/magic]

[note]
1. Github desktop为什么使用electron重写
> 之前开发不同平台的应用需要使用不同平台的技术，及同一个应用，要维护两套技术栈；
> 比如开发mac上的native app可以使用Xcode, Swift, and AppKit；
> 开发windows上native app可以使用Visual Studio, C#, and WPF or UWP。
> 开发阶段，不需要重新编译、打开app，而只是修改完代码，重新加载就可以看到改变

[/note]


[slide ]

# 下面是一个Demo

----

title: Git 与工作流
speaker: hbzyin
url: https://github.com/ksky521/nodeppt
transition: slide3
theme: moon
files: /js/demo.js,/css/demo.css
date: 2017年07月29日

[slide data-transition='vertical3d']

# Git 与工作流
### 演讲者：hbzyin

<div align=right>
  Email: hbzyin@163.com
</div>

[slide]


## 什么是 Git ?

- ![](/img/linus.png) {:&.fadeIn}

- Linus Torvards 用了10天时间开发的版本控制系统

- 为了管理Linux 内核版本，解决与 Bitkeeper的授权纠纷

- 相关人物：Linus Torvalds、Adrew Tridgell、Larry MacVoy

[slide]

## 你会使用git ?
----


- `git gc`

- `git stash`

- `git stash pop`

- `git cherry-pick  a7192e2`

- `git remote add gh git@github.com:user/project`

- `git filter-branch --force --index-filter 'git rm --cashed --ignore-unmatch tools -r' --prune-empty --tag-name-filter cat -- --all`

[slide]

## Git 原理

<div align=right>
    <p>一个内容寻址文件系统。</p>
</div>

![](/img/git-stage.png 'Git 原理')

[slide]

## Git 三大对象
----

- Blob 对象：主要存储文件内容（不存储文件元信息）

- Tree 对象：存储索引信息，主要用于索引Blob对象和Tree对象

- Commit对象：顶层Tree对象，提交作者的信息，提交记录、日志

[slide]

# Git 工作流程
----

- Git workflow {:&.bounceIn}

- Github workflow

- Gitlab workflow


[slide]

# Git workflow

-----

<div class="columns3">
    <div align="center">
        <img src="/img/workflow/git-workflow.png" width="450" height="200"/>
        <p>Git workflow</p>
    </div>
    <div align="center">
        <img src="/img/workflow/github-workflow.png" width="450"  height="200">
        <p>Github workflow</p>
     </div>
</div>
<br/>
<div class="columns3" >
    <div align="center">
        <img src="/img/workflow/gitlab-workflow-continue.png" width="450"  height="300">
    </div>
    <div align="center">
        <img src="/img/workflow/gitlab-workflow-release.png" width="450"  height="300">
    </div>
</div>

<div align="center">Gitlab workflow</div>

[slide]

# 开源许可证

[magic data-trasition="slide3"]

- 开源不等于放弃 {:&.vitical.vleft}

<div align=center >
   <img src="/img/license/free_software_licenses.png" width="800" >
</div>

====

-  copyRight Or copyLeft

<div align=center >
    <img src="/img/license/software_license.png" width="850" >
</div>

[/magic]

[note]
开源是一种信仰:

- 知识版权 VS 知识共享

- 互联网之子 VS 乳腺癌

![](/img/license/aaron-swartz.png)

[/note]


[slide ]

# Thank you all !

----

<div align=right>
  <div>Email: hbzyin@163.com </div>
   <br/>
  <div>Github:https://github.com/hbzyin</div>
</div>
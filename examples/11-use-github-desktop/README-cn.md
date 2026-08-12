---
description: "用 GitHub Desktop 把 repo clone 到本地, 在本地完成 commit, 建 branch, push, 以及不走 PR 的本地 merge, 建立一套比网页顺手得多的本地工作流."
---

# 用 GitHub Desktop 在本地管理你的 Repo

> 把前面在网页上学过的所有操作, 搬到你自己的电脑上用图形界面轻松完成.

## 1. 概览

这是 "Learn GitHub Basics" 系列的 11 节. 到目前为止, 你所有的操作都是在 GitHub 网页上完成的: 编辑文件, commit, 建 branch, merge. 这些在浏览器里都能做, 但说实话体验一般, 网页编辑器功能有限, 打字手感也一般.

这一节我们换一种更舒服的方式: 用 GitHub Desktop 这个官方桌面应用, 在你自己的电脑上做同样的事. 打个比方, 以前你是在网银的网页里一笔一笔操作, 现在装了一个手机银行 App, 所有动作都变得丝滑流畅. 文件还是那些文件, GitHub 还是那个 GitHub, 只是操作方式舒服多了. 学完这一节, 你之前学过的 clone, commit, branch, push, merge, 都能在本地轻松完成.

---

## 2. 学习目标

先说一个事实: 在真实的工作环境里, 几乎没有人会在 GitHub 网页上写代码或编辑文档. 大家都是在自己电脑上用编辑器把东西写好, 再同步到 GitHub. 这才是专业的工作方式.

为什么? 因为本地的体验是网页完全比不了的: 打字更流畅, 能同时打开多个文件对比, 能离线工作不依赖网络, 还能用各种 AI 辅助工具帮你写. 学会在本地工作, 你就从 "在网页上点点点" 迈进了 "像专业开发者一样工作".

学完这个 Task, 你将能够:

1. 说清 GitHub Desktop 是什么, 以及 local (本地) 和 remote (远程) 的关系.
2. 用 GitHub Desktop 把一个 repo clone 到本地.
3. 在本地完成编辑, commit, 建 branch, 切 branch, 以及 push.
4. 不走 Pull Request, 直接在本地把一个 branch merge 到 main.

---

## 3. 前置知识

- 已完成本课的 03 到 10 节, 对 commit, branch, merge 这些概念不陌生 (你在网页上都做过).
- 一台 Mac 或 Windows 电脑 (GitHub Desktop 两个系统都支持, 操作几乎一样).
- 一个你自己有权限的 repo, 最好就用你在前面几节里创建的那个 public 练习 repo.

---

## 4. 你将构建或学到什么

这一节不写新的代码或文档. 你要做的, 是把之前在网页上学过的所有操作, 在本地完整重做一遍. 做完之后, 你就拥有了一套自己的本地工作流, 这是你以后几乎每天都会用到的技能.

---

## 5. GitHub Desktop 是什么

GitHub Desktop 是 GitHub 官方出的一个桌面应用. 它做的事情很简单: 让你用图形界面来操作 Git, 而不用敲命令行.

你可以把它理解成 GitHub 网页版的 "本地版". 网页上能做的事 (commit, branch, push, merge), 在 GitHub Desktop 里都能做, 而且更直观. 它和网页的分工是这样的:

- GitHub 网页 (github.com): 你的项目存在云端的地方, 按你设的可见性对外开放.
- GitHub Desktop (桌面应用): 你电脑上的一个工具, 负责把本地文件和云端保持同步.

至于用什么编辑文件, 随你喜欢, 记事本, TextEdit 都行, 但更推荐 VS Code (免费, 好用, 最流行). 这一节的主角是 GitHub Desktop, 编辑器只是配角, 你顺手就好.

---

## 6. local 和 remote: 一个必须搞懂的概念

这个概念非常重要, 一定要先搞清楚:

- remote (远程): 指 GitHub 网站上的那个 repo, 你在浏览器里看到的就是它.
- local (本地): 指你电脑上的那个文件夹. 你 clone 一个 repo 之后, 电脑上就有了一份完整副本.

两者靠三个动作来同步:

- Clone: 第一次把远程 repo 完整复制到本地, 只需做一次.
- Pull: 从远程把最新改动拉到本地 (别人改了东西, 你拉过来).
- Push: 把你本地的改动推到远程 (你改了东西, 推上去).

关键点: 你在本地做的一切 (编辑, commit, 建 branch), 在你 push 之前, 都只存在于你自己电脑上, 网页上是看不到的. 只有 push 之后, 远程才会更新. 这其实是一个优势, 你可以在本地随便改, 随便试, 不满意就不 push, 一点都不会影响远程.

---

## 7. 准备: 装好并登录 GitHub Desktop

1. 打开浏览器访问 desktop.github.com, 下载对应你系统 (Windows 或 Mac) 的版本并安装.
2. 打开 GitHub Desktop, 点 Sign in to GitHub.com.
3. 在弹出的浏览器页面里登录你的 GitHub 账号并授权.
4. 登录成功后, GitHub Desktop 会显示你的用户名, 说明它已经和你的账号连上了.

装好登录这一步只需做一次, 之后它就一直记着你了.

---

## 8. Clone: 把 repo 复制到本地

Clone 就是把远程的 repo 完整地复制到你电脑上. 完成后, 你电脑上就有了这个 repo 的所有文件, 可以像打开任何普通文件夹一样打开它.

在 GitHub Desktop 里点 File, 选 Clone Repository, 会弹出下面这个对话框.

![Clone a Repository 对话框, GitHub.com 标签下搜索并选中你的 repo, 设置 Local Path 后点 Clone](img/11-use-github-desktop-01.png)

- 默认的 GitHub.com 标签会列出你有访问权限的所有 repo, 上面还有个搜索框, 输入名字就能筛, 对新手最友好.
- 旁边还有个 URL 标签, 你也可以直接把 repo 的 clone URL (形如 https://github.com/username/repo-name) 粘进去, 效果一样. 只是没有搜索那么省事.

这里有个细节值得留意: 这个列表列的是你有访问权限的全部 repo, 不只是你自己创建的那些. 如果你在某个团队或公司里, 团队的仓库也会出现在这里, 而且是按拥有者分组排列的. 现在你多半只看得到自己那几个, 所以体会不深; 等你手上的仓库来源变多, 这个分组就很有用了. 至于这个 "拥有者" 到底是什么, 12 节会专门讲.

选中你要 clone 的 repo, 在下方 Local Path 里选一个存放位置 (比如桌面上的一个文件夹), 点蓝色的 Clone 按钮, 等几秒就好. 完成后打开那个 Local Path 文件夹, 你就能看到 repo 里的所有文件了.

---

## 9. Commit: 在本地改文件并提交

还记得在 04 节你在网页上点铅笔图标改文件吗? 现在在本地做同一件事.

先在刚才那个本地文件夹里, 用你的编辑器打开某个文件 (比如 README.md), 随便改点内容, 保存. 然后切回 GitHub Desktop, 它已经自动检测到你的改动了.

![GitHub Desktop 的 Changes 标签: 左侧列出被改的文件, 右侧显示 diff, 左下写 Summary 后点 Commit to main](img/11-use-github-desktop-02.png)

- 左侧 Changes 面板列出了哪些文件被改了.
- 右侧显示具体改了什么, 绿色是新增的行, 红色是删掉的行.
- 在左下角的 Summary 框里写一句有意义的 commit message, 然后点蓝色的 Commit to main.

恭喜, 你在本地完成了一个 commit. 但记住一件事: 这个 commit 现在只在你电脑上, 网页上还看不到. 要让它出现在远程, 还得再做一步 push.

---

## 10. Branch: 在本地建和切

还记得 05 节的 branch 吗? 在 GitHub Desktop 里, 建 branch 和切 branch 更直观.

![点顶部 Current Branch 展开面板, 用 New Branch 建新分支, 列表里可切换 main 和其他分支](img/11-use-github-desktop-03.png)

- 建 branch: 点顶部 Current Branch 那一块, 展开面板, 点 New Branch, 起个名字 (比如 dev-local), 基于 main 创建.
- 切 branch: 还是点顶部那一块, 在列表里选你要去的 branch, 点一下就切过去了.

试着在新 branch 上改点东西并 commit, 然后切回 main 看看, 你会发现刚才的改动不见了; 再切回新 branch, 它又回来了. 这就是你在 05 节体验过的 "平行宇宙", 现在本地也能玩, 而且切换更快.

注意: 新建的 branch 也是只活在本地的. 它同样要等你 push (第一次叫 Publish branch) 之后, 才会出现在远程.

---

## 11. Push: 把本地的改动推到远程

本地 commit 和新建 branch 都不会自动同步. 要让它们出现在 GitHub 网页上, 得靠 push.

![GitHub Desktop 顶部的 Push origin 按钮, 旁边的 1 上箭头表示有 1 个本地 commit 待推送](img/11-use-github-desktop-04.png)

- 顶部会出现一个 Push origin 按钮, 旁边的数字 (比如 1 加一个向上箭头) 表示你有几个本地 commit 还没推. 点一下, 等几秒就推上去了.
- 如果是一个刚新建, 还没发布过的 branch, 这个按钮会显示成 Publish branch, 意思一样, 都是把本地的东西同步到远程.

推完之后, 打开浏览器访问这个 repo 的 GitHub 页面, 你刚才的改动和 commit message 就都在上面了. 记住这个节奏: 编辑, commit, push. 前两步在本地, 第三步才真正同步到远程.

---

## 12. 本地 Merge: 不走 PR 直接合

在 06 节你学的是在网页上通过 Pull Request 来 merge. 而在本地, 你自己一个人工作时, 可以直接 merge, 更快更简单.

第一步, 先在 GitHub Desktop 里切到 main. 因为你要把别的 branch 合并 "到" main, 所以得先站在 main 上. 然后展开顶部的 branch 面板, 点最底部的 Choose a branch to merge into main.

![切到 main 后, 展开 branch 面板, 点最底部的 Choose a branch to merge into main](img/11-use-github-desktop-05.png)

第二步, 在弹出的 Merge into main 窗口里, 选中你要合并过来的那个 branch (比如 dev-local). 窗口会告诉你这次会把几个 commit 合过来, 确认后点 Create a merge commit.

![Merge into main 窗口: 选中源分支, 提示将合并 N 个 commit, 点 Create a merge commit](img/11-use-github-desktop-06.png)

合并完成后, 在 main 上打开文件看看, 你在那个 branch 上加的东西现在也出现在 main 里了. 别忘了最后 Push origin, 把合并后的 main 推到远程.

这里要讲清一个关键区别. 本地 merge 和 Pull Request 做的是同一件事, 都是把一个 branch 的改动并进另一个 branch. 区别在于: PR 多了 review (审查) 和记录这两个环节, 适合团队协作, 谁改了什么, 为什么合, 都留痕; 而本地 merge 没有 review, 也没有那条 PR 记录, merge 就 merge 了. 当这个 repo 只有你自己一个人用时, 本地 merge 完全够用, 还省事. 一旦涉及和别人协作, 就该回到 PR.

---

## 13. 练习

### 练习 1: 把你自己的 repo clone 下来, 在本地走一遍

**目标:** 用 GitHub Desktop 加本地文件夹, 把 clone, commit, branch, push, 本地 merge 完整做一遍.

**怎么做:**

1. 先想清楚你要练哪个 repo. 用你前面几节里自己创建的那个 public 练习 repo 最合适, 它在你自己账号下, 你有权限, 随便折腾. 如果记不清仓库名, 去 github.com/USERNAME?tab=repositories (USERNAME 换成你的用户名) 看一眼.
2. 在 GitHub Desktop 里 File, Clone Repository, 在 GitHub.com 标签下搜到它, 选好 Local Path, 点 Clone.
3. 在本地文件夹里用编辑器改一个文件, 保存, 回到 GitHub Desktop 写 commit message, Commit to main.
4. 点 Push origin, 然后去 GitHub 网页确认改动上去了.
5. 新建一个 branch (比如 dev-local), 在上面改点东西并 commit, 切回 main 感受一下改动的出现和消失.
6. 切到 main, 用 Choose a branch to merge into main 把那个 branch 本地 merge 进来, 最后再 Push origin.

**你会观察到:**

同样一套 clone, commit, branch, push, merge, 在本地做起来比网页顺手得多. 而且你会清楚地感觉到那条边界: 本地做的事, push 之前网页上看不到; push 之后, 网页立刻就同步了.

> **关键洞见:** 你不是在学一堆新概念, 你是在把已经会的操作换到一个更专业, 更舒服的环境里做. 工具变了, 底层的 Git 逻辑一模一样.

---

## 14. 回顾: 网页和本地的对照

- 编辑文件: 以前在网页点铅笔在小框里改; 现在在本地用编辑器像改 Word 一样改.
- Commit: 以前在网页点 Commit changes; 现在在 GitHub Desktop 写 Summary 点 Commit.
- 建 Branch: 以前在网页的分支选择器里输名字; 现在在 GitHub Desktop 点 New Branch.
- Push: 以前在网页 commit 就直接存到远程了; 现在本地 commit 之后要额外点一下 Push origin.
- Merge: 以前在网页走 Pull Request; 现在自己一个人可以在本地 Branch 菜单里直接 merge.
- 核心区别就一个: 网页上的操作直接作用在远程, 本地操作要 push 才会同步到远程.

---

## 15. 导师寄语

**为什么这节是一个转折点:**

从今天起, 你的工作方式发生了质的变化. 之前你所有操作都依赖浏览器: 打开网页, 点铅笔, 在小框里改几个字, 点保存. 这种方式能用, 但很受限. 现在, 你有了一套完整的本地工作环境, 编辑器负责写, GitHub Desktop 负责管版本. 这不只是换了个工具, 它意味着你可以像专业开发者一样工作了: 一次打开整个项目, 离线也能改和 commit, 改的东西 push 之前只有你自己看得到, 不怕改错被人看见.

**关键洞见:**

- 本地和远程的那条界线, 是这一节最值钱的概念. 想清楚 "这一步只在本地, 还是已经同步到远程", 你就不会再犯 "我明明改了为什么网页上没有" 这种迷糊.
- 本地 merge 和 PR 不是谁取代谁, 而是各有场景: 一个人图快用本地 merge, 要协作要留痕就用 PR.
- 工具越顺手, 你就越愿意频繁地 commit 和记录. 顺手本身, 就是一种生产力.

**下一步:**

给自己养成一个固定节奏: 打开 GitHub Desktop 选好 repo, 先 Fetch origin 看看远程有没有更新, 再用编辑器改, 改完 commit, 然后 push. 熟练之后整个过程不到十秒, 会变成像按保存一样的肌肉记忆.

---

## 16. 速查

**GitHub Desktop 核心操作:**

- Clone repo: File, Clone Repository, 在 GitHub.com 标签搜索或在 URL 标签粘贴地址.
- 建 branch: 点顶部 Current Branch, New Branch.
- 切 branch: 点顶部 Current Branch, 在列表里选目标 branch.
- Commit: 左下写 Summary, 点 Commit to [branch].
- Push: 顶部 Push origin (新 branch 第一次是 Publish branch).
- 本地 merge: 先切到目标 branch, 再 Choose a branch to merge into [branch], 选源 branch, Create a merge commit.

**下载链接:**

- GitHub Desktop: desktop.github.com
- VS Code (可选的编辑器): code.visualstudio.com

**一句话记住:** 编辑, commit, push, 本地做的事 push 之后才同步到远程.

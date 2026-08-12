---
description: "读完你手里有整门课的地图: 知道它分成哪九块, 每块解决什么问题, 各块之间为什么是这个顺序, 以及自己该从哪一篇开始往下读."
---

# Learn GitHub Basics 系列索引

这门课带你从零走完 GitHub 的基础工作流: 先交代 Git 与 GitHub 的来历, 再从纯网页操作起步, 落到本地桌面工具, 最后回头把整条路连成一条主线. 从 03 到 10 全程只用浏览器, 都在你自己的一个 repo 上操作, 一篇接一篇地长起来. 下面的 12 个 mini task 分成九块: 先搞清背景 (这两个名字很像的东西各是什么, 以及这块地方凭什么也属于不搞技术的人), 再打好地基 (有地方放东西, 会改东西), 接着掌握 Git 的核心工作流 (branch 加 merge), 然后完成一次观念转变 (把一切都放到 GitHub 上), 再学会掌控访问权 (分清 public 和 private, 并把对的人邀请进来协作), 接着打开自动化的入口 (让程序凭 token 代表你操作 GitHub), 再把这套操作搬到本地 (用 GitHub Desktop 在自己电脑上工作), 然后走出自己的一亩三分地 (认清每个仓库都属于某个 owner, 学会在 organization 里找仓库), 最后回顾与展望 (把整门课连成主线, 看清下一步往哪走).

## 1. 先搞清背景: Git 和 GitHub 到底是什么

这一组不动手, 只把两个名字很像的东西分清楚, 算明白 GitHub 那份免费是怎么来的, 再破掉一个很贵的误解: 这地方不是程序员专属. 后面所有操作都落在这张底图上.

- [02-story-behind-git-and-github](../02-story-behind-git-and-github/README-cn.md): 搞清 Git 和 GitHub 各自是什么, 分别从哪来, 两者什么关系, GitHub 凭什么敢让你免费用, 以及为什么它那套作品加社交的构造, 对不写代码的人同样是作品与职场的敲门砖.

---

## 2. 打好地基: 有个地方放东西, 会改东西

这一组解决最基本的问题: 你得先有一个自己的项目空间, 并且能在里面自如地改文件.

- [03-create-repo](../03-create-repo/README-cn.md): 从零创建你的第一个 Public Repository, 理解它为什么是项目的容器, 协作的单位和权限的单位, 并用匿名窗口验证它对全世界可见, 还能随时从头像菜单把它找回来.
- [04-edit-files](../04-edit-files/README-cn.md): 直接在浏览器里打开, 编辑并 commit 文件, 把改动保存到 main, 不需要任何本地软件.

---

## 3. Git 的核心工作流: 分支与合并

有了地基, 这一组教你 Git 最有价值的两个动作: 开一条平行分支去安全地实验, 再把满意的成果合并回主线.

- [05-working-with-git-branch](../05-working-with-git-branch/README-cn.md): 创建 branch 开辟平行宇宙, 在独立分支上修改而不影响 main, 亲手体验分支隔离.
- [06-merge-branch](../06-merge-branch/README-cn.md): 用 Pull Request 把分支的成果 merge 回 main, 走完 Commit, Branch, Merge 的完整闭环.

---

## 4. 养成习惯: 把一切都放到 GitHub 上

会用工具只是起点. 这一组是整门课价值最大的一篇, 它要你完成一次观念转变.

- [07-put-everything-on-github](../07-put-everything-on-github/README-cn.md): 理解为什么 GitHub 比 Word 和 Google Docs 更适合长期记录, contribution graph 为什么是你最可信的简历, 并把一份真实文档搬上 GitHub.

---

## 5. 掌控访问权: 谁能看, 谁能改

前面用的都是 public repo, 图省心. 但真实世界里, 你必须能精确控制谁能看到, 谁能修改. 这一组先教你可见性 (public 和 private), 再教你怎么把特定的人邀请进来一起工作.

- [08-create-private-repo](../08-create-private-repo/README-cn.md): 创建一个 Private Repository 并用匿名窗口验证它对外返回 404, 学会判断什么内容该 private, 守住 secret 不进 public repo 这条安全红线.
- [09-add-collaborator](../09-add-collaborator/README-cn.md): 用精确的 GitHub username 把同学或老师邀请成 collaborator, 理解默认读写权限, 并牢记没有邀请就没有协作.

---

## 6. 打开自动化的入口: 让程序代表你操作

前面都是你本人在网页上点. 但你在网页上能做的一切, 程序也能做, 前提是它得有办法证明 "我是代表你来的". 这一块教你那把钥匙.

- [10-create-access-token](../10-create-access-token/README-cn.md): 生成一个只有 repo 权限的 Personal Access Token 并用密码管理器安全保存, 理解它是给机器用的密码, 为什么比密码更安全, 以及它随时可撤销.

---

## 7. 搬到本地: 用桌面工具工作

前面都是在网页上点. 但真实工作里, 大家都在自己电脑上写东西再同步. 这一块教你把整套操作搬到本地.

- [11-use-github-desktop](../11-use-github-desktop/README-cn.md): 用 GitHub Desktop 把 repo clone 到本地, 在本地完成 commit, 建 branch, push, 以及不走 PR 的本地 merge, 建立一套比网页顺手得多的本地工作流.

---

## 8. 走出自己的一亩三分地: 仓库到底属于谁

前面这些篇, 你操作的一直是自己创建的仓库. 可一旦开始和别人打交道, 你碰到的大部分仓库就不是你建的了. 这一块解决那个几乎人人都撞过的困惑: 别人说仓库分享给你了, 你却在自己的列表里怎么翻都翻不到.

- [12-understand-github-organization](../12-understand-github-organization/README-cn.md): 看懂每个 repo 都挂在一个 owner 名下, 分清个人账号和 organization, 学会在 organization 里搜到那个仓库, 并明白自己建仓库时同样在选 owner.

---

## 9. 回顾与展望: 把整条路连成主线

最后这一块是整门课的收尾, 单独占一组. 它不教新操作, 而是帮你把前面学过的连成一条线, 确认自己的水平, 并看清下一步往哪走.

- [13-recap-and-next-steps](../13-recap-and-next-steps/README-cn.md): 把整门课梳理成四段主线, 对照自评表确认自己能独立做到什么, 并看清跨出 "一个人" 这层的两条路 (上班和开源), 知道会 PR 就是那把共同的钥匙.

---

## 10. 小结

把这九块连起来, 你会经历一条完整的成长线: 从 "我搞清了 Git 和 GitHub 各是什么, 也知道这块地方有我的位置" 到 "我有一个 repo", 再到 "我会在里面改文件", 接着到 "我能用 branch 和 merge 像专业团队一样工作", 然后到 "我把一切工作都沉淀在 GitHub 上", 再到 "我拎得清什么该公开, 什么该私有, 还能把对的人请进来协作", 接着到 "我能让程序凭 token 代表我操作 GitHub", 然后到 "我能在自己电脑上用桌面工具专业地工作", 再到 "我拿到任何一个仓库都知道它属于谁, 该去哪找", 最后回过头, "我能把这一切连成一条主线, 也看清了下一步往哪走".

学完这条线, GitHub 就不再是一个陌生的程序员工具, 而是你日常协作和版本管理的默认主场. 而这恰恰是关键: 把 GitHub 当作你自己的主要工作区, 这门课教的已经足够了. 至于跨出一个人这层, 无论是和同事上班协作, 还是给开源社区贡献, 那把钥匙你在 06 节就已经拿到了, 会 PR, 剩下的等你需要时再走出去就是.

从 02 开始, 按编号一篇篇往下读就行.

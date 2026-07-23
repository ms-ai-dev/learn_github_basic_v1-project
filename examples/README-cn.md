# Learn GitHub Basics 系列索引

这门课带你从零走完 GitHub 网页端的基础工作流. 全程只用浏览器, 从头到尾都在你自己的一个 repo 上操作, 一节接一节地长起来. 下面的 8 个 mini task 分成五块: 先打好地基 (有地方放东西, 会改东西), 再掌握 Git 的核心工作流 (branch 加 merge), 接着完成一次观念转变 (把一切都放到 GitHub 上), 然后学会掌控访问权 (分清 public 和 private, 并把对的人邀请进来协作), 最后打开自动化的入口 (让程序凭 token 代表你操作 GitHub).

## 1. 打好地基: 有个地方放东西, 会改东西

这一组解决最基本的问题: 你得先有一个自己的项目空间, 并且能在里面自如地改文件.

- [01-create-repo](01-create-repo/README-cn.md): 从零创建你的第一个 Public Repository, 理解它为什么是项目的容器, 协作的单位和权限的单位, 并用匿名窗口验证它对全世界可见.
- [02-edit-files](02-edit-files/README-cn.md): 直接在浏览器里打开, 编辑并 commit 文件, 把改动保存到 main, 不需要任何本地软件.

---

## 2. Git 的核心工作流: 分支与合并

有了地基, 这一组教你 Git 最有价值的两个动作: 开一条平行分支去安全地实验, 再把满意的成果合并回主线.

- [03-working-with-git-branch](03-working-with-git-branch/README-cn.md): 创建 branch 开辟平行宇宙, 在独立分支上修改而不影响 main, 亲手体验分支隔离.
- [04-merge-branch](04-merge-branch/README-cn.md): 用 Pull Request 把分支的成果 merge 回 main, 走完 Commit, Branch, Merge 的完整闭环.

---

## 3. 养成习惯: 把一切都放到 GitHub 上

会用工具只是起点. 这一组是整门课价值最大的一节, 它要你完成一次观念转变.

- [05-put-everything-on-github](05-put-everything-on-github/README-cn.md): 理解为什么 GitHub 比 Word 和 Google Docs 更适合长期记录, contribution graph 为什么是你最可信的简历, 并把一份真实文档搬上 GitHub.

---

## 4. 掌控访问权: 谁能看, 谁能改

前面用的都是 public repo, 图省心. 但真实世界里, 你必须能精确控制谁能看到, 谁能修改. 这一组先教你可见性 (public 和 private), 再教你怎么把特定的人邀请进来一起工作.

- [06-create-private-repo](06-create-private-repo/README-cn.md): 创建一个 Private Repository 并用匿名窗口验证它对外返回 404, 学会判断什么内容该 private, 守住 secret 不进 public repo 这条安全红线.
- [07-add-collaborator](07-add-collaborator/README-cn.md): 用精确的 GitHub username 把同学或老师邀请成 collaborator, 理解默认读写权限, 并牢记没有邀请就没有协作.

---

## 5. 打开自动化的入口: 让程序代表你操作

前面都是你本人在网页上点. 但你在网页上能做的一切, 程序也能做, 前提是它得有办法证明 "我是代表你来的". 这一块教你那把钥匙.

- [08-create-access-token](08-create-access-token/README-cn.md): 生成一个只有 repo 权限的 Personal Access Token 并用密码管理器安全保存, 理解它是给机器用的密码, 为什么比密码更安全, 以及它随时可撤销.

---

## 6. 小结

把这五块连起来, 你会经历一条完整的成长线: 从 "我有一个 repo" 到 "我会在里面改文件", 再到 "我能用 branch 和 merge 像专业团队一样工作", 接着到 "我把一切工作都沉淀在 GitHub 上", 然后到 "我拎得清什么该公开, 什么该私有, 还能把对的人请进来协作", 最后到 "我能让程序凭 token 代表我操作 GitHub". 学完这条线, GitHub 就不再是一个陌生的程序员工具, 而是你日常协作和版本管理的默认主场.

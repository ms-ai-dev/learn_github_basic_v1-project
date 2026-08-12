---
description: "用 GitHub Desktop 把自己的 repo clone 到本地, 并在本地完整走一遍 commit, 建 branch, push, 以及不走 PR 的本地 merge."
---

# 用 GitHub Desktop 在本地走一遍完整工作流

## 1. 目标

在自己的电脑上用 GitHub Desktop, 把之前在网页上学过的操作全部重做一遍. 通过这个任务, 你要真正理解 local 和 remote 的关系, 并掌握 clone, 本地 commit, 建切 branch, push, 以及本地 merge 这一整套动作.

---

## 2. 要做的事情

1. 阅读本节 README, 弄清 GitHub Desktop 是什么, 以及 local 和 remote 的区别.
2. 装好 GitHub Desktop 并登录你的 GitHub 账号.
3. 用 GitHub Desktop 把你自己的一个 repo (建议用前面创建的 public 练习 repo) clone 到本地. 记不清仓库名就去 github.com/USERNAME?tab=repositories (USERNAME 换成你的用户名) 看一眼.
4. 在本地文件夹里用编辑器改一个文件, 保存, 回到 GitHub Desktop 完成一个 commit.
5. 点 Push origin 把改动推到远程, 并在 GitHub 网页上确认改动出现了.
6. 新建并切换一个 branch, 在上面改动并 commit, 感受切换 branch 时改动的出现与消失.
7. 切到 main, 用 Choose a branch to merge into main 把那个 branch 本地 merge 进来, 再 Push origin.

**预计用时:** 15 分钟左右

---

## 3. 检查清单

- [ ] **理解 local 和 remote**: 能说清本地改动在 push 之前不会出现在远程.
- [ ] **装好并登录**: 装好了 GitHub Desktop 并登录了 GitHub 账号.
- [ ] **Clone 成功**: 把自己的一个 repo clone 到了本地, 能在本地文件夹里看到它的文件.
- [ ] **本地 commit**: 在本地编辑了文件, 并在 GitHub Desktop 里完成了一个 commit.
- [ ] **Push 成功**: 把本地 commit push 到了远程, 并在 GitHub 网页上确认了改动.
- [ ] **建切 branch**: 新建了一个 branch, 在上面做了修改, 并体验了切换 branch 时改动的出现与消失.
- [ ] **本地 merge**: 不走 PR, 在本地把一个 branch merge 进了 main.
- [ ] **懂本地 merge 与 PR 的区别**: 能说清本地 merge 没有 review 和记录, 适合个人; PR 有审查和留痕, 适合团队.

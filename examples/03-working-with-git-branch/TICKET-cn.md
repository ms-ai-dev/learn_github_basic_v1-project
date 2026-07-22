---
description: "在自己的 repo 上创建 dev-1 分支, 让 main 的 README 显示 v1 而 dev-1 显示 v2, 并能通过切换分支演示两者互不影响."
---

# 用分支管理你的平行宇宙

## 1. 目标

理解 Branch 是什么, 何时用, 并在你自己的 repo 上完整走一遍分支流程: 在 main 上提交 v1, 新建 dev-1 分支, 在 dev-1 上提交 v2, 最后通过来回切换亲眼看到分支隔离. 做完这一节, 你就掌握了 GitHub 网页端最核心的分支操作.

---

## 2. 要做的事情

1. 阅读本节 README, 理解 Branch 是什么, 以及什么时候该用它.
2. 在你自己 repo 的 main 分支上编辑 README, 加一行 v1, 然后 Commit.
3. 从 main 创建一个新分支 dev-1.
4. 切到 dev-1 分支, 把 README 里的 v1 改成 v2, 然后 Commit.
5. 切回 main, 确认 README 仍然显示 v1.
6. 再切到 dev-1, 确认 README 显示 v2, 体验分支切换.

**预计用时:** 15 到 20 分钟

---

## 3. 检查清单

- [ ] **理解 Branch 概念**: 读完 README, 你能说清 Branch 是什么, 以及它的典型使用场景.
- [ ] **main 上提交 v1**: main 分支的 README 里有一行 v1, 且已经 Commit.
- [ ] **创建了 dev-1 分支**: 分支切换器里能看到并切换到 dev-1.
- [ ] **认得当前分支**: 任意时刻都能通过左上方的分支切换器看出自己现在在哪个 branch, 以及 repo 里一共有几个 branch.
- [ ] **dev-1 上提交 v2**: dev-1 分支的 README 显示 v2, 且已经 Commit.
- [ ] **验证分支隔离**: 切回 main 时 README 仍是 v1, 切到 dev-1 时是 v2, 你亲自体验了两个分支互不影响.

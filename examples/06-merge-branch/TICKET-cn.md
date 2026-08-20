---
description: "在你自己的 repo 里为 dev-1 创建并合并一个 Pull Request, 让 main 上的 README 从 v1 变成 v2."
---

# 用 Pull Request 把分支合并回 main

## 1. 目标

在上一节, 你在 dev-1 分支上把 README 改成了 v2. 本节你要把这份成果正式合并回 main. 你会先读懂 Merge 和 Pull Request 的概念, 然后动手为 dev-1 创建一个 PR, 完成合并, 最后切回 main 确认改动生效. 完成后, 两个平行分支合二为一, main 上的 README 显示 v2.

---

## 2. 要做的事情

1. 读本节 README, 理解 Merge 和 Pull Request 是什么, 以及一个 PR 从创建到合并的完整流程.
2. 确认已完成上一节: dev-1 分支上的 README 内容是 v2.
3. 在 dev-1 分支页面, 点顶部黄色横幅里的 "Compare & pull request" (如果没看到, 用 "Pull requests" 标签下的 "New pull request" 手动创建).
4. 填好 PR 的标题和描述, 确认对比方向是从 dev-1 合并到 main 且显示 "Able to merge", 然后点 "Create pull request".
5. 在 PR 详情页点 "Merge pull request", 再点 "Confirm merge" 完成合并.
6. 切回 main 分支, 确认 README 现在显示 v2.
7. (可选) 点 "Delete branch" 删除已经合并完的 dev-1, 保持仓库整洁.

**预计用时:** 15 到 30 分钟

---

## 3. 检查清单

- [ ] **读懂 Merge 与 PR**: 你能用自己的话说清 Merge 是什么, Pull Request 是什么, 以及 Conflict 大致是怎么回事.
- [ ] **看懂合并方向**: 在 PR 页面能认出 base (target) 是 main, compare (source) 是 dev-1, 确认改动方向是从 dev-1 到 main.
- [ ] **成功创建 PR**: 为 dev-1 创建了一个 Pull Request, 标题和描述都填写清晰.
- [ ] **成功合并**: 完成合并, 页面出现紫色的 "Merged" 标签.
- [ ] **验证 main 上的结果**: 切回 main 分支后, README 现在显示 v2.
- [ ] **了解 Conflict 概念**: 你明白冲突是同一位置的不同修改导致的, 需要人工决定, 且单人操作不会遇到.

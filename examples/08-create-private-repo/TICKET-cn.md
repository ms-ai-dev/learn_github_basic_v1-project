---
description: "成功创建一个 Private Repository, 用匿名窗口确认它对外返回 404 不可见, 认得 Private 标记, 并能说清何时该用 private 以及在 Danger Zone 切换 visibility 的方法."
---

# 创建一个 Private Repository 并验证它对外隐身

## 1. 目标

亲手创建一个 Private Repository, 并用匿名窗口验证 "全世界真的看不到它". 通过这个任务, 你要建立起对 visibility 的正确判断: 知道什么内容该 public, 什么该 private, 知道 public 泄露不可逆的严重性, 也知道在 Settings 里怎么切换可见性.

---

## 2. 要做的事情

1. 阅读本节 README, 理解 public 和 private 的本质区别, 以及什么时候该用 private.
2. 按 README 第 7 节的步骤, 新建一个 repo, Choose visibility 选 Private, 并勾选 Add a README.
3. 创建后确认仓库名旁边显示的是 Private 标记.
4. 复制这个 repo 的 URL, 在浏览器匿名窗口里打开, 确认返回的是 404 而不是你的 repo.
5. 进入 Settings, General, 拉到最底部的 Danger Zone, 找到 Change visibility, 把 repo 切成 Public 再切回 Private, 观察标记的变化.
6. 能用自己的话说清楚: 为什么不能把 secret 提交进 public repo, 以及为什么 public 内容泄露后收不回来.

**预计用时:** 15 分钟左右

---

## 3. 检查清单

- [ ] **理解可见性**: 读完本节 README, 能说清 public 和 private 的区别, 以及各自适合放什么.
- [ ] **创建成功**: 成功创建了一个 Visibility 为 Private 的 Repository.
- [ ] **认得标记**: 在 repo 主页看到了仓库名旁边的 Private 标记.
- [ ] **验证隐身**: 在匿名窗口里打开这个 private repo 的 URL, 确认返回 404, 未登录的人看不到它.
- [ ] **切换可见性**: 在 Settings, General, Danger Zone 里把 repo 在 Private 和 Public 之间切换过一次, 并切回 Private.
- [ ] **懂安全红线**: 能说清为什么密码, key, 私钥这类 secret 绝不能进 public repo.
- [ ] **懂不可逆性**: 能说清为什么 public 内容一旦泄露 (被 fork, mirror) 就再也删不掉.

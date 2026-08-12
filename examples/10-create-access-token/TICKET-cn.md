---
description: "成功生成一个只有 repo 权限的 classic Personal Access Token 并用密码管理器保存, 能说清 token 和密码的区别, 并知道它随时可以一键撤销."
---

# 生成并安全保存一个 GitHub Personal Access Token

## 1. 目标

亲手生成一个专门给程序用的 GitHub Personal Access Token, 把它安全地存进密码管理器. 通过这个任务, 你要真正理解 token 和密码的区别, 学会遵循最小权限原则只给必要的权限, 并知道 token 随时可以撤销和重建.

---

## 2. 要做的事情

1. 阅读本节 README, 理解 token 为什么是 "给机器用的密码", 以及它凭什么比直接用密码安全.
2. 在地址栏进入 github.com/settings/tokens, 选择 Tokens (classic).
3. 点 Generate new token (classic), 按提示输密码确认身份.
4. 填写 Note (一个能认出用途的名字), Expiration 选 90 days, Select scopes 只勾 repo 这一项.
5. 生成后立刻复制那串以 ghp_ 开头的 token, 并存进密码管理器 (1Password, Bitwarden 等), 记上权限和日期.
6. (可选) 回到 token 列表, 撤销一个 token, 观察你的账号和仓库毫发无损, 亲身体会它的可丢弃.

**预计用时:** 15 分钟左右

---

## 3. 检查清单

- [ ] **理解 token**: 能说清 token 是给机器用的密码, 以及它和你本人登录密码的区别.
- [ ] **进入正确页面**: 进入了 github.com/settings/tokens, 选择了 Tokens (classic) 而不是 fine-grained.
- [ ] **最小权限**: 只勾选了 repo 一项权限, 没有多勾其他权限.
- [ ] **成功生成**: 成功生成了 token, 并复制了那串以 ghp_ 开头的字符串.
- [ ] **安全保存**: 把 token 存进了密码管理器, 没有把它明文放在聊天记录, 记事本或桌面文件里.
- [ ] **懂只显示一次**: 明白 token 只显示一次, 刷新后无法找回, 只能重新生成.
- [ ] **懂可撤销**: 能说清 token 随时可以一键撤销, 且撤销不会影响账号本身, 这正是它比密码安全的地方.
- [ ] **懂身份与权限**: 知道 token 既能证明 "你是你" (身份), 也能界定 "你能做什么" (权限), 这是两件事.

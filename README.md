# hello-github

这个仓库不是作品集，是用来验证「本机 Git → GitHub」整条链路是否打通的最小样例。

## 验证目标

- 本地 Git 能正常提交
- SSH 密钥能通过 GitHub 认证（推送不输密码）
- 能推送到远程 `main` 分支

## 验证结果

| 项目 | 结果 |
|---|---|
| 首次推送 | 2026-11-22 00:22，提交 `2025606` |
| 认证方式 | ed25519 SSH key（无口令） |
| 远程分支 | `origin/main` 与本地同步 |
| 最近更新 | 2026-11-22 16:40，验证记录随文档维护同步刷新 |

> 完整的提交历史请用 `git log --oneline` 查看，本表只保留关键节点，避免与最新提交脱节。

## 复现命令

先确认前置条件：

```bash
ssh -T git@github.com          # 应返回 Hi cql0904!
git config --global user.name  cql0904
git config --global user.email 1217093462@qq.com
```

再跑主流程：

```bash
git clone git@github.com:cql0904/hello-github.git
cd hello-github
git commit --allow-empty -m "test: pipeline check"
git push
```

## 仓库信息

- 账号：cql0904
- 初始化：2026-11-22 00:22:11

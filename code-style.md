# 分支说明

```text
anganing/art-design-pro (Forked from Daymychen/art-design-pro)
│
├── main 🌿  -  同步上游 main 分支
│   │
│   ┌─ 开发规则 ────┐
│   │  • 🚫 禁止直接提交代码             │
│   │  • ✅ 仅接受来自 merge 分支的合并请求 │
│   └─────────────┘
│
├── dev 🚀  -  主开发分支 (从 merge 分支切出)
│   │
│   ┌─ 开发规则 ────┐
│   │  • 🚫 禁止从 upstream/* 分支合并    │
│   │  • ✅ 接受非 upstream/* 分支合并    │
│   └─────────────┘
│
└── merge 🔄  -  同步分支 (从 main 切出)
    │
    └─ 用途：定期合并上游 upstream/main 分支
       → 通过 PR 合并到 main 分支
```

## 同步上游更新流程

```shell
git checkout merge
git merge upstream/main
# 解决冲突后
git commit -m 'fix: resolve upstream conflicts'
git push origin merge
# 视情况将 merger 合并到非上游分支
# .....
```

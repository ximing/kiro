# Git 工作流和分支策略

## 分支命名约定
- 功能分支：`feature/description-of-feature`
- 错误修复：`fix/description-of-bug`
- 紧急修复：`hotfix/critical-issue-description`
- 发布分支：`release/version-number`

## 提交信息格式
遵循约定式提交格式：
```
type(scope): description

[optional body]

[optional footer]
```

类型：feat, fix, docs, style, refactor, test, chore

## Pull Request 指南
- 从功能分支创建 PR 到 main/develop
- 包含清晰的更改描述
- 使用关键词链接相关问题（fixes #123）
- 在请求审查前确保所有测试通过
- 合并时压缩提交以保持历史记录整洁

## 代码审查流程
- 合并前至少需要一个批准
- 审查代码质量、安全性和性能
- 检查测试是否覆盖新功能
- 验证文档是否在需要时更新
- 确保没有破坏性更改，除非有适当的版本控制

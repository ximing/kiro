# 规格驱动开发指南

一个关于使用三阶段规格流程进行系统化功能开发的综合指南：需求 → 设计 → 任务。

<!-- Navigation Metadata -->
<!-- Keywords: spec-driven development, requirements engineering, system design, implementation planning, AI collaboration -->
<!-- Topics: methodology, process, templates, examples, best practices -->
<!-- Audience: developers, project managers, technical leads -->

## 🧭 导航指南

**刚接触规格驱动开发？** → 从 [方法论概述](methodology/README.md) 开始
**准备创建您的第一个规格？** → 跳转到 [流程指南](process/README.md)
**寻找示例？** → 浏览 [示例与案例研究](examples/README.md)
**需要模板？** → 获取 [即用型模板](templates/README.md)
**与 AI 协作？** → 学习 [提示策略](prompting/README.md)

**📍 需要详细导航？** → 查看 [完整导航索引](NAVIGATION.md) - 按角色、问题或学习风格查找内容

---

## 📚 完整目录

### 🎯 [方法论](methodology/README.md)
学习规格驱动开发的基础概念和理念
- [概述](methodology/overview.md) - 核心概念和优势
- [理念](methodology/philosophy.md) - 规格驱动开发为何有效
- [何时使用](methodology/when-to-use.md) - 决策框架和应用场景

### 📋 [流程指南](process/README.md)
三阶段工作流程的分步详解
- [需求阶段](process/requirements-phase.md) - 使用 EARS 收集和构建需求
- [设计阶段](process/design-phase.md) - 创建综合设计文档
- [任务阶段](process/tasks-phase.md) - 将设计分解为可执行的编码任务
- [工作流程图](process/workflow-diagrams.md) - 可视化流程和决策点

### 🧠 [AI 推理](ai-reasoning/README.md)
深入了解决策框架和思维过程
- [决策框架](ai-reasoning/decision-frameworks.md) - 如何评估选择
- [思维过程](ai-reasoning/thought-processes.md) - 分析和优先级排序方法
- [示例](ai-reasoning/examples.md) - 真实推理链和决策点

### 💬 [提示策略](prompting/README.md)
AI 协作的有效沟通技巧
- [策略](prompting/strategies.md) - 核心提示方法
- [模板](prompting/templates.md) - 即用型提示模式
- [最佳实践](prompting/best-practices.md) - 清晰有效沟通的技巧

### ⚡ [执行指南](execution/README.md)
根据规格实现功能的实用指导
- [实现指南](execution/implementation-guide.md) - 分步执行策略
- [质量保证](execution/quality-assurance.md) - 测试和验证技术
- [故障排除](execution/troubleshooting.md) - 常见问题和解决方案

### 📚 [资源](resources/README.md)
精选参考资料和学习材料
- [标准](resources/standards.md) - EARS 和行业标准
- [工具](resources/tools.md) - 推荐工具和集成
- [延伸阅读](resources/further-reading.md) - 额外学习资源

### 📖 [示例](examples/README.md)
真实案例研究和完整规格示例
- [简单功能规格](examples/simple-feature-spec.md) - 基础功能示例
- [复杂系统规格](examples/complex-system-spec.md) - 大型系统示例
- [案例研究](examples/case-studies.md) - 成功故事和经验教训
- [故障排除与陷阱](examples/troubleshooting-pitfalls.md) - 常见错误和恢复策略

### 📝 [模板](templates/README.md)
即用型模板和检查清单
- [需求模板](templates/requirements-template.md) - EARS 格式化需求
- [设计模板](templates/design-template.md) - 综合设计结构
- [任务模板](templates/tasks-template.md) - 实现规划格式

---

## 快速开始

刚接触规格驱动开发？从这里开始：

1. **理解方法论** - 阅读 [概述](methodology/overview.md) 了解核心概念
2. **实际应用** - 查看 [简单功能规格](examples/simple-feature-spec.md) 示例
3. **亲自尝试** - 使用 [需求模板](templates/requirements-template.md) 创建您的第一个规格
4. **获得更好结果** - 应用 [提示策略](prompting/strategies.md) 进行 AI 协作

## 导航提示

- 📋 **流程章节** 提供分步说明
- 🧠 **AI 推理章节** 解释决策背后的"原因"
- 💬 **提示章节** 帮助您与 AI 有效沟通
- 📖 **示例** 展示完整的真实应用
- 📝 **模板** 为您提供即用型起始点

---

## 🔗 交叉引用与相关内容

### 按工作流阶段
- **规划阶段**：[方法论](methodology/README.md) → [需求](process/requirements-phase.md) → [设计](process/design-phase.md) → [任务](process/tasks-phase.md)
- **执行阶段**：[实现指南](execution/implementation-guide.md) → [质量保证](execution/quality-assurance.md)
- **AI 协作**：[提示策略](prompting/README.md) → [AI 推理](ai-reasoning/README.md) → [最佳实践](prompting/best-practices.md)

### 按经验水平
- **初学者**：[方法论](methodology/README.md) → [简单示例](examples/simple-feature-spec.md) → [模板](templates/README.md)
- **中级用户**：[流程指南](process/README.md) → [提示策略](prompting/README.md) → [案例研究](examples/case-studies.md)
- **高级用户**：[AI 推理](ai-reasoning/README.md) → [复杂示例](examples/complex-system-spec.md) → [决策框架](ai-reasoning/decision-frameworks.md)

### 快速问题解决
- **需求不清晰** → [需求阶段](process/requirements-phase.md) + [EARS 标准](resources/standards.md)
- **设计挑战** → [设计阶段](process/design-phase.md) + [AI 决策框架](ai-reasoning/decision-frameworks.md)
- **实现问题** → [实现指南](execution/implementation-guide.md) + [故障排除](examples/troubleshooting-pitfalls.md)
- **AI 沟通问题** → [提示最佳实践](prompting/best-practices.md) + [故障排除](examples/troubleshooting-pitfalls.md)

---

*本指南既是学习资源也是参考手册。根据您当前的需求跳转到任何章节，或按顺序阅读以获得全面理解。*

**📍 按角色、问题或学习风格的详细导航，请参见 [完整导航索引](NAVIGATION.md)**

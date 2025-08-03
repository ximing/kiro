# 流程指南

<!-- 导航元数据 -->
<!-- 章节：流程 | 等级：概述 | 前提条件：methodology/README.md -->
<!-- 相关：templates/README.md, prompting/strategies.md, examples/simple-feature-spec.md -->

**📍 您在这里：** [主指南](../../README.md) → **流程指南**

## 快速导航
- **前提条件：** [方法论概述](../methodology/README.md) - 首先理解基础
- **模板：** [即用型模板](../templates/README.md) - 快速开始
- **示例：** [查看完整规范](../examples/README.md) - 从真实示例中学习
- **AI帮助：** [提示策略](../prompting/README.md) - 与AI有效协作

---

三阶段规范驱动开发工作流程的逐步演练。

## 本节内容

- **[需求阶段](requirements-phase.md)** - 使用EARS格式收集和结构化需求
- **[设计阶段](design-phase.md)** - 通过研究创建全面的设计文档
- **[任务阶段](tasks-phase.md)** - 将设计分解为可执行的编码任务
- **[变更管理](change-management.md)** - 管理规范演进和处理发现的需求
- **[工作流程图](workflow-diagrams.md)** - 可视化流程和决策点

## 三阶段工作流程

```mermaid
stateDiagram-v2
  [*] --> Requirements : 从用户需求开始
  Requirements --> Design : 需求已批准
  Design --> Tasks : 设计已批准
  Tasks --> [*] : 准备实施

  Requirements --> Requirements : 基于反馈迭代
  Design --> Design : 完善设计
  Tasks --> Tasks : 调整任务分解
```

每个阶段都建立在前一个阶段的基础上，具有明确的批准门槛，确保在进入下一阶段之前保证质量和一致性。

## 阶段概述

1. **需求** - 将粗糙的想法转换为结构化、可测试的需求
2. **设计** - 研究并架构一个全面的解决方案
3. **任务** - 创建一个具有离散编码步骤的可执行实施计划

---

## 🔗 相关内容

### 前提条件
- [方法论概述](../methodology/README.md) - 首先理解基础

### 下一步
- [需求阶段](requirements-phase.md) - 开始三阶段流程
- [模板](../templates/README.md) - 获取即用型起始点

### 相关章节
- [示例](../examples/README.md) - 查看完整流程示例
- [提示策略](../prompting/README.md) - 获得更好的AI协作
- [执行指南](../execution/README.md) - 实施你完成的规范

[← 返回主指南](../../README.md) | [从需求开始 →](requirements-phase.md)

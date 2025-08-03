# 创建指导文档

基于项目类型和需求为开发项目创建全面的指导文档。

## 使用方法

```
Create steering documents for [项目描述]
```

## 示例

- `Create steering documents for a React TypeScript e-commerce application`
- `Create steering documents for a Python Django REST API with PostgreSQL`
- `Create steering documents for a Node.js microservices architecture`
- `Create steering documents for a Vue.js component library`

## 流程

您是创建项目指导文档的专家，这些文档为开发工作提供上下文指导。请按照以下系统化方法：

### 1. 项目分析
首先，分析项目需求并确定需要哪些指导文档：

**前端项目 (React, Vue, Angular):**
- 包含：project-standards.md, git-workflow.md, frontend-standards.md, development-environment.md
- 考虑：component-library.md, testing-strategy.md

**后端/API项目 (Node.js, Python, Java):**
- 包含：project-standards.md, git-workflow.md, api-design.md, development-environment.md
- 考虑：database-standards.md, security-guidelines.md

**全栈项目:**
- 包含：所有核心文档加上特定技术文档
- 考虑：deployment-standards.md, monitoring-guidelines.md

**库/包项目:**
- 包含：project-standards.md, git-workflow.md, documentation-standards.md
- 考虑：versioning-strategy.md, publishing-guidelines.md

### 2. 文档创建策略

使用这些模板和指导方针创建指导文档：

#### 核心文档（始终创建）

**project-standards.md** - #[[file:.kiro/steering/project-standards.md]]
- 根据项目语言/框架调整代码质量标准
- 基于项目复杂度定制测试要求
- 包含项目特定的文档需求
- 设置与领域相关的安全实践

**git-workflow.md** - #[[file:.kiro/steering/git-workflow.md]]
- 根据团队规模和发布策略调整分支命名
- 根据项目需求定制提交信息格式
- 设置适当的审查要求
- 定义合并策略

#### 条件性文档（基于项目类型创建）

**frontend-standards.md** - #[[file:.kiro/steering/frontend-standards.md]]
```yaml
---
inclusion: fileMatch
fileMatchPattern: '*.tsx|*.jsx|*.vue|*.svelte|*.ts|*.js'
---
```
- 针对特定框架（React/Vue/Angular）定制
- 包含设计系统和样式方法
- 设置无障碍访问要求
- 定义性能标准

**api-design.md** - #[[file:.kiro/steering/api-design.md]]
```yaml
---
inclusion: fileMatch
fileMatchPattern: '*api*|*route*|*controller*|*endpoint*'
---
```
- 根据项目需求调整REST/GraphQL标准
- 包含身份认证/授权模式
- 设置错误处理约定
- 定义API版本控制策略

**development-environment.md** - #[[file:.kiro/steering/development-environment.md]]
```yaml
---
inclusion: fileMatch
fileMatchPattern: 'package.json|requirements.txt|Dockerfile|docker-compose.yml|Makefile'
---
```
- 针对项目的技术栈进行定制
- 包含特定工具要求
- 设置环境变量模式
- 定义构建和部署流程

### 3. 内容定制指导方针

**语言/框架特定适配:**
- **JavaScript/TypeScript**: ESLint, Prettier, Jest, package.json脚本
- **Python**: Black, flake8, pytest, requirements.txt, 虚拟环境
- **Java**: Checkstyle, Maven/Gradle, JUnit, Spring Boot约定
- **Go**: gofmt, go mod, 测试模式, 项目结构
- **Rust**: rustfmt, Cargo.toml, cargo test, clippy

**项目规模适配:**
- **小型项目**: 轻量级流程，最小工具集
- **团队项目**: 代码审查要求，共享标准
- **企业级**: 全面安全，合规性，文档

**领域特定考虑:**
- **电子商务**: PCI合规，性能，安全性
- **医疗保健**: HIPAA合规，数据隐私，审计跟踪
- **金融**: 安全标准，监管合规
- **开源**: 贡献指导方针，许可证，社区标准

### 4. 文件引用集成

使用 `#[[file:path]]` 语法包含相关外部文件：
- API项目的OpenAPI规范
- 后端项目的数据库模式
- 前端项目的设计系统令牌
- 环境设置的配置文件

### 5. 质量检查清单

在完成指导文档前，确保：
- [ ] 所有文档都具有适当的包含逻辑前置元数据
- [ ] 指导方针具体且可操作，而非泛泛而谈
- [ ] 为复杂概念提供示例
- [ ] 文档间无冲突标准
- [ ] 包含安全和性能考虑
- [ ] 文档覆盖完整开发生命周期
- [ ] 文件引用格式正确且有效

## 参考资料

使用这些全面指南创建指导文档：

**创建指南:** #[[file:.kiro/steering/steering-creation-guide.md]]

**模板示例:**
- #[[file:.kiro/steering/project-standards.md]]
- #[[file:.kiro/steering/git-workflow.md]]
- #[[file:.kiro/steering/frontend-standards.md]]
- #[[file:.kiro/steering/api-design.md]]
- #[[file:.kiro/steering/development-environment.md]]

## 输出格式

在 `.kiro/steering/` 目录中创建完整的指导文档集，包含：
1. 适当的包含逻辑前置元数据
2. 项目特定的内容和示例
3. 清晰、可操作的指导方针
4. 适当的文件引用（如适用）
5. 一致的格式和结构

指导文档应该立即改善开发一致性，并为特定项目需求提供上下文指导。

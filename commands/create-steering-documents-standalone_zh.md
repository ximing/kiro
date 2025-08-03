# 创建指导文档 - 独立版本

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

**project-standards.md 模板:**
```markdown
# 项目标准和指导方针

## 代码质量标准
- 遵循语言特定的风格指南（JS/TS使用ESLint，Python使用Black等）
- 在代码库中保持一致的命名约定
- 编写自文档化代码，使用清晰的变量和函数名
- 为复杂业务逻辑包含有意义的注释
- 保持函数小而专注于单一职责

## 测试要求
- 为所有业务逻辑函数编写单元测试
- 保持至少80%的代码覆盖率
- 为API端点包含集成测试
- 为关键用户流程编写端到端测试
- 使用描述性测试名称解释正在测试的场景

## 文档标准
- 为任何重大更改更新README.md
- 用清晰示例记录API端点
- 包含设置和部署说明
- 为版本发布维护变更日志
- 以ADR格式记录架构决策

## 安全实践
- 永远不要提交密钥、API密钥或密码
- 使用环境变量进行配置
- 验证所有用户输入
- 实施适当的身份认证和授权
- 遵循OWASP安全指导方针

## 性能指导方针
- 优化数据库查询并避免N+1问题
- 在适当的地方实施缓存
- 对大数据集使用懒加载
- 定期监控和分析性能
- 在架构决策中考虑可扩展性
```

**git-workflow.md 模板:**
```markdown
# Git工作流和分支策略

## 分支命名约定
- 功能分支：`feature/description-of-feature`
- 错误修复：`fix/description-of-bug`
- 热修复：`hotfix/critical-issue-description`
- 发布：`release/version-number`

## 提交信息格式
遵循约定式提交格式：
```
type(scope): description

[optional body]

[optional footer]
```

类型：feat, fix, docs, style, refactor, test, chore

## 拉取请求指导方针
- 从功能分支到main/develop创建PR
- 包含清晰的更改描述
- 使用关键字链接相关问题（fixes #123）
- 在请求审查前确保所有测试通过
- 合并时压缩提交以保持历史清洁

## 代码审查流程
- 合并前至少需要一个批准
- 审查代码质量、安全性和性能
- 检查测试是否覆盖新功能
- 验证必要时文档已更新
- 确保没有破坏性更改而没有适当版本控制
```

#### 条件性文档（基于项目类型创建）

**frontend-standards.md 模板:**
```markdown
---
inclusion: fileMatch
fileMatchPattern: '*.tsx|*.jsx|*.vue|*.svelte'
---

# 前端开发标准

## 组件架构
- 使用带钩子的函数式组件（React）
- 保持组件小而专注
- 实施适当的属性验证
- 使用TypeScript进行类型安全
- 遵循组件组合模式

## 状态管理
- 为组件特定数据使用本地状态
- 为共享应用数据实施全局状态
- 使用适当的状态管理库（Redux、Zustand、Pinia）
- 通过上下文或状态管理避免属性钻取

## 样式指导方针
- 使用CSS模块或styled-components进行组件样式
- 为CSS类命名遵循BEM方法论
- 用移动优先方法实施响应式设计
- 使用CSS自定义属性进行主题化
- 维护一致的间距和排版比例

## 性能优化
- 实施代码分割和懒加载
- 为昂贵组件使用React.memo或类似技术
- 优化图像和资源
- 实施适当的缓存策略
- 监控包大小和性能指标

## 无障碍访问标准
- 使用语义HTML元素
- 实施适当的ARIA属性
- 确保键盘导航支持
- 维护适当的颜色对比度
- 用屏幕阅读器测试

## 测试策略
- 为工具函数编写单元测试
- 使用React Testing Library进行组件测试
- 实施视觉回归测试
- 测试用户交互和工作流
- 适当地模拟外部依赖
```

**api-design.md 模板:**
```markdown
---
inclusion: manual
---

# API设计指导方针

## RESTful API标准
- 适当使用HTTP方法（GET、POST、PUT、DELETE、PATCH）
- 遵循基于资源的URL模式：`/api/v1/users/{id}`
- 为资源集合使用复数名词
- 实施适当的HTTP状态代码
- 在URL路径中包含API版本控制

## 请求/响应格式
- 为请求和响应体使用JSON
- 遵循一致的命名约定（camelCase或snake_case）
- 为列表端点包含分页
- 实施适当的错误响应格式：
```json
{
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid input provided",
    "details": ["Email is required", "Password too short"]
  }
}
```

## 身份认证和授权
- 为无状态身份认证使用JWT令牌
- 实施适当的令牌刷新机制
- 使用基于角色的访问控制（RBAC）
- 对API端点进行速率限制以防止滥用

## 文档
- 使用OpenAPI/Swagger进行API文档
- 包含请求/响应示例
- 记录所有可能的错误响应
- 提供SDK或客户端库示例

#[[file:openapi.yml]]
```

**development-environment.md 模板:**
```markdown
---
inclusion: fileMatch
fileMatchPattern: 'package.json|requirements.txt|Dockerfile|docker-compose.yml'
---

# 开发环境设置

## 本地开发
- 使用.nvmrc文件中指定的Node.js版本
- 使用`npm ci`安装依赖以获得一致的构建
- 为本地数据库和服务依赖使用Docker
- 在提交更改前运行代码检查和格式化

## 环境变量
- 复制`.env.example`到`.env`进行本地开发
- 永远不要提交实际的环境文件
- 在README中记录所有必需的环境变量
- 为不同环境使用不同前缀（DEV_、PROD_等）

## 数据库管理
- 为所有模式更改使用迁移
- 为迁移包含回滚脚本
- 种子数据应该是幂等的
- 在重大更改前备份数据库

## 构建和部署
- 确保构建在各环境间可重现
- 使用多阶段Docker构建进行优化
- 在容器化应用程序中包含健康检查
- 记录部署程序和回滚步骤

## 调试和日志记录
- 使用适当日志级别的结构化日志
- 为请求跟踪包含关联ID
- 设置适当的错误监控和警报
- 在开发中使用调试器而不是console.log
```

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

## 指导文档创建和使用指南

### 什么是指导文档？

指导文档是影响AI助手处理开发任务方式的上下文指导方针。它们包含项目特定的标准、约定和最佳实践，有助于提供更相关和一致的协助。

### 指导文档的工作原理

#### 包含机制
1. **始终包含（默认）**：没有前置元数据的文档在每次交互中都会包含
2. **文件匹配条件**：带有`inclusion: fileMatch`和`fileMatchPattern`的文档在特定文件在上下文中时包含
3. **手动包含**：带有`inclusion: manual`的文档仅在使用`#steering-name`显式引用时包含

#### 上下文集成
- 指导内容在处理用户请求前被注入到AI的系统上下文中
- AI接收适用指导文档的完整内容
- 多个指导文档可以同时激活
- 使用`#[[file:path]]`语法的文件引用会被解析和包含

### 指导文档应包含什么

#### 需要创建的核心类别：

1. **开发环境标准**
   - 本地设置程序
   - 工具配置
   - 环境变量管理
   - 构建和部署流程

2. **代码质量指导方针**
   - 语言特定风格指南
   - 命名约定
   - 代码组织模式
   - 文档要求

3. **Git工作流标准**
   - 分支命名约定
   - 提交信息格式
   - 拉取请求流程
   - 代码审查指导方针

4. **技术特定标准**
   - 前端开发模式
   - 后端API设计
   - 数据库管理
   - 测试策略

5. **安全和性能**
   - 安全最佳实践
   - 性能优化指导方针
   - 监控和警报标准

#### 应遵循的内容结构：

```markdown
---
inclusion: [always|fileMatch|manual]
fileMatchPattern: 'pattern' # 如果是fileMatch
---

# 清晰标题

## 有组织的章节
- 具体、可操作的指导方针
- 相关的代码示例
- 工具配置
- 使用#[[file:path]]引用外部文件

## 实施细节
- 逐步程序
- 要避免的常见陷阱
- 质量检查点
```

### 如何构建指导文档

#### 评估流程：
1. **项目分析**：检查代码库结构、使用的技术和现有模式
2. **差距识别**：识别标准可以改善一致性的领域
3. **优先级排序**：首先关注高影响领域（安全、代码质量、工作流）
4. **模板选择**：基于项目类型选择适当模板

#### 内容开发：
1. **研究最佳实践**：从行业标准和经过验证的模式中汲取
2. **为项目定制**：将通用实践适配到特定项目需求
3. **包含示例**：提供具体的代码示例和配置
4. **引用集成**：链接到现有项目文件和规范

#### 质量保证：
1. **完整性检查**：确保涵盖所有关键领域
2. **一致性验证**：验证指导方针不会相互冲突
3. **实用性评估**：确认指导方针可操作且现实
4. **更新机制**：规划随项目发展维护文档

### 包含策略和上下文传输

#### 发送的内容：
- **完整内容**：传输完整的指导文档内容
- **解析引用**：使用`#[[file:path]]`引用的文件会被读取和包含
- **多个文档**：所有适用的指导文档会被组合
- **实时评估**：每次交互都会评估包含规则

#### 何时包含文档：
- **始终**：没有前置元数据的文档的默认行为
- **文件上下文触发器**：当特定文件模式在对话上下文中时
- **手动触发器**：当用户使用`#steering-name`显式引用时
- **自动解析**：系统基于文件模式确定相关性

#### 上下文限制：
- 如果大型指导文档超过上下文限制可能会被截断
- 更具体/相关的指导文档会被优先考虑
- 最近的交互可能影响优先考虑哪些文档

### 指导创建的最佳实践

#### 应该：
- 保持文档专注且具体
- 使用清晰、可操作的语言
- 包含具体示例
- 引用外部规范
- 随项目发展定期更新
- 使用适当的包含机制

#### 不应该：
- 创建过于宽泛或通用的指导方针
- 在多个文档间重复信息
- 包含敏感信息或密钥
- 创建冲突标准
- 使文档过长或复杂

### 维护和演进

#### 定期审查：
- 评估现有指导文档的有效性
- 基于项目变化和学习进行更新
- 移除过时或冲突的指导方针
- 随项目增长添加新标准

#### 反馈集成：
- 监控指导文档对代码质量的影响
- 基于团队反馈和开发模式进行调整
- 为更好相关性优化包含模式
- 优化文档结构以提高清晰度

### 技术实施注意事项

#### 文件结构：
```
.kiro/steering/
├── project-standards.md (始终包含)
├── git-workflow.md (始终包含)
├── frontend-standards.md (fileMatch: *.tsx,*.jsx)
├── api-design.md (手动包含)
└── development-environment.md (fileMatch: package.json)
```

#### 前置元数据选项：
```yaml
---
inclusion: always|fileMatch|manual
fileMatchPattern: 'glob-pattern' # 仅用于fileMatch
---
```

#### 文件引用语法：
```markdown
#[[file:relative/path/to/file.ext]]
```

## 输出格式

在 `.kiro/steering/` 目录中创建完整的指导文档集，包含：
1. 适当的包含逻辑前置元数据
2. 项目特定的内容和示例
3. 清晰、可操作的指导方针
4. 适当的文件引用（如适用）
5. 一致的格式和结构

指导文档应该立即改善开发一致性，并为特定项目需求提供上下文指导。

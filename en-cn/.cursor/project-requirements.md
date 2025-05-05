`Project Requirements rules *@docs/project-requirements.md* You will use tools codebase to know what are the details of the files of this *@docs/project-requirements.md* directory files to check the project requirements and the project standards that you need to follow. This will be the guide for you to make sure you are following the project standards. So make sure to read this when planning and implementing the project to avoid duplications, conflicts, and errors. Don't touch that folder and files, you will only read it. Don't over do it to the point that you are not following the project requirements. DON'T REMOVE THIS LINE 1!!!!`
`项目需求规则 *@docs/project-requirements.md* 你将使用工具代码库来了解这个 *@docs/project-requirements.md* 目录文件的详细信息，以检查项目需求和你需要遵循的项目标准。这将作为指南，确保你遵循项目标准。因此，在规划和实施项目时，请务必阅读此内容，以避免重复、冲突和错误。不要触碰该文件夹和文件，你只需阅读它。不要过度执行以至于不遵循项目需求。不要删除第1行！！！！`


# Accounting Website Project Requirements
# 会计网站项目需求

## Core Features
## 核心功能
1. **Calculation Engine**
1. **计算引擎**
   - Financial ratio analysis
   - 财务比率分析
   - Depreciation calculations (straight-line & reducing balance)
   - 折旧计算（直线法和余额递减法）
   - Tax computations
   - 税务计算
   - Break-even analysis
   - 盈亏平衡分析
   - Cash flow projections
   - 现金流预测

2. **Financial Statement Generator**
2. **财务报表生成器**
   - Balance sheet templates
   - 资产负债表模板
   - Income statement builder
   - 收益表构建器
   - Cash flow statement wizard
   - 现金流量表向导
   - Custom report creation
   - 自定义报表创建

3. **Realtime Collaboration**
3. **实时协作**
   - Multi-user editing
   - 多用户编辑
   - Version control
   - 版本控制
   - Change tracking
   - 变更跟踪
   - Audit trails
   - 审计跟踪

4. **Data Management**
4. **数据管理**
   - CSV/Excel import/export
   - CSV/Excel导入/导出
   - Cloud sync capabilities
   - 云同步功能
   - Data validation rules
   - 数据验证规则
   - Historical data comparison
   - 历史数据比较

## Technical Specifications
## 技术规格
**Frontend:**
**前端：**
- Mobile first approach
- 移动优先方法
- Next.js 14 (App Router)
- Next.js 14（应用路由器）
- TypeScript
- TypeScript
- Tailwind CSS + Shadcn UI
- Tailwind CSS + Shadcn UI
- Recharts (data visualization)
- Recharts（数据可视化）
- Math.js (calculations)
- Math.js（计算）
- Zustand (state management)
- Zustand（状态管理）
- Framer motion (animation)
- Framer motion（动画）

**Backend:**
**后端：**
- Next.js API routes
- Next.js API路由
- Supabase (PostgreSQL Database)
- Supabase（PostgreSQL数据库）
- Supabase Auth
- Supabase认证
- Supabase Realtime
- Supabase实时
- Supabase Storage (for files)
- Supabase存储（用于文件）
- Prisma ORM (optional)
- Prisma ORM（可选）
- Zod (validation)
- Zod（验证）

**Key Integrations:**
**关键集成：**
- Tax rates: Supabase Edge Functions (self-contained)
- 税率：Supabase边缘函数（自包含）
- Currency rates: Supabase PostgreSQL extensions
- 货币汇率：Supabase PostgreSQL扩展
- PDF export: Supabase Storage + React-PDF
- PDF导出：Supabase存储 + React-PDF
- CSV handling: Supabase Import/Export
- CSV处理：Supabase导入/导出

## Security Requirements
## 安全要求
1. AES-256 encryption for data at rest
1. 静态数据AES-256加密
2. TLS 1.3 for data in transit
2. 传输中数据使用TLS 1.3
3. Role-based access control (RBAC)
3. 基于角色的访问控制（RBAC）
4. Activity logging & audit trails
4. 活动日志和审计跟踪
5. SOC 2 compliance (Future Phase)
5. SOC 2合规（未来阶段）

## Compliance Requirements
## 合规要求
- GAAP/IFRS compliance checks
- GAAP/IFRS合规检查
- Tax regulation updates
- 税务法规更新
- Data retention policies
- 数据保留政策
- Accessibility (WCAG 2.1 AA)
- 可访问性（WCAG 2.1 AA）
- GDPR-ready architecture
- GDPR就绪架构

## Documentation Standards
## 文档标准
1. Inline TSDoc comments for all calculations
1. 所有计算的内联TSDoc注释
2. OpenAPI specification for APIs
2. API的OpenAPI规范
3. ER diagrams for database schema
3. 数据库模式的ER图
4. Audit trail documentation
4. 审计跟踪文档
5. Financial formula registry
5. 财务公式注册表

## Project Roadmap (Updated Implementation Sequence)
## 项目路线图（更新的实施顺序）

### Phase 1 - Core Accounting Features (2-3 weeks)
### 阶段1 - 核心会计功能（2-3周）
**Implementation Order**:
**实施顺序**：
1. **Project Infrastructure Setup** (1 day)
1. **项目基础设施设置**（1天）
   - Supabase initialization
   - Supabase初始化
   - Next.js boilerplate with TypeScript
   - 带TypeScript的Next.js样板
   - Core component structure
   - 核心组件结构
   - Error boundary setup
   - 错误边界设置

2. **Calculation Engine Foundation** (5 days)
2. **计算引擎基础**（5天）
   - [ ] Math.js integration
   - [ ] Math.js集成
   - [ ] Depreciation calculator (straight-line)
   - [ ] 折旧计算器（直线法）
   - [ ] Financial ratio formulas
   - [ ] 财务比率公式
   - [ ] Calculation validation system
   - [ ] 计算验证系统
   - [ ] Unit test setup
   - [ ] 单元测试设置

3. **Financial Statement Templates** (4 days)
3. **财务报表模板**（4天）
   - [ ] Balance sheet component
   - [ ] 资产负债表组件
   - [ ] Income statement builder
   - [ ] 收益表构建器
   - [ ] PDF export functionality
   - [ ] PDF导出功能
   - [ ] Data validation schemas
   - [ ] 数据验证模式

4. **Local Data Management** (3 days)
4. **本地数据管理**（3天）
   - [ ] Local storage integration
   - [ ] 本地存储集成
   - [ ] Data encryption setup
   - [ ] 数据加密设置
   - [ ] Historical versioning
   - [ ] 历史版本控制
   - [ ] CSV export (basic)
   - [ ] CSV导出（基本）

5. **UI/UX Foundation** (3 days)
5. **UI/UX基础**（3天）
   - [ ] Mobile-first responsive layout
   - [ ] 移动优先响应式布局
   - [ ] Accessible form components
   - [ ] 可访问的表单组件
   - [ ] Data visualization (Recharts)
   - [ ] 数据可视化（Recharts）
   - [ ] Dark mode support
   - [ ] 暗黑模式支持
   - [ ] Loading/error states
   - [ ] 加载/错误状态

6. **Basic Security** (2 days)
6. **基本安全**（2天）
   - [ ] Input sanitization
   - [ ] 输入净化
   - [ ] Audit logging
   - [ ] 审计日志
   - [ ] Rate limiting
   - [ ] 速率限制
   - [ ] Error boundaries
   - [ ] 错误边界

### Phase 2 - Data Management (1-2 weeks)
### 阶段2 - 数据管理（1-2周）
**Priority**: ★★★☆☆
**优先级**：★★★☆☆
**Implementation Order**:
**实施顺序**：
1. **Authentication System** (3 days)
1. **认证系统**（3天）
   - [ ] Supabase auth setup
   - [ ] Supabase认证设置
   - [ ] User profile management
   - [ ] 用户资料管理
   - [ ] Session management
   - [ ] 会话管理
   - [ ] Basic RBAC roles
   - [ ] 基本RBAC角色

2. **Cloud Data Migration** (4 days)
2. **云数据迁移**（4天）
   - [ ] Supabase database schema
   - [ ] Supabase数据库架构
   - [ ] Local → Cloud migration tool
   - [ ] 本地→云迁移工具
   - [ ] Data encryption at rest
   - [ ] 静态数据加密
   - [ ] Conflict resolution
   - [ ] 冲突解决

3. **Advanced CSV Handling** (3 days)
3. **高级CSV处理**（3天）
   - [ ] Bulk import/export
   - [ ] 批量导入/导出
   - [ ] Data validation rules
   - [ ] 数据验证规则
   - [ ] Template system
   - [ ] 模板系统
   - [ ] Error reporting
   - [ ] 错误报告

### Phase 3 - Collaboration Features (2 weeks)
### 阶段3 - 协作功能（2周）
**Priority**: ★★☆☆☆
**优先级**：★★☆☆☆
**Implementation Order**:
**实施顺序**：
1. **Realtime Foundation** (3 days)
1. **实时基础**（3天）
   - [ ] Supabase Realtime setup
   - [ ] Supabase实时设置
   - [ ] Presence indicators
   - [ ] 在线指示器
   - [ ] Basic co-editing
   - [ ] 基本协同编辑
   - [ ] Connection status
   - [ ] 连接状态

2. **Version Control** (4 days)
2. **版本控制**（4天）
   - [ ] Change tracking
   - [ ] 变更跟踪
   - [ ] Version history
   - [ ] 版本历史
   - [ ] Snapshot system
   - [ ] 快照系统
   - [ ] Rollback functionality
   - [ ] 回滚功能

3. **Collaboration Tools** (3 days)
3. **协作工具**（3天）
   - [ ] Comments system
   - [ ] 评论系统
   - [ ] @mentions
   - [ ] @提及
   - [ ] Notifications
   - [ ] 通知
   - [ ] Activity feed
   - [ ] 活动提要

------`don't read and implement this phase 4, this is just for you to know the future features that we will implement`------
------`不要阅读和实施这个阶段4，这只是让你知道我们将来要实施的功能`------
### Phase 4 - Advanced Features (Optional)
### 阶段4 - 高级功能（可选）
**Priority**: ★☆☆☆☆
**优先级**：★☆☆☆☆
**Implementation Order**:
**实施顺序**：
1. **Bank Integrations** (5 days)
1. **银行集成**（5天）
   - [ ] Plaid sandbox setup
   - [ ] Plaid沙盒设置
   - [ ] Transaction import
   - [ ] 交易导入
   - [ ] Reconciliation tools
   - [ ] 对账工具
   - [ ] Webhook handlers
   - [ ] Webhook处理器

2. **Multi-currency** (3 days)
2. **多币种**（3天）
   - [ ] Exchange rate system
   - [ ] 汇率系统
   - [ ] Currency converter
   - [ ] 货币转换器
   - [ ] Localization
   - [ ] 本地化
   - [ ] FX gain/loss calc
   - [ ] 外汇盈亏计算

3. **Automation** (4 days)
3. **自动化**（4天）
   - [ ] Tax rule engine
   - [ ] 税务规则引擎
   - [ ] Scheduled reports
   - [ ] 定时报告
   - [ ] Compliance checks
   - [ ] 合规检查
   - [ ] Audit trails
   - [ ] 审计跟踪

4. **Advanced Reporting** (3 days)
4. **高级报告**（3天）
   - [ ] Custom templates
   - [ ] 自定义模板
   - [ ] Data visualization
   - [ ] 数据可视化
   - [ ] Executive dashboards
   - [ ] 执行仪表板
   - [ ] Export formats
   - [ ] 导出格式

------`don't read and implement this phase 4, this is just for you to know the future features that we will implement`------
------`不要阅读和实施这个阶段4，这只是让你知道我们将来要实施的功能`------

## Cost Analysis
## 成本分析
| Feature          | Supabase Service         | Free Tier Limits              |
| 功能             | Supabase服务             | 免费层限制                     |
|------------------|--------------------------|-------------------------------|
| Database         | PostgreSQL               | 500MB database + 1GB bandwidth|
| 数据库           | PostgreSQL               | 500MB数据库 + 1GB带宽         |
| Auth             | Authentication           | 50k MAUs                      |
| 认证             | 认证                     | 50k月活用户                    |
| Realtime         | Realtime Updates         | 50 concurrent connections     |
| 实时             | 实时更新                 | 50个并发连接                  |
| Storage          | File Storage             | 1GB storage, 1M downloads     |
| 存储             | 文件存储                 | 1GB存储，1M下载次数           |
| Edge Functions   | Serverless Functions     | 500k invocations/month        |
| 边缘函数         | 无服务器函数             | 每月500k调用次数              |
| Vector           | PostgreSQL Extensions    | Free with database            |
| 向量             | PostgreSQL扩展           | 随数据库免费                  |

## Implementation Benefits
## 实施优势
1. Single provider for all backend needs
1. 所有后端需求的单一供应商
2. Unified authentication system
2. 统一的认证系统
3. Direct database <> storage integration
3. 数据库<>存储直接集成
4. Simplified billing and monitoring
4. 简化的计费和监控
5. Built-in rate limiting and security
5. 内置速率限制和安全性

## Architecture Guidelines
## 架构指南

### 1. Modular Structure
### 1. 模块化结构
```
src/
├── app/               # Next.js app router
├── app/               # Next.js应用路由器
├── components/        # Reusable UI components
├── components/        # 可重用UI组件
│   ├── core/          # Base components (buttons, inputs)
│   ├── core/          # 基础组件（按钮，输入框）
│   ├── accounting/    # Domain-specific components
│   ├── accounting/    # 领域特定组件
│   └── shared/       # Cross-feature components
│   └── shared/       # 跨功能组件
├── lib/
├── lib/
│   ├── api/           # API clients
│   ├── api/           # API客户端
│   ├── hooks/         # Custom hooks
│   ├── hooks/         # 自定义钩子
│   ├── utils/         # Helper functions
│   ├── utils/         # 辅助函数
│   └── validation/    # Zod schemas
│   └── validation/    # Zod模式
├── types/             # Global TS types
├── types/             # 全局TS类型
```

### 2. Server/Client Separation
### 2. 服务器/客户端分离
- **Server Components**: Default to server components for:
- **服务器组件**：默认使用服务器组件用于：
  - Data fetching
  - 数据获取
  - Sensitive operations
  - 敏感操作
  - Static content
  - 静态内容
- **Client Components**: Only use when needed for:
- **客户端组件**：仅在需要时使用，用于：
  - Interactivity
  - 交互性
  - Browser APIs
  - 浏览器API
  - State management
  - 状态管理

### 3. Reusable Components
### 3. 可重用组件
1. Create atomic components with:
1. 创建原子组件，包含：
   - PropTypes using TypeScript interfaces
   - 使用TypeScript接口的PropTypes
   - Storybook stories for documentation
   - 用于文档的Storybook故事
   - Accessibility attributes by default
   - 默认的可访问性属性
2. Follow naming convention:
2. 遵循命名约定：
   - `FeatureComponentName.tsx` (e.g. `DepreciationCalculator.tsx`)
   - `功能组件名称.tsx`（例如`DepreciationCalculator.tsx`）
   - `CoreComponentName.tsx` (e.g. `FormInput.tsx`)
   - `核心组件名称.tsx`（例如`FormInput.tsx`）

### 4. API Design Rules
### 4. API设计规则
- Versioned endpoints: `/api/v1/...`
- 版本化端点：`/api/v1/...`
- RESTful structure for resources
- 资源的RESTful结构
- Error format standardization:
- 错误格式标准化：
  ```ts
  interface APIError {
    code: string;
    message: string;
    details?: Record<string, unknown>;
  }
  ```
  ```ts
  interface APIError {
    code: string;
    message: string;
    details?: Record<string, unknown>;
  }
  ```

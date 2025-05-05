# 🎯 AI 上下文规则系统（Vibe Coding多智能体协作规则系统 v1.2）

## 🌟 概览
一个全面的系统，通过记忆管理、经验教训跟踪和双模式操作（规划Plan/执行Act）来管理 AI 交互。该系统确保一致、高质量的开发，同时维护详细的项目文档和知识保留。

## 🔄 核心组件
1. **记忆系统(Memory System)** (`@memories.md`)
   - 包含带日期的分类条目（例如，"项目初始化（2024-03-15）"）
   - 记录一行带有完整上下文的描述
   - 使用清晰的版本编号格式 [x.x.x] 标记每个条目
   - 根据开发里程碑的时间顺序进行记录
   - 超过1000行时，创建新的记忆文件，例如 @memories2.md，所有的记忆体文件互相交叉引用
   - 记录完整的交互上下文、变更和技术细节
   - 历史条目永不删除以保存项目历史

2. **经验教训(Lessons Learned)** (`@lessons-learned.md`)
   - 记录解决方案和最佳实践
   - 结构化格式：问题 → 解决方案 → 影响
   - 按组件、技术语言、功能模块、错误等进行分类
   - 按优先级（关键/重要/增强）排序问题
   - 记录相关代码示例

3. **草稿本(Scratchpad)** (`@scratchpad.md`)
   - 管理当前阶段和任务
   - 跟踪实施进度
   - 使用清晰的状态标记 [X]、[-]、[ ]、[!]、[?]
   - 维护任务依赖关系
   - 更新置信度指标（confidence metrics）

## 🎯 模式化系统操作(Mode System Operation)

### 规划模式(Plan Mode) 🎯
```markdown
触发器："/plan"
目的：信息收集和规划
要求：
- 解析用户输入
- 需求交叉参考
- 生成澄清问题
- 计算置信度分数
- 分解任务
```

### 执行模式(Agent/Act Mode) ⚡
```markdown
触发器："/agent" 或 "/act"
激活依赖：
- 95% 置信度水平
- 所有问题已回答
- 任务已定义
- 无阻塞问题
- 需求已验证
```

## 🚀 工作流程步骤(Workflow Steps)

1. **初始化规划(Initialize Planning)** 🎯
   ```markdown
   - 使用"/plan"触发器
   - 系统创建新的草稿本条目
   - 生成至少3个问题
   - 设置初始置信度分数
   ```

2. **构建置信(Build Confidence)** 📈
   ```markdown
   - 回答所有问题
   - 验证需求
   - 更新任务依赖关系
   - 监控置信度分数
   ```

3. **执行实施(Execute Implementation)** ⚡
   ```markdown
   - 达到95%置信度
   - 使用"/agent" 或 "/act" 触发器
   - 实施解决方案
   - 更新文档
   ```

## 🎮 工作流程示例(Workflow Examples)

### 示例1：创建新功能
```markdown
用户："/plan 追加一个按钮组件"

AI：🎯 规划模式已激活
当前任务：实现新按钮组件
问题：
1. 需要哪些样式类型？（primary/secondary/outline）
2. 是否应支持图标？
3. 需要哪些尺寸？
置信度：65%

用户："primary 和 secondary 样式类型, 支持图标, 三种尺寸"

AI：更新理解：
- Primary/Secondary 样式类型
- 支持图标
- 小/中/大 三种尺寸
置信度：95%

用户："/agent"
(或者"/act")

AI：⚡ 执行模式已激活
- 创建按钮组件
- 实现样式类型
- 添加图标支持
- 测试可访问性
```

### 示例2：修复错误
```markdown
用户："/plan 修复一个表单提交错误"

AI：🎯 规划模式已激活
当前任务：调试表单提交错误
问题：
1. 错误何时发生？
2. 控制台有错误信息吗？
3. 哪个表单组件受影响？
置信度：50%

用户："用户登录表单时，控制台输出校验错误"

AI：思维链分析：
1. 登录表单验证
2. 控制台错误检查
3. 输入验证规则
置信度：95%

用户："/act"
(或者"/agent")

AI：⚡ 执行模式已激活
- 调试验证
- 修复错误处理
- 测试提交
```

### 示例3：项目设置
```markdown
用户："/plan 创建一个 Next.js 新项目"

AI：🎯 规划模式已激活
当前任务：初始化Next.js项目
问题：
1. 使用哪个版本的Next.js？
2. TypeScript还是JavaScript？
3. 需要哪些UI组件？
置信度：70%

用户："Next.js 14, TypeScript, Shadcn UI"

AI：项目结构：
- Next.js 14设置
- TypeScript配置
- Shadcn UI集成
置信度：95%

用户："/act"
(或者"/agent")

AI：⚡ 执行模式已激活
- 创建项目
- 设置TypeScript
- 设置Shadcn UI
- 安装依赖
```

### 示例4：文档更新
```markdown
用户："/plan 更新API文档"

AI：🎯 规划模式已激活
问题：
1. 哪些接口需要更新？
2. 是否添加了新参数？
3. 响应格式有变化吗？
置信度：60%

用户："新的认证接口"

AI：文档计划：
- 认证接口
- 请求/响应格式
- 使用示例
置信度：95%

用户："/agent"
(或者"/act")

AI：⚡ 执行模式已激活
- 更新文档
- 添加示例
- 验证格式
```

## 📝 文档标准(Documentation Standards)

### 实时更新(Real-time Updates)
- 记忆(Memories)：每次交互
- 经验教训(Lessons)：解决方案后
- 草稿本(Scratchpad)：实施期间

### 版本控制(Version Control)
```markdown
记忆条目格式：
- [x.x.x] 带日期的类别：带完整上下文的综合描述
- 示例：[1.0.0] 项目设置（2024年3月15日）：成功初始化了一个新的Next.js 14项目...

跨文件管理：
- 超过1000行时创建新的记忆文件，例如 @memories2.md
- 维护记忆文件之间的交叉引用
- 永不删除记忆的历史条目
```

### 交叉引用(Cross-referencing)
```markdown
@memories.md ↔️ @lessons-learned.md ↔️ @scratchpad.md
```

## 🔍 目录结构(Directory Structure)
```
.cursor/
├── memories.md          # 交互历史（记忆文件）
├── lessons-learned.md   # 解决方案和实践（经验教训文件）
├── scratchpad.md       # 当前阶段跟踪（草稿本文件）
├── project-requirements.md  # 项目规格（项目需求文件）
└── rules/              # 系统规则
    └── .cursorrules    # 核心规则文件
```

## 🛠️ 最佳实践

1. **记忆管理(Memory Management)**
   - 创建带有清晰日期的分类条目
   - 编写全面的单行描述
   - 使用一致的版本编号[x.x.x]
   - 包含完整的技术实施细节
   - 记录所有开发决策和结果
   - 维护项目里程碑的时间顺序
   - 超过1000行时创建新的记忆文件，例如 @memories2.md
   - 永不删除记忆的历史条目

2. **任务跟踪(Task Tracking)**
   - 生成唯一的任务ID
   - 跟踪依赖关系
   - 实时更新状态
   - 维护层次结构

3. **文档(Documentation)**
   - 实时更新
   - 包含版本号
   - 交叉引用相关文件
   - 遵循结构化格式

## 🎯 提示和技巧

### 🔄 AI和Cursor问题
1. **必需的打开标签**：
   ```
   1️⃣ 活动工作文件(Active working file，不清楚实际作用)
   2️⃣ Cursor设置（Feature → Resync index）
   3️⃣ .cursorrules（用于自动重新加载，新版Cursor中使用项目级别规则适配来对应）
   ```

2. **快速重新加载过程**：
   ```
   1. Ctrl+Shift+P 或者 Mac下 Command+Shift+P
   2. "Developer: Reload Window"
   3. 等待3-10秒
   ```

### 💡 专业提示
- 保持.cursorrules文件打开（新版Cursor中使用项目级别规则适配来对应，不再需要）
- 监控置信度分数
- 使用正确的触发器
- 遵循记忆条目格式：[x.x.x] 类别（日期）：全面描述
- 按开发里程碑对记忆条目进行分类
- 在记忆描述中包含完整的技术细节
- 交叉引用

## 🤝 Contributing
Feel free to enhance this system:
1. Add custom rules
2. Improve tracking
3. Enhance metrics
4. Share practices

## 📝 License
MIT License - Free to use and modify!

## 👋 Contacts / Hire me
- Instagram: https://www.instagram.com/clover_nat/
- Facebook: https://www.facebook.com/nathanielmarquez.20
- Twitter: https://x.com/T1nker1220

## 👋 中文化
- by 微笑卡卡西

## 💖 Support This Project
If this system helps you, consider supporting:
- PayPal: https://www.paypal.me/JohnNathanielMarquez
- GCash: 09605088715

## 📚 Learn More
For full context and discussions:
https://forum.cursor.com/t/rules-for-ultra-context-memories-lessons-scratchpad-with-plan-and-act-modes/48792/22?u=t1nker-1220

---

*注：该系统旨在无缝管理AI交互。有关详细实施指南，请参阅各个规则文件。* 🚀

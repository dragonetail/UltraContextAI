# 🎯 AI Context Rules System
# 🎯 AI 上下文规则系统

## 🌟 Quick Overview
## 🌟 快速概览
A comprehensive system for managing AI interactions through memory management, lessons learned tracking, and dual-mode operation (Plan/Agent). This system ensures consistent, high-quality development while maintaining detailed project documentation and knowledge retention.
一个全面的系统，通过记忆管理、经验教训跟踪和双模式操作（计划/代理）来管理 AI 交互。该系统确保一致、高质量的开发，同时维护详细的项目文档和知识保留。

## 🔄 Core Components
## 🔄 核心组件
1. **Memory System** (`@memories.md`)
1. **记忆系统** (`@memories.md`)
   - Contains categorized entries with dates (e.g., "Project Initialization (March 15, 2024)")
   - 包含带日期的分类条目（例如，"项目初始化（2024年3月15日）"）
   - Provides comprehensive single-line descriptions with full context
   - 提供带完整上下文的全面单行描述
   - Uses clear version numbering format [x.x.x] for each entry
   - 每个条目使用清晰的版本编号格式 [x.x.x]
   - Maintains chronological order of development milestones
   - 维护开发里程碑的时间顺序
   - Creates @memories2.md at 1000 lines with cross-references
   - 在1000行处创建 @memories2.md 并进行交叉引用
   - Documents complete interaction context, changes, and technical details
   - 记录完整的交互上下文、变更和技术细节
   - Never deletes past entries to preserve project history
   - 永不删除过去的条目以保存项目历史

2. **Lessons Learned** (`@lessons-learned.md`)
2. **经验教训** (`@lessons-learned.md`)
   - Captures solutions and best practices
   - 捕获解决方案和最佳实践
   - Uses structured format: Issue → Solution → Impact
   - 使用结构化格式：问题 → 解决方案 → 影响
   - Categorizes by component, TypeScript, errors, etc.
   - 按组件、TypeScript、错误等进行分类
   - Prioritizes issues (Critical/Important/Enhancement)
   - 按优先级（关键/重要/增强）排序问题
   - Links to related code examples
   - 链接到相关代码示例

3. **Scratchpad** (`@scratchpad.md`)
3. **草稿本** (`@scratchpad.md`)
   - Manages current phase and tasks
   - 管理当前阶段和任务
   - Tracks implementation progress
   - 跟踪实施进度
   - Uses clear status markers [X], [-], [ ], [!], [?]
   - 使用清晰的状态标记 [X]、[-]、[ ]、[!]、[?]
   - Maintains task dependencies
   - 维护任务依赖关系
   - Updates confidence metrics
   - 更新置信度指标

## 🎯 Mode System Operation
## 🎯 模式系统操作

### Plan Mode 🎯
### 计划模式 🎯
```markdown
Trigger: "plan"
触发器："plan"
Purpose: Information gathering and planning
目的：信息收集和规划
Requirements:
要求：
- Parse user input
- 解析用户输入
- Cross-reference requirements
- 交叉参考需求
- Generate clarifying questions
- 生成澄清问题
- Calculate confidence score
- 计算置信度分数
- Create task breakdown
- 创建任务分解
```

### Agent Mode ⚡
### 代理模式 ⚡
```markdown
Trigger: "agent"
触发器："agent"
Activation Requirements:
激活要求：
- 95% confidence level
- 95% 置信度水平
- All questions answered
- 所有问题已回答
- Tasks defined
- 任务已定义
- No blocking issues
- 无阻塞问题
- Requirements verified
- 需求已验证
```

## 🚀 Workflow Steps
## 🚀 工作流程步骤

1. **Initialize Planning** 🎯
1. **初始化规划** 🎯
   ```markdown
   - Use "plan" trigger
   - 使用"plan"触发器
   - System creates new scratchpad entry
   - 系统创建新的草稿本条目
   - Generates minimum 3 questions
   - 生成至少3个问题
   - Sets initial confidence score
   - 设置初始置信度分数
   ```

2. **Build Confidence** 📈
2. **建立信心** 📈
   ```markdown
   - Answer all questions
   - 回答所有问题
   - Verify requirements
   - 验证需求
   - Update task dependencies
   - 更新任务依赖关系
   - Monitor confidence score
   - 监控置信度分数
   ```

3. **Execute Implementation** ⚡
3. **执行实施** ⚡
   ```markdown
   - Reach 95% confidence
   - 达到95%置信度
   - Use "agent" trigger
   - 使用"agent"触发器
   - System implements solution
   - 系统实施解决方案
   - Updates documentation
   - 更新文档
   ```

## 🎮 Workflow Examples
## 🎮 工作流程示例

### Example 1: Creating a New Feature
### 示例1：创建新功能
```markdown
USER: "plan implement a new button component"
用户："plan implement a new button component"

AI: 🎯 PLAN MODE ACTIVATED
AI：🎯 计划模式已激活
Current Task: Implement new button component
当前任务：实现新按钮组件
Questions:
问题：
1. What variants are needed? (primary/secondary/outline)
1. 需要哪些变体？（主要/次要/轮廓）
2. Should it support icons?
2. 是否应支持图标？
3. What sizes are required?
3. 需要哪些尺寸？
Confidence: 65%
置信度：65%

USER: "primary and secondary variants, with icons, three sizes"
用户："primary and secondary variants, with icons, three sizes"

AI: Updated Understanding:
AI：更新理解：
- Primary/Secondary variants
- 主要/次要变体
- Icon support
- 图标支持
- Small/Medium/Large sizes
- 小/中/大尺寸
Confidence: 95%
置信度：95%

USER: "agent"
用户："agent"

AI: ⚡ AGENT MODE ACTIVATED
AI：⚡ 代理模式已激活
- Creating Button component
- 创建按钮组件
- Implementing variants
- 实现变体
- Adding icon support
- 添加图标支持
- Testing accessibility
- 测试可访问性
```

### Example 2: Fixing a Bug
### 示例2：修复错误
```markdown
USER: "plan fix the form submission error"
用户："plan fix the form submission error"

AI: 🎯 PLAN MODE ACTIVATED
AI：🎯 计划模式已激活
Current Task: Debug form submission error
当前任务：调试表单提交错误
Questions:
问题：
1. When does the error occur?
1. 错误何时发生？
2. Any error messages in console?
2. 控制台有错误信息吗？
3. Which form component is affected?
3. 哪个表单组件受影响？
Confidence: 50%
置信度：50%

USER: "happens on login form, console shows validation error"
用户："happens on login form, console shows validation error"

AI: Chain of Thought Analysis:
AI：思维链分析：
1. Login form validation
1. 登录表单验证
2. Console error check
2. 控制台错误检查
3. Input validation rules
3. 输入验证规则
Confidence: 95%
置信度：95%

USER: "agent"
用户："agent"

AI: ⚡ AGENT MODE ACTIVATED
AI：⚡ 代理模式已激活
- Debugging validation
- 调试验证
- Fixing error handling
- 修复错误处理
- Testing submission
- 测试提交
```

### Example 3: Project Setup
### 示例3：项目设置
```markdown
USER: "plan setup new Next.js project"
用户："plan setup new Next.js project"

AI: 🎯 PLAN MODE ACTIVATED
AI：🎯 计划模式已激活
Current Task: Initialize Next.js project
当前任务：初始化Next.js项目
Questions:
问题：
1. Which version of Next.js?
1. 使用哪个版本的Next.js？
2. TypeScript or JavaScript?
2. TypeScript还是JavaScript？
3. Which UI components needed?
3. 需要哪些UI组件？
Confidence: 70%
置信度：70%

USER: "Next.js 14, TypeScript, Shadcn UI"
用户："Next.js 14, TypeScript, Shadcn UI"

AI: Project Structure:
AI：项目结构：
- Next.js 14 setup
- Next.js 14设置
- TypeScript configuration
- TypeScript配置
- Shadcn UI integration
- Shadcn UI集成
Confidence: 95%
置信度：95%

USER: "agent"
用户："agent"

AI: ⚡ AGENT MODE ACTIVATED
AI：⚡ 代理模式已激活
- Creating project
- 创建项目
- Setting up TypeScript
- 设置TypeScript
- Installing dependencies
- 安装依赖
```

### Example 4: Documentation Update
### 示例4：文档更新
```markdown
USER: "plan update API documentation"
用户："plan update API documentation"

AI: 🎯 PLAN MODE ACTIVATED
AI：🎯 计划模式已激活
Current Task: Update API docs
当前任务：更新API文档
Questions:
问题：
1. Which endpoints need updates?
1. 哪些端点需要更新？
2. Any new parameters added?
2. 是否添加了新参数？
3. Response format changes?
3. 响应格式有变化吗？
Confidence: 60%
置信度：60%

USER: "new authentication endpoints"
用户："new authentication endpoints"

AI: Documentation Plan:
AI：文档计划：
- Auth endpoints
- 认证端点
- Request/Response formats
- 请求/响应格式
- Example usage
- 使用示例
Confidence: 95%
置信度：95%

USER: "agent"
用户："agent"

AI: ⚡ AGENT MODE ACTIVATED
AI：⚡ 代理模式已激活
- Updating docs
- 更新文档
- Adding examples
- 添加示例
- Verifying formats
- 验证格式
```

## 📝 Documentation Standards
## 📝 文档标准

### Real-time Updates
### 实时更新
- Memories: Every interaction
- 记忆：每次交互
- Lessons: After solutions
- 经验教训：解决方案后
- Scratchpad: During implementation
- 草稿本：实施期间

### Version Control
### 版本控制
```markdown
Memory entry format:
记忆条目格式：
- [x.x.x] Category with date: Comprehensive description with complete context
- [x.x.x] 带日期的类别：带完整上下文的综合描述
- Example: [1.0.0] Project Setup (March 15, 2024): Successfully initialized a new Next.js 14 project with...
- 示例：[1.0.0] 项目设置（2024年3月15日）：成功初始化了一个新的Next.js 14项目...

Cross-file management:
跨文件管理：
- Create @memories2.md at 1000 lines
- 在1000行处创建@memories2.md
- Maintain cross-references between memory files
- 维护记忆文件之间的交叉引用
- Never delete historical entries
- 永不删除历史条目
```

### Cross-referencing
### 交叉引用
```markdown
@memories.md ↔️ @lessons-learned.md ↔️ @scratchpad.md
@memories.md ↔️ @lessons-learned.md ↔️ @scratchpad.md
```

## 🔍 Directory Structure
## 🔍 目录结构
```
.cursor/
├── memories.md          # Interaction history
├── memories.md          # 交互历史
├── lessons-learned.md   # Solutions & practices
├── lessons-learned.md   # 解决方案和实践
├── scratchpad.md       # Current phase tracking
├── scratchpad.md       # 当前阶段跟踪
├── project-requirements.md  # Project specs
├── project-requirements.md  # 项目规格
└── rules/              # System rules
└── rules/              # 系统规则
    └── .cursorrules    # Core rules file
    └── .cursorrules    # 核心规则文件
```

## 🛠️ Best Practices
## 🛠️ 最佳实践

1. **Memory Management**
1. **记忆管理**
   - Create categorized entries with clear dates
   - 创建带有清晰日期的分类条目
   - Write comprehensive single-line descriptions
   - 编写全面的单行描述
   - Use consistent version numbering [x.x.x]
   - 使用一致的版本编号[x.x.x]
   - Include complete technical implementation details
   - 包含完整的技术实施细节
   - Document all development decisions and outcomes
   - 记录所有开发决策和结果
   - Maintain chronological order of project milestones
   - 维护项目里程碑的时间顺序
   - Never delete historical entries
   - 永不删除历史条目

2. **Task Tracking**
2. **任务跟踪**
   - Generate unique task IDs
   - 生成唯一的任务ID
   - Track dependencies
   - 跟踪依赖关系
   - Update status in real-time
   - 实时更新状态
   - Maintain hierarchy
   - 维护层次结构

3. **Documentation**
3. **文档**
   - Update in real-time
   - 实时更新
   - Include version numbers
   - 包含版本号
   - Cross-reference related files
   - 交叉引用相关文件
   - Follow structured formats
   - 遵循结构化格式

## 🎯 Tips & Tricks
## 🎯 提示和技巧

### 🔄 Handling AI & Cursor Issues
### 🔄 处理AI和Cursor问题
1. **Required Open Tabs**:
1. **必需的打开标签**：
   ```
   1️⃣ Active working file
   1️⃣ 活动工作文件
   2️⃣ Cursor Settings (Feature → Resync)
   2️⃣ Cursor设置（功能→重新同步）
   3️⃣ .cursorrules (for auto-reload)
   3️⃣ .cursorrules（用于自动重新加载）
   ```

2. **Quick Reload Process**:
2. **快速重新加载过程**：
   ```
   1. Ctrl+Shift+P
   1. Ctrl+Shift+P
   2. "Developer: Reload Window"
   2. "开发者：重新加载窗口"
   3. Wait 3-10 seconds
   3. 等待3-10秒
   ```

### 💡 Pro Tips
### 💡 专业提示
- Keep .cursorrules file open
- 保持.cursorrules文件打开
- Monitor confidence scores
- 监控置信度分数
- Use proper triggers
- 使用正确的触发器
- Follow memory entry format: [x.x.x] Category (Date): Comprehensive description
- 遵循记忆条目格式：[x.x.x] 类别（日期）：全面描述
- Categorize memory entries by development milestones
- 按开发里程碑对记忆条目进行分类
- Include complete technical details in memory descriptions
- 在记忆描述中包含完整的技术细节
- Cross-reference frequently
- 频繁交叉引用

## 🤝 Contributing
## 🤝 贡献
Feel free to enhance this system:
随时增强此系统：
1. Add custom rules
1. 添加自定义规则
2. Improve tracking
2. 改进跟踪
3. Enhance metrics
3. 增强指标
4. Share practices
4. 分享实践

## 📝 License
## 📝 许可证
MIT License - Free to use and modify!
MIT许可证 - 免费使用和修改！

## 👋 Contacts / Hire me
## 👋 联系方式/雇佣我
- Instagram: https://www.instagram.com/clover_nat/
- Instagram: https://www.instagram.com/clover_nat/
- Facebook: https://www.facebook.com/nathanielmarquez.20
- Facebook: https://www.facebook.com/nathanielmarquez.20
- Twitter: https://x.com/T1nker1220
- Twitter: https://x.com/T1nker1220

## 💖 Support This Project
## 💖 支持本项目
If this system helps you, consider supporting:
如果此系统对您有帮助，请考虑支持：
- PayPal: https://www.paypal.me/JohnNathanielMarquez
- PayPal: https://www.paypal.me/JohnNathanielMarquez
- GCash: 09605088715
- GCash: 09605088715

## 📚 Learn More
## 📚 了解更多
For full context and discussions:
有关完整上下文和讨论：
https://forum.cursor.com/t/rules-for-ultra-context-memories-lessons-scratchpad-with-plan-and-act-modes/48792/22?u=t1nker-1220
https://forum.cursor.com/t/rules-for-ultra-context-memories-lessons-scratchpad-with-plan-and-act-modes/48792/22?u=t1nker-1220

---

*Note: This system is designed for seamless AI interaction management. For detailed implementation guidelines, refer to the individual rule files.* 🚀
*注：该系统旨在无缝管理AI交互。有关详细实施指南，请参阅各个规则文件。* 🚀

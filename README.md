# 逻明同学 v16 程序化自适应思维融合版

## 🎯 项目概述

逻明同学是一个基于PromptX框架开发的高级AI角色，专注于问题分析和解决方案设计。本版本成功融合了v16程序化自适应思维模板的精华，实现了"像AI程序一样精确思考，像朋友一样自然交流"的设计理念。

**重要说明**：本项目提供的是AI角色定义文件，需要配合PromptX框架才能运行。逻明同学的所有智能能力都依赖于PromptX的MCP服务器环境。

## 📋 依赖说明

### 🔗 **核心依赖**
- **PromptX框架** - 本项目的运行基础
  - 项目地址：https://github.com/Deepractice/PromptX
  - 版本要求：支持DPML协议和MCP服务器
  - 作用：提供AI角色的运行环境和工具集成能力

### 🎯 **项目关系**
- **逻明同学项目** = AI角色定义文件（.role.md、.thought.md、.execution.md等）
- **PromptX框架** = AI角色运行环境（MCP服务器、工具集成、角色激活等）
- **关系**：逻明同学需要在PromptX环境中才能发挥完整能力

## ⚙️ 环境配置

### 🚀 **一键配置PromptX MCP服务器**

**零配置模式 - 30秒完成配置**

1. **打开Claude Desktop配置文件**
   - **Windows**: `%APPDATA%\Claude\claude_desktop_config.json`
   - **macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`

2. **添加MCP服务器配置**
   ```json
   {
     "mcpServers": {
       "promptx": {
         "command": "npx",
         "args": [
           "-y",
           "-f",
           "--registry",
           "https://registry.npmjs.org",
           "dpml-prompt@beta",
           "mcp-server"
         ]
       }
     }
   }
   ```

3. **重启Claude Desktop**
   - 保存配置文件后重启Claude Desktop
   - 配置成功后会自动下载和启动PromptX MCP服务器

### ✅ **配置验证**
配置成功后，您应该能看到：
- Claude Desktop启动时自动连接PromptX MCP服务器
- 可以使用`promptx_hello`等PromptX命令
- 能够激活和使用逻明同学角色

### 🔧 **高级配置**（可选）
如需自定义配置，请参考PromptX官方文档：
- 文档地址：https://github.com/Deepractice/PromptX/blob/main/README.md
- 配置选项：工作目录、日志级别、扩展插件等

## ✨ 核心特性

### 🧠 **智能分析能力**
- **深度问题分析** - 从模糊描述中快速识别真实需求
- **系统性思维** - 多维度思考，总分总结构
- **贾维斯式智能** - 复杂数据分析、战略规划、自主决策

### ⚡ **程序化自适应执行** (v16精华)
- **五步程序化流程** - 任务接收→三次信息收集→智能规划→分步执行→质量检查
- **"别贪多，一步一步做"原则** - 严格按步骤执行，确保质量
- **自适应回退机制** - 发现问题立即回到相应步骤优化

### 💬 **人性化交流** ("说人话"理念)
- **例子先行策略** - 用具体例子解释抽象概念
- **生活化比喻** - 技术概念生活化（如API=餐厅服务员）
- **通俗易懂表达** - 避免技术黑话，降低理解门槛

### 🔧 **系统化工具使用**
- **逻辑门架构** - AND/OR/NOT/XOR门验证决策逻辑
- **程序控制结构** - 顺序/分支/循环/函数结构化执行
- **智能工具选择** - 基于任务复杂度选择最优工具组合

## 📁 文件结构

```
.promptx/resource/domain/luoming/
├── luoming.role.md                           # 主角色文件
├── baseline-config.md                        # 出厂默认配置
├── factory-config.md                         # 工厂配置管理
├── architecture-overview.md                  # 逻辑门架构说明
├── adaptive-system-integration.md            # 自适应系统集成说明
├── tool-workflow-architecture.md             # 工具使用工作流程架构
├── thought/                                  # 思维模式文件
│   ├── problem-analysis.thought.md           # 问题分析思维
│   ├── jarvis-intelligence.thought.md        # 贾维斯智能思维
│   ├── logic-gate-architecture.thought.md    # 逻辑门架构思维
│   ├── config-management.thought.md          # 配置管理思维
│   └── example-first-thinking.thought.md     # 例子先行思维模式 (v16新增)
└── execution/                                # 执行流程文件
    ├── solution-design.execution.md          # 解决方案设计流程
    ├── program-control-structure.execution.md # 程序控制结构流程
    ├── adaptive-learning.execution.md        # 自适应学习流程
    ├── tool-integration.execution.md         # 工具集成执行流程
    ├── adaptive-execution-flow.execution.md  # 程序化自适应执行流程 (v16新增)
    └── human-friendly-communication.execution.md # 人性化交流执行规范 (v16新增)
```

## 🚀 使用方法

### 📋 **使用前准备**
在使用逻明同学之前，请确保已完成以下步骤：
1. ✅ **配置PromptX MCP服务器** - 参考上方"环境配置"章节
2. ✅ **重启Claude Desktop** - 确保MCP服务器正常运行
3. ✅ **验证PromptX连接** - 测试`promptx_hello`命令是否可用

### 1. 环境要求
- **PromptX框架** - 必须先完成MCP服务器配置
- **Claude Desktop** - 支持MCP协议的AI客户端
- **Node.js环境** - PromptX MCP服务器运行依赖

### 2. 角色激活
```bash
# 第一步：验证PromptX是否正常工作
promptx_hello

# 第二步：激活逻明同学角色
promptx_action luoming
```

**激活成功标志**：
- 看到"逻明同学角色已完全激活"的确认信息
- 获得完整的角色能力说明
- 可以开始使用逻明同学的专业服务

### 3. 核心功能使用

#### 🔍 **复杂问题分析**
```
逻明同学，我遇到了[具体问题描述]，请帮我分析问题本质和解决方案
```

#### 💡 **技术方案设计**
```
逻明同学，我需要设计一个[项目描述]，请帮我制定技术方案
```

#### 📊 **项目规划管理**
```
逻明同学，请帮我规划[项目名称]的实施计划和风险控制
```

## 🎯 v16版本更新内容

### 🆕 **新增特性**
- **程序化自适应执行流程** - 融合v16模板的五步执行框架
- **"说人话"交流理念** - 大幅提升用户交互友好性
- **例子先行思维模式** - 具体例子→抽象概念的认知路径
- **技术概念生活化比喻库** - 降低技术理解门槛

### 🔄 **优化改进**
- **执行力检查清单** - 确保高质量执行的程序化验证
- **自适应回退机制** - 智能问题识别和流程优化
- **三次信息收集强制** - 确保信息全面可靠
- **工具使用流程增强** - 融入新的执行原则和质量保证

## 🏆 核心优势

1. **🎯 专业性与友好性并重** - 既保持技术专业性，又具备极佳的用户体验
2. **⚡ 严谨性与灵活性统一** - 程序化执行确保质量，自适应机制保证灵活
3. **🧠 系统性与实用性结合** - 完整的理论框架支撑实用的解决方案
4. **💬 智能化与人性化融合** - AI级别的分析能力配合人性化的交流方式

## 📝 开发历程

- **v1.0** - 基础问题分析能力
- **v2.0** - 贾维斯智能分析集成
- **v3.0** - 逻辑门架构设计
- **v4.0** - 程序控制结构化
- **v5.0** - 自适应学习系统
- **v6.0** - 工具集成使用流程
- **v16.0** - 程序化自适应思维融合 (当前版本)

## 🛠️ 故障排除

### ❌ **常见问题及解决方案**

#### **问题1：找不到promptx命令**
```
错误信息：Command 'promptx_hello' not found
```
**解决方案**：
1. 检查MCP服务器配置是否正确
2. 确认已重启Claude Desktop
3. 验证配置文件路径和JSON格式

#### **问题2：逻明同学角色激活失败**
```
错误信息：角色 "luoming" 不存在
```
**解决方案**：
1. 确保项目文件完整下载
2. 检查`.promptx/resource/domain/luoming/`目录是否存在
3. 运行`promptx_init`刷新角色注册表

#### **问题3：MCP服务器连接失败**
```
错误信息：MCP server connection failed
```
**解决方案**：
1. 检查网络连接是否正常
2. 确认Node.js环境可用
3. 尝试手动运行MCP服务器命令
4. 查看Claude Desktop日志文件

#### **问题4：角色功能不完整**
```
现象：逻明同学回复简单，缺少专业能力
```
**解决方案**：
1. 确认角色激活成功（看到完整激活信息）
2. 检查所有.thought.md和.execution.md文件是否存在
3. 重新激活角色：`promptx_action luoming`

### 📞 **获取帮助**
- **PromptX框架问题** - 访问：https://github.com/Deepractice/PromptX/issues
- **逻明同学问题** - 在本项目提交Issue
- **配置问题** - 参考PromptX官方文档

## 🤝 贡献指南

欢迎提交Issue和Pull Request来改进逻明同学的能力！

### 📋 **贡献方式**
- **Bug报告** - 发现问题请提交详细的Issue
- **功能建议** - 欢迎提出新功能和改进建议
- **代码贡献** - 提交Pull Request改进角色能力
- **文档完善** - 帮助改进使用说明和配置指南

## 📄 许可证

本项目采用MIT许可证。

---

**逻明同学v16 - 让AI真正为人服务，用人话与用户交流，像AI程序一样精确思考！** 🧠💬✨
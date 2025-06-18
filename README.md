# 逻明同学 v16 - 全自动化AI助手

## 🚀 三步安装，立即使用

**第一步**：配置PromptX到Claude Desktop → **第二步**：下载本项目 → **第三步**：复制角色文件

### 📋 详细步骤

1. **配置PromptX MCP服务器**
   - 打开Claude Desktop配置文件：`%APPDATA%\Claude\claude_desktop_config.json` (Windows) 或 `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS)
   - 添加配置：
   ```json
   {
     "mcpServers": {
       "promptx": {
         "command": "npx",
         "args": ["-y", "-f", "--registry", "https://registry.npmjs.org", "dpml-prompt@beta", "mcp-server"]
       }
     }
   }
   ```
   - 重启Claude Desktop

2. **下载并安装角色包**
   ```bash
   # 下载项目
   git clone https://github.com/xiuminsama99/luoming-v16-adaptive-thinking.git

   # 初始化PromptX
   promptx_init

   # 复制角色文件到PromptX目录
   # Windows: xcopy "项目路径\.promptx\*" "%USERPROFILE%\.promptx\" /E /Y
   # macOS/Linux: cp -r "项目路径/.promptx/*" "~/.promptx/"

   # 激活逻明同学
   promptx_action luoming
   ```

3. **开始使用**
   - 看到激活成功信息即可开始使用
   - 直接对话："逻明同学，帮我分析这个项目..."

## 🎯 核心特色

- **🤖 全自动化AI助手** - 提出需求即可自动分析、规划、执行
- **💬 说人话交流** - 用生活化语言解释技术概念
- **🧠 智能决策** - 具备自主思考和问题解决能力
- **🔄 自适应执行** - 遇到问题自动调整策略直到满意

## 📞 遇到问题？

- **PromptX框架问题** → https://github.com/Deepractice/PromptX/issues
- **逻明同学问题** → https://github.com/xiuminsama99/luoming-v16-adaptive-thinking/issues

---

**📁 [查看完整安装说明](./README-FULL.md)** | **MIT许可证** | **逻明同学v16 - 让AI真正为人服务！** 🧠💬✨


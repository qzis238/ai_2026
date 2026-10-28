# 🌤️ 智能天气查询 AI Agent (V1/V2 双版本)

这是一个基于 LangChain 和大语言模型（LLM）独立开发的智能天气助手，包含底层原理实现与多轮对话应用。

## ✨ 核心亮点
1. **底层 ReAct 循环实现 (V1)**：不依赖高阶黑盒框架，手写了 Thought -> Action -> Observation 的核心循环，精准解析模型意图并调度 `get_weather` 工具。
2. **多轮对话与上下文管理 (V2)**：基于 LangChain `create_agent` 构建，自行维护 `messages` 历史列表，使 AI 具备记忆能力，支持连贯追问。
3. **高可用降级策略（Fallback）**：针对第三方公开 API（wttr.in）网络不稳定、超时的情况，设计了全局异常捕获（try-except）。当网络异常时，自动切换至本地 Mock 数据，**确保程序不崩溃且用户体验不中断**。

## 🛠️ 技术栈
- Python 3
- LangChain (LangChain Core / LangChain OpenAI)
- 阿里云百炼大模型 (通义千问)
- 环境变量管理 (`dotenv`)

## 🚀 运行说明
1. 安装依赖：`pip install -r requirements.txt`
2. 配置 `.env` 文件（填入你的 `DATA_API_KEY`, `DATA_BASE_URL`, `DATA_MODEL`）
3. 运行 V2 多轮对话版：`python Weather02.py`
4. 运行 V1 底层测试版：`python Weather01.py`

*图：第三方 API 超时，系统触发降级策略，平滑输出模拟数据*

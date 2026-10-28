# 🌤️ 智能天气查询 AI Agent (多轮对话版)

这是一个基于大语言模型（LLM）独立开发的智能天气查询助手。它不仅能进行多轮自然语言对话，还能通过意图识别调用外部天气 API 获取实时数据。

## ✨ 核心功能
- **意图识别与工具调用**：通过 Prompt Engineering 让大模型准确提取用户提问中的城市和时间参数。
- **多轮对话管理**：支持上下文连贯对话（如追问“那明天呢？”），并提供 `clear` 指令清空上下文。
- **安全的密钥管理**：使用 `.env` 文件隔离大模型 API Key，确保开源代码安全。

## 🛠️ 技术栈
- Python 3
- 阿里云通义千问 API (DashScope)
- Python-dotenv (环境变量管理)
- Requests (HTTP 请求处理)

## 🚀 如何运行
1. 克隆项目到本地。
2. 安装依赖：`pip install -r requirements.txt`
3. 在根目录创建 `.env` 文件，并填入你的密钥：`API_KEY=你的阿里云API_KEY`
4. 运行主程序：`python Weather02.py`

# 智扫通机器人智能客服系统

A RAG (Retrieval-Augmented Generation) based intelligent customer service system with Streamlit web interface.

## 项目简介

这是一个基于RAG（检索增强生成）技术的智能客服系统，集成了大语言模型、向量数据库和智能代理，能够根据用户的提问从知识库中检索相关信息并生成准确的回答。

## 主要功能

- **智能问答**: 基于RAG技术的问答系统，能够从文档库中检索相关信息
- **多工具集成**: 集成了天气查询、用户位置、用户ID获取等多种工具
- **实时监控**: 内置工具调用监控和日志记录功能
- **流式响应**: 支持流式输出，提供更好的用户体验
- **Web界面**: 基于Streamlit的现代化Web界面

## 技术栈

- **Python 3.8+**
- **Streamlit**: Web应用框架
- **LangChain**: LLM应用开发框架
- **ChromaDB**: 向量数据库
- **大语言模型**: 支持多种LLM模型

## 项目结构

```
├── agent/               # 智能代理模块
│   ├── react_agent.py   # React代理实现
│   └── tools/           # 工具函数
├── rag/                 # RAG服务模块
│   ├── rag_service.py   # RAG服务实现
│   └── vector_store.py  # 向量存储服务
├── config/              # 配置文件
│   ├── agent.yml        # 代理配置
│   ├── rag.yml          # RAG配置
│   ├── chroma.yml       # ChromaDB配置
│   └── prompts.yml      # 提示词配置
├── model/               # 模型相关
├── utils/               # 工具函数
├── data/                # 数据文件
├── logs/                # 日志文件
├── app.py               # Streamlit应用入口
└── main.py              # 主程序
```

## 快速开始

### 环境要求

- Python 3.8 或更高版本
- pip 包管理器

### 安装步骤

1. **克隆项目**
   ```bash
   git clone <repository-url>
   cd RAG_Project
   ```

2. **创建虚拟环境**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Linux/Mac
   # 或
   .venv\Scripts\activate     # Windows
   ```

3. **安装依赖**
   ```bash
   pip install -r requirements.txt
   ```

4. **配置环境变量**
   创建 `.env` 文件并配置必要的API密钥：
   ```
   # LLM API配置
   OPENAI_API_KEY=your_api_key
   # 或其他模型API密钥
   ```

5. **启动应用**
   ```bash
   streamlit run app.py
   ```

## 配置说明

### 模型配置
在 `config/` 目录下配置各种模型参数：
- `agent.yml`: 智能代理配置
- `rag.yml`: RAG服务配置
- `prompts.yml`: 系统提示词配置

### 向量数据库
使用 ChromaDB 作为向量存储，配置在 `config/chroma.yml` 中。

## 使用方法

1. 启动应用后，在浏览器中访问显示的URL
2. 在聊天界面输入问题
3. 系统会自动检索相关知识并生成回答
4. 可以实时查看回答的生成过程

## 开发指南

### 添加新的工具

在 `agent/tools/` 目录下创建新的工具函数，然后在 `react_agent.py` 中导入并使用。

### 自定义提示词

修改 `config/prompts.yml` 文件来自定义系统提示词。

### 扩展知识库

将文档添加到 `data/` 目录，系统会自动处理并建立向量索引。

## 贡献指南

1. Fork 项目
2. 创建功能分支
3. 提交更改
4. 推送到分支
5. 创建 Pull Request

## 联系方式

如有问题或建议，请提交 Issue 或联系项目维护者。
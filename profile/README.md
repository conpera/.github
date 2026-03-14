<div align="center">

<img src="https://avatars.githubusercontent.com/u/123456789" width="120" height="120" style="border-radius: 50%;">

# Conpera AI

**开源 AI Agent 平台 — 让智能服务触手可及**

[![GitHub Org's stars](https://img.shields.io/github/stars/conpera?style=social)](https://github.com/conpera)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white)](https://python.org)

[官网](https://conpera.ai) • [文档](https://docs.conpera.ai) • [社区](https://discord.gg/conpera)

</div>

---

## 🚀 关于 Conpera

Conpera 是一个**模块化、可扩展的开源 AI Agent 平台**，致力于让开发者和企业能够快速构建、部署和管理智能代理服务。

### 核心特点

| 特性 | 说明 |
|------|------|
| 🤖 **多 Agent 架构** | 支持新闻、天气、股票等多种 Agent，易于扩展 |
| 🔗 **工作流编排** | 基于 DAG 的可视化工作流设计，支持复杂业务逻辑 |
| 🧠 **多模型支持** | 集成 OpenAI、Gemini、Claude 等主流 LLM |
| ⚡ **高性能异步** | 基于 FastAPI + Celery，支持高并发处理 |
| 🔌 **插件化设计** | Provider 注册机制，轻松接入新服务 |

---

## 📦 核心项目

### [conpera.ai-agent](https://github.com/conpera/conpera.ai-agent)

AI Agent 平台核心实现

```bash
pip install conpera-agent
```

**技术栈**: `Python` `FastAPI` `PostgreSQL` `Redis` `Celery`

**功能亮点**:
- ✅ RSS 新闻抓取与 AI 总结
- ✅ 多 Provider LLM 路由
- ✅ DAG 工作流执行引擎
- ✅ Telegram Bot 集成
- ✅ RESTful API

---

## 🏗️ 架构概览

```
┌─────────────────────────────────────────────────────────────┐
│                        用户交互层                             │
├─────────────┬─────────────┬─────────────┬─────────────────┤
│  Telegram   │   Discord   │   Web UI    │   REST API      │
└──────┬──────┴──────┬──────┴──────┬──────┴────────┬────────┘
       │             │             │               │
       └─────────────┴──────┬──────┴───────────────┘
                            │
       ┌────────────────────▼────────────────────┐
       │         Conpera Agent Core              │
       │    ┌──────────────────────────────┐     │
       │    │      Workflow Engine         │     │
       │    │   (DAG Execution)            │     │
       │    └──────────────┬───────────────┘     │
       │                   │                     │
       │    ┌──────────────┼──────────────┐      │
       │    ▼              ▼              ▼      │
       │ ┌──────┐     ┌──────┐      ┌────────┐   │
       │ │News  │     │ LLM  │      │Other   │   │
       │ │Agent │     │Router│      │Agents  │   │
       │ └──┬───┘     └──┬───┘      └────┬───┘   │
       └────┼────────────┼───────────────┼───────┘
            │            │               │
       ┌────▼────────────▼───────────────▼───────┐
       │              Data Layer                  │
       │  ┌────────┐ ┌────────┐ ┌────────────┐  │
       │  │PostgreSQL│ │ Redis  │ │  Vector DB │  │
       │  └────────┘ └────────┘ └────────────┘  │
       └─────────────────────────────────────────┘
```

---

## 🚀 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/conpera/conpera.ai-agent.git
cd conpera.ai-agent
```

### 2. 安装依赖

```bash
pip install -r requirements.txt
```

### 3. 配置环境变量

```bash
cp .env.example .env
# 编辑 .env，设置你的 API keys
```

### 4. 运行演示

```bash
# 命令行演示
python main.py demo --keyword technology

# 启动 API 服务
python main.py serve
```

---

## 🛠️ 开发路线图

- [x] 核心 Agent 框架
- [x] 工作流引擎 (DAG)
- [x] 多 Provider LLM 支持
- [x] News Agent (RSS + AI 总结)
- [ ] Weather Agent
- [ ] Stock Agent
- [ ] Web 管理后台
- [ ] 可视化工作流编辑器
- [ ] 插件市场

---

## 🤝 参与贡献

我们欢迎所有形式的贡献！

```bash
# Fork 仓库
git clone https://github.com/conpera/conpera.ai-agent.git

# 创建分支
git checkout -b feature/your-feature

# 提交更改
git commit -m "feat: add amazing feature"

# 推送分支
git push origin feature/your-feature

# 创建 Pull Request
```

查看 [CONTRIBUTING.md](CONTRIBUTING.md) 了解详情。

---

## 📄 许可证

所有项目均采用 [MIT 许可证](LICENSE) 开源。

---

<div align="center">

**Made with ❤️ by Conpera Team**

[GitHub](https://github.com/conpera) • [Twitter](https://twitter.com/conpera_ai) • [Discord](https://discord.gg/conpera)

</div>

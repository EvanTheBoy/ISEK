
<!-- Banner Image -->
<p align="center">
  <img src="assets/banner_cn.png" alt="Isek Banner" width="100%" />
</p>

<h1 align="center">Isek：去中心化的 Agent-to-Agent (A2A) 网络</h1>

<p align="center">
  <a href="https://pypi.org/project/isek/"><img src="https://img.shields.io/pypi/v/isek" alt="PyPI 版本" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="许可证：MIT" /></a>
  <a href="mailto:team@isek.xyz"><img src="https://img.shields.io/badge/contact-team@isek.xyz-blue" alt="邮箱" /></a>
</p>

<h4 align="center">
    <a href="README.md">English</a> |
    <a href="README_CN.md">中文</a>
</h4>

---

**ISEK** 是一个去中心化的Agent网络框架，旨在构建具备智能协作能力的 A2A (Agent-to-Agent) 系统。Isek 网络集成了 Google **A2A** 协议和 **ERC-8004** 合约，以实现身份注册、声誉构建和协作任务解决。这些元素共同形成了一个自组织的去中心化智能体社区。

> 🧪 **ISEK 正在持续完善中。** 欢迎大家贡献代码、参与试用并反馈建议。

---

## ISEK 解决什么问题?

我们的平台允许智能体开发者在本地运行其智能体。通过点对点连接，这些智能体加入 ISEK 网络，并可以直接向用户提供服务。
虽然大多数框架将智能体视为孤立的执行器，但 **ISEK** 专注于缺失的一层：**去中心化的智能体协作与协调**。我们相信智能系统的未来在于能够进行上下文共享、团队组建和集体推理的**自组织智能体网络** —— 所有这些都无需中央控制。

> ISEK 不仅仅是运行智能体 —— 它是赋能智能体**相互发现、协同推理并作为去中心化系统行动**。

## 为什么 ERC-8004 很重要?

ERC-8004 提供了一个去中心化的身份、声誉和验证注册框架，为无需信任的验证和声誉管理奠定了基础。
---

## 🌟 功能亮点

- **🧠 去中心化协作**  
  使用 ERC-8004 无需信任的智能体合约作为我们的注册中心，我们提供去中心化的身份、声誉和验证服务。智能体可以直接发现伙伴并协作 —— 没有单点故障。
- **🌐 分布式部署**  
  智能体所有者可以 100% 在本地运行其智能体，铸造智能体 NFT，并使用智能体钱包来获得完全的所有权和控制权。
- **🔌 基于 MCP 的智能体发现**  
  我们的地图服务器连接到智能体发现服务，使用户可以轻松找到智能体。配置一次 MCP 服务，您就可以通过您喜欢的 AI 聊天机器人直接访问智能体。
- **💻 开发者友好 CLI：**  
  简洁的命令行界面使智能体的设置、部署和管理变得快速而简单。

---

## 🚀 快速开始

### 安装

```bash
pip install isek
isek setup
```

### 前置要求

- **Python 3.10+**
- **Node.js 18+**（用于 P2P 功能）

> 💡 **提示：** `isek setup` 命令会自动处理 Python 和 JavaScript 依赖。

### 设置环境变量

创建 `.env` 文件：

```env
OPENAI_MODEL_NAME=gpt-4o-mini
OPENAI_BASE_URL=https://api.openai.com/v1
OPENAI_API_KEY=your_api_key
```

### 启动智能体

```python
from isek.agent.isek_agent import IsekAgent
from isek.models.openai import OpenAIModel
import dotenv
dotenv.load_dotenv()

agent = IsekAgent(
    name="My Agent",
    model=OpenAIModel(model_id="gpt-4o-mini"),
    description="A helpful assistant",
    instructions=["Be polite", "Provide accurate information"],
    success_criteria="User gets a helpful response"
)

response = agent.run("hello")
```

### 试用示例

在 examples 文件夹中，按照从 level 1 到 level 10 的示例顺序学习，您就能对 ISEK 有很好的了解。

---

## 🧪 CLI 命令

```bash
isek setup       # 安装 Python 和 JavaScript 依赖
isek clean       # 清理临时文件
isek --help      # 查看可用命令
```

---

## 🧱 项目结构

```
isek/
├── examples                   # Isek 使用示例脚本
├── isek                       # 核心功能模块
│   ├── agent                  # Agent 的逻辑与行为定义
│   ├── node                   # 节点编排
│   ├── protocol               # Agent 间通信的协议层
│   ├── memory                 # Agent 的上下文与状态管理
│   ├── models                 # LLM 后端模型接口
│   ├── team                   # 多 Agent 组织结构接口
│   ├── tools                  # Agent 可调用的工具库
│   ├── utils                  # 通用工具函数
│   ├── cli.py                 # 命令行入口
│   └── isek_center.py         # 本地注册中心与协调服务
├── docs/                      # 文档
└── README.md                  # 项目简介与文档入口
```

---

## 🌟 给我们 Star 吧 😉

<img src="/Users/haowenxia/PycharmProjects/ISEK/star_gif.gif" alt="star_gif" style="zoom:67%;" />

---

## 🤝 贡献方式

我们欢迎开发者、研究人员和早期使用者的加入！

* 💬 通过 [GitHub Issues](https://github.com/your-repo/issues) 提出建议或反馈问题
* 📧 直接联系我们：[team@isek.xyz](mailto:team@isek.xyz)
* 📄 查阅我们的 [贡献指南](CONTRIBUTING.md)

---

## 📜 开源协议

本项目采用 [MIT License](LICENSE) 开源。

---
## ⚠️ 法律声明

ISEK 是一个开源、无许可的技术框架，旨在支持去中心化智能体协作系统的构建。  
本项目的贡献者不运营、控制或监控任何已部署的智能体或其行为。  
使用本项目即表示您将为自己的行为承担全部责任。详情请参阅 [LEGAL.md](./LEGAL.md)。

---
<p align="center">
  Made with ❤️ by the <strong>Isek Team</strong><br />
  <em>Autonomy is not isolation. It's cooperation, at scale.</em>
</p>

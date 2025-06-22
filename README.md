<!-- Banner Image -->
<p align="center">
  <img src="assets/banner.png" alt="Isek Banner" width="100%" />
</p>

<h1 align="center">Isek: Decentralized Agent-to-Agent (A2A) Network</h1>

<p align="center">
  <a href="https://pypi.org/project/isek/"><img src="https://img.shields.io/pypi/v/isek" alt="PyPI version" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT" /></a>
  <a href="mailto:team@isek.xyz"><img src="https://img.shields.io/badge/contact-team@isek.xyz-blue" alt="Email" /></a>
</p>

<h4 align="center">
    <a href="README.md">English</a> |
    <a href="README_CN.md">中文</a>
</h4>

---

**Isek** is a decentralized agent network framework designed for building intelligent, collaborative agent-to-agent (A2A) systems. Agents in Isek autonomously discover peers, share context, and cooperatively solve tasks, forming a self-organizing, decentralized society.

With native integration of large language models (LLMs) and a user-friendly CLI, Isek empowers developers and researchers to quickly prototype, deploy, and manage intelligent agent networks.

> 🧪 **ISEK is under active development.** Contributions, feedback, and experiments are highly welcome.

---

## 🌟 Features

- **🧠 Decentralized Cooperation:**  
  Autonomous peer discovery and agent-to-agent collaboration with no single point of failure.

- **🌐 Distributed Deployment:**  
  Seamless multi-node or cloud deployment for scalability and robustness.

- **🗣️ LLM-Enhanced Intelligence:**  
  Built-in integration with models like OpenAI for natural interaction and reasoning.

- **🔌 Modular and Extensible:**  
  Easily customize agents, add new models, or extend functionalities.

- **💻 Developer-Friendly CLI:**  
  Streamlined CLI for painless agent setup and control.

---

## 📦 Installation

```bash
pip install isek
```

> Requires **Python 3.10+**

---

## 🚀 Quick Start

### 1️⃣ Set Up Environment

Create a `.env` file:

```env
OPENAI_MODEL_NAME=gpt-4o-mini
OPENAI_BASE_URL=https://api.openai.com/v1
OPENAI_API_KEY=your_api_key
```

### 2️⃣ Launch Agent

```python
from isek.agent.agent import Agent
from isek.models.openai import OpenAIModel
import dotenv
dotenv.load_dotenv()

agent = Agent(
    name="My Agent",
    model=OpenAIModel(model_id="gpt-4o-mini"),
    description="A helpful assistant",
    instructions=["Be polite", "Provide accurate information"],
    success_criteria="User gets a helpful response"
)

response = agent.run("hello")
```

---

## 🧪 CLI Commands

```bash
isek clean       # Clean temporary files
isek --help      # View available commands
```

---

## 🧱 Project Structure

```
isek/
├── examples                   # Sample scripts demonstrating Isek usage
├── isek                       # Core functionality and modules
│   ├── agent                  # Agent logic and behavior
│   ├── node                   # Node orchestration
│   ├── protocol               # Inter-Agent communication Protocol Layer
│   ├── memory                 # Agent state and context
│   ├── models                 # LLM backends and interfaces
│   ├── team                   # Multi-Agent Organization Interface
│   ├── tools                  # The toolkit library for Agents
│   ├── utils                  # Utility functions
│   ├── cli.py                 # CLI entry point
│   └── isek_center.py         # Local registry and coordinator
├── script                     # Utility scripts (e.g., clean.py)
├── pyproject.toml             # Build and dependency configuration
└── README.md                  # Project overview and documentation
```

---

## 🤝 Contributing

We welcome collaborators, researchers, and early adopters!

* 💬 Open issues or suggestions via [GitHub Issues](https://github.com/your-repo/issues)
* 📧 Contact us directly: [team@isek.xyz](mailto:team@isek.xyz)
* 📄 See our [Contribution Guidelines](CONTRIBUTING.md)

---

## 📜 License

Licensed under the [MIT License](LICENSE).

---

<p align="center">
  Made with ❤️ by the <strong>Isek Team</strong><br />
  <em>Autonomy is not isolation. It's cooperation, at scale.</em>
</p>

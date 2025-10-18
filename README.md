# 🚀 Google ADK & MCP Learning Project Collection

<div align="center">

![Google ADK](https://img.shields.io/badge/Google-ADK-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-2.0-FF6F00?style=for-the-badge&logo=google&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-Protocol-00A67E?style=for-the-badge&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**A comprehensive collection of Google Agent Development Kit (ADK) projects demonstrating AI agent patterns, workflows, and Model Context Protocol (MCP) integration**

[🎯 Features](#-key-features) • [📚 Projects](#-projects) • [🛠️ Getting Started](#-getting-started) • [📖 Learn More](#-learn-more)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [What is Google ADK?](#-what-is-google-adk)
- [What is MCP?](#-what-is-mcp)
- [Key Features](#-key-features)
- [Projects](#-projects)
- [Architecture Patterns](#-architecture-patterns)
- [Getting Started](#-getting-started)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Usage Examples](#-usage-examples)
- [Learn More](#-learn-more)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌟 Overview

This repository is a comprehensive learning collection showcasing **Google's Agent Development Kit (ADK)** framework with practical, real-world examples. It demonstrates various AI agent patterns including hierarchical agents, parallel processing, loop agents, and Model Context Protocol (MCP) integration.

Each project is designed to be a **standalone learning module** that you can run, modify, and learn from to build sophisticated AI agent systems.

---

## 🤖 What is Google ADK?

**Google Agent Development Kit (ADK)** is a powerful framework for building AI-powered agents using Google's Gemini models. It provides:

- 🎯 **Agent Types**: LlmAgent, LoopAgent, ParallelAgent, SequentialAgent
- 🔧 **Built-in Tools**: Google Search, web scraping, and custom tools
- 💾 **State Management**: Session-based state handling across agent interactions
- 🔄 **Orchestration**: Complex workflows with sub-agents and delegation
- 📊 **Event Streaming**: Real-time streaming responses and progress tracking

ADK simplifies the creation of complex AI systems by providing abstractions for agent communication, task delegation, and workflow orchestration.

---

## 🔌 What is MCP?

**Model Context Protocol (MCP)** is an open protocol that standardizes how applications provide context to Large Language Models (LLMs). Think of it as a universal connector that allows:

- 🌐 **Tool Interoperability**: Share tools across different AI frameworks
- 🔄 **Bidirectional Communication**: Client-server architecture for AI tools
- 📦 **Standardized Interface**: Consistent tool definitions and execution
- 🚀 **Scalability**: Build once, use across multiple AI applications

In this repository, you'll see how ADK agents can consume MCP servers and how ADK tools can be exposed as MCP servers.

---

## ✨ Key Features

### 🎨 Diverse Agent Patterns
- **Hierarchical Agents**: Parent-child delegation patterns
- **Parallel Agents**: Concurrent task execution
- **Loop Agents**: Iterative workflows
- **Sequential Agents**: Step-by-step pipelines

### 🛠️ Real-World Applications
- YouTube Shorts script generation with visuals
- E-commerce shopping assistants
- Sustainable energy research automation
- Web content extraction and analysis

### 📚 Learning-Focused
- Clear code comments and documentation
- Progressive complexity (simple to advanced)
- Standalone, runnable examples
- Best practices for AI agent development

---

## 📦 Projects

### 1️⃣ YouTube Shorts Script Assistant
**Path**: `1youtube_short_script_assistant/`

A hierarchical agent system that creates complete YouTube Shorts concepts with scripts and visual ideas.

**Features**:
- 🎬 Script generation using Google Search
- 🎨 Visual concept creation
- 📝 Markdown formatting
- 🔄 Sub-agent coordination

**Agent Pattern**: Hierarchical (LlmAgent with sub-agents)

**Tech Stack**: Gemini 2.5 Pro/Flash, Google Search API

```python
# Agent hierarchy:
youtube_shorts_agent (Parent)
├── scriptwriter_agent (Script creation)
├── visualizer_agent (Visual concepts)
└── formatter_agent (Markdown output)
```

---

### 2️⃣ YouTube Shorts Loop Agent
**Path**: `2youtube_short_loop_agent/`

An iterative workflow that processes YouTube Shorts creation through multiple iterations.

**Features**:
- 🔁 Loop-based processing (max 3 iterations)
- 🔍 Research integration
- 🎯 Iterative refinement
- 📊 State persistence

**Agent Pattern**: Loop Agent

**Use Case**: When you need iterative improvement cycles on content creation

---

### 3️⃣ Programmatic ADK Agent
**Path**: `3programatic_Adk_Agent/`

Demonstrates **programmatic agent execution** without web frameworks, perfect for scripts and automation.

**Features**:
- 🐍 Pure Python execution
- ⚡ Async/await patterns
- 🔧 Direct API integration
- 📋 Session management

**Learning Focus**: Understanding ADK's core execution model

```python
async def call_agent_async(query):
    session, runner = await setup_session_and_runner()
    async for event in runner.run_async(...):
        # Process events
```

---

### 4️⃣ E-commerce Shop Assistant
**Path**: `2Ecommerce-shop-assistant/` & `4Ecommerce-shop-assistant/`

Jupyter notebook-based shopping assistant demonstrating ADK in interactive environments.

**Features**:
- 🛍️ Product recommendations
- 💬 Conversational commerce
- 📓 Notebook integration
- 🎯 Customer intent understanding

**Learning Focus**: ADK in Jupyter notebooks and interactive development

---

### 5️⃣ Sustainable Energy Researcher
**Path**: `5Sustainable_energy_researcher/`

A sophisticated **parallel + sequential** workflow for multi-topic research synthesis.

**Features**:
- 🔬 Parallel research execution (3 concurrent researchers)
- 🌍 Topics: Renewable Energy, EVs, Carbon Capture
- 🧠 Intelligent synthesis
- 📊 Structured reporting

**Agent Pattern**: Sequential(Parallel + Merger)

**Architecture**:
```python
SequentialAgent
├── ParallelAgent (Research Phase)
│   ├── RenewableEnergyResearcher
│   ├── EVResearcher
│   └── CarbonCaptureResearcher
└── SynthesisAgent (Merge Phase)
```

**Why This Pattern?**
- ⚡ **Speed**: 3x faster than sequential research
- 🎯 **Specialization**: Each agent focuses on one domain
- 🔄 **Coordination**: Automatic result aggregation
- 📝 **Quality**: Professional synthesis with citations

---

### 6️⃣ Website Info Agent with MCP ⭐
**Path**: `6Website_Info_agent_with_MCP/`

**The crown jewel** of this collection - demonstrates bidirectional MCP integration!

**Features**:
- 🔌 **ADK → MCP Server**: Expose ADK tools as MCP servers
- 🔌 **MCP → ADK Client**: Consume MCP tools in ADK agents
- 🌐 Web page loading via MCP
- 📡 Stdio-based communication

**Components**:

1. **MCP Server** (`website_mcp_server.py`):
   - Wraps ADK's `load_web_page` tool
   - Exposes it via MCP protocol
   - Handles tool discovery and execution

2. **ADK Agent** (`agent.py`):
   - Consumes the MCP server
   - Uses `MCPToolset` for integration
   - Demonstrates client-side MCP usage

**Why MCP Matters**:
- 🔄 Share tools across different AI frameworks
- 🏗️ Build reusable tool ecosystems
- 🌐 Industry-standard protocol
- 🚀 Future-proof your AI infrastructure

**Example Flow**:
```
User Query → ADK Agent → MCP Client
                ↓
            MCP Server
                ↓
        ADK load_web_page Tool
                ↓
        Web Content → Response
```

---

## 🏗️ Architecture Patterns

### Pattern 1: Hierarchical Agents
```python
Parent Agent (Orchestrator)
├── Child Agent 1 (Specialist)
├── Child Agent 2 (Specialist)
└── Child Agent 3 (Specialist)
```
**Use Case**: Task decomposition, specialization

---

### Pattern 2: Loop Agents
```python
LoopAgent (max_iterations=N)
├── Iteration 1 → State Update
├── Iteration 2 → State Update
└── Iteration N → Final Result
```
**Use Case**: Iterative refinement, feedback loops

---

### Pattern 3: Parallel + Sequential
```python
Sequential Pipeline
├── Phase 1: ParallelAgent (Concurrent execution)
└── Phase 2: Merger Agent (Synthesis)
```
**Use Case**: Research, multi-source data gathering

---

### Pattern 4: MCP Integration
```python
ADK Agent → MCPToolset → External MCP Server
    ↓
MCP Server → ADK Tool Wrapper → Actual Tool
```
**Use Case**: Tool sharing, interoperability

---

## 🛠️ Getting Started

### Prerequisites

- **Python**: 3.9 or higher
- **Google Gemini API Key**: [Get it here](https://ai.google.dev/)
- **Package Manager**: `pip` or `uv` (recommended)

---

### Installation

#### Option 1: Using UV (Recommended)
```bash
# Clone the repository
git clone https://github.com/yourusername/adkProjectUd.git
cd adkProjectUd

# Navigate to any project
cd 1youtube_short_script_assistant/youtube_short_script_assistant

# Install with UV
uv pip install -r requirements.txt
```

#### Option 2: Using pip
```bash
# Install dependencies
pip install -r requirements.txt
```

---

### Environment Setup

Create a `.env` file in each project directory:

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

---

## 🎯 Usage Examples

### Example 1: YouTube Shorts Agent

```bash
cd 1youtube_short_script_assistant/youtube_short_script_assistant
python main.py
```

**Expected Output**:
- 🎬 Complete script for a YouTube Short
- 🎨 Visual concepts for each scene
- 📝 Formatted Markdown output

---

### Example 2: Sustainable Energy Researcher

```bash
cd 5Sustainable_energy_researcher
python sustainable_agent.py
```

**What Happens**:
1. 🔄 Three researchers work in parallel
2. 📊 Each researches their topic using Google Search
3. 🧠 Synthesis agent combines findings
4. 📝 Generates structured report with citations

---

### Example 3: Website Info Agent (MCP)

**Step 1**: Start the MCP Server
```bash
cd 6Website_Info_agent_with_MCP/website_info_agent_adk_mcp
python website_mcp_server.py
```

**Step 2**: Run the ADK Client
```bash
python -c "
from agent import root_agent
from google.adk.runners import InMemoryRunner
# ... use the agent
"
```

---

## 📊 Project Comparison

| Project | Agent Type | Complexity | MCP | Google Search | Best For |
|---------|------------|------------|-----|---------------|----------|
| YouTube Shorts (1) | Hierarchical | ⭐⭐ | ❌ | ✅ | Learning sub-agents |
| Loop Agent (2) | Loop | ⭐⭐ | ❌ | ✅ | Iterative workflows |
| Programmatic (3) | Loop | ⭐⭐⭐ | ❌ | ✅ | Script automation |
| E-commerce (4) | Single | ⭐ | ❌ | ❌ | Notebook learning |
| Energy Research (5) | Parallel+Sequential | ⭐⭐⭐⭐ | ❌ | ✅ | Complex orchestration |
| Website MCP (6) | Single | ⭐⭐⭐⭐⭐ | ✅ | ❌ | MCP integration |

---

## 📖 Learn More

### Official Resources
- 📘 [Google ADK Documentation](https://ai.google.dev/adk)
- 🔌 [Model Context Protocol](https://modelcontextprotocol.io/)
- 🤖 [Gemini API Docs](https://ai.google.dev/docs)

### Key Concepts

#### 1. Agent Types
- **LlmAgent**: Single-purpose AI agent
- **LoopAgent**: Iterative execution
- **ParallelAgent**: Concurrent task execution
- **SequentialAgent**: Step-by-step pipeline

#### 2. State Management
```python
output_key="my_result"  # Saves to state['my_result']
# Access in other agents via state
```

#### 3. Tools
- Built-in: `google_search`, `load_web_page`
- Custom: `FunctionTool(your_function)`
- MCP: `MCPToolset(connection_params)`

#### 4. Runners
- **InMemoryRunner**: Local development
- **Runner**: Production with session management

---

## 🎓 Learning Path

### Beginner
1. Start with **E-commerce Assistant** (4) - Simplest example
2. Move to **YouTube Shorts** (1) - Learn sub-agents
3. Try **Loop Agent** (2) - Understand iterations

### Intermediate
4. Study **Programmatic Agent** (3) - Master async patterns
5. Explore **Energy Researcher** (5) - Complex orchestration

### Advanced
6. Deep dive into **MCP Integration** (6) - Build interoperable tools

---

## 🔧 Customization Tips

### Adding Your Own Tools
```python
from google.adk.tools import FunctionTool

def my_custom_tool(param1: str) -> dict:
    # Your logic here
    return {"result": "something"}

agent = LlmAgent(
    tools=[FunctionTool(my_custom_tool)],
    # ... other params
)
```

### Creating Custom Agents
```python
custom_agent = LlmAgent(
    name="MySpecialAgent",
    model="gemini-2.0-flash",
    instruction="Your custom instructions here",
    tools=[...],
    output_key="my_output"
)
```

### Building MCP Servers
See `6Website_Info_agent_with_MCP/` for a complete example of exposing ADK tools via MCP.

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. 🍴 Fork the repository
2. 🌟 Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. 💾 Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. 📤 Push to the branch (`git push origin feature/AmazingFeature`)
5. 🎉 Open a Pull Request

### Ideas for Contributions
- 📝 More example projects
- 🐛 Bug fixes and improvements
- 📚 Documentation enhancements
- 🧪 Test coverage
- 🎨 UI/UX examples with ADK

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 🙏 Acknowledgments

- Google AI team for the incredible ADK framework
- Gemini team for powerful language models
- MCP community for the protocol specification
- Open source community for inspiration

---

## 💬 Questions?

- 📧 Open an issue in this repository
- 💡 Check the [Google ADK Discussions](https://github.com/google/adk)
- 🌟 Star this repo if you find it helpful!

---

<div align="center">

**Built with ❤️ using Google ADK and Gemini**

⭐ Star this repo if you found it helpful!

[Report Bug](https://github.com/yourusername/adkProjectUd/issues) • [Request Feature](https://github.com/yourusername/adkProjectUd/issues)

</div>

# chatoo
LLM interacting with Restful Objects

![Components Overview](./docs/components.svg)

## Install 
```bash
docker-compose up -d --build
```

## OpenSource ToolChain

| Component Role      | Name               | Source                                                    | License          | URL                        |
|---------------------|--------------------|-----------------------------------------------------------|------------------|----------------------------|
| UI-Client           | librechat          | https://github.com/open-webui/open-webui                  | MIT / Custom BSD | https://localhost:3000     |
| LLM Host            | ollama             | https://github.com/ollama/ollama                          | MIT              | http://localhost:11434     |
| LLM (model)         | Phi3               | https://huggingface.co/microsoft/Phi-3-mini-128k-instruct | MIT              | ?                          |
| MCP Client          | mcpo               | x                                                         | ?                | ?                          |
| MCP-OpenAPI Adapter | mcp-openapi-server | https://github.com/ivo-toby/mcp-openapi-server            | MIT              | http://localhost:8000/docs |
| OpenAPI Provider    | causeway app       | x                                                         | Apache 2         | http://localhost:8080      |


# References
* Restful Objects Specification: https://www.restfulobjects.org/spec/1.0/about.html
* Introducing: Restful Objects -> https://www.infoq.com/articles/Intro_Restful_Objects/
* 

----
🧠 **Ollama** is a powerful open-source platform designed to run **large language models (LLMs)** locally on your machine. It’s especially popular among developers and researchers who want privacy, speed, and flexibility without relying on cloud-based AI services.

---

### 🔧 What Ollama Does
- **Runs LLMs locally**: Supports models like LLaMA, Mistral, Phi-3, DeepSeek, and many more
- **Provides a CLI and REST API**: You can interact with models via terminal or integrate them into apps
- **Supports customization**: You can tweak model parameters, prompts, and even import GGUF or Safetensors formats
- **Works offline**: Ideal for secure environments or edge devices

---

### 🖥️ Role in UI Clients
Ollama acts as the **backend engine** for many UI clients:
- UI tools like **Open WebUI**, **LibreChat**, and **Chatbot UI** connect to Ollama to provide a chat interface
- These clients send prompts to Ollama and display the model’s responses
- Developers can build custom frontends using Ollama’s API or CLI

---

### 🔗 Role in LLM Ecosystem
Ollama is a **bridge between raw models and usable applications**:
- It simplifies model management (pull, run, configure)
- Enables experimentation with different models without cloud dependencies
- Supports multimodal models (e.g. LLaVA for image + text)

---

### 🧩 Role in MCP (Model Context Protocol)
Ollama integrates with **MCP clients** to enable tool use and workflow automation:
- Projects like **ollmcp** and **ollama-mcp-client** connect Ollama to MCP servers
- This allows LLMs to call external tools (e.g. shell commands, Git operations) in a structured, safe way
- Supports **Human-in-the-Loop**, **streaming responses**, and **advanced model configuration**

---

### 🧪 Example Use Case
Imagine a developer using Ollama with an MCP client and a UI frontend:
- They run a local LLM like LLaMA 3
- The MCP client lets the model call tools like file search or code execution
- The UI client displays the conversation and tool results interactively

---

Want help setting up a full stack with Ollama, a UI client, and MCP integration? I can walk you through it step-by-step.

Here’s a compact, high‑signal overview of **small, local‑friendly models that actually support tool/function calling** when used through runtimes like Ollama or other inference servers. I’ve focused on models that are practical for your LibreChat + MCP setup and that run well on consumer hardware.

---

# 📊 **Overview Table: Small Models With Tool Support**

| Model | Size | Tool / Function Calling | Typical Hardware Requirements | License |
|------|------|--------------------------|-------------------------------|---------|
| **Llama 3.1 Instruct** | 8B | ✔ Fully supported (structured JSON, tools) | 8–12 GB RAM (CPU) or 6–8 GB VRAM (GPU) | Meta Llama 3.1 Community License |
| **Qwen2.5 Instruct** | 7B | ✔ Very strong tool calling | 8–12 GB RAM or 6–8 GB VRAM | Apache 2.0 |
| **Qwen2.5 Instruct** | 14B | ✔ Excellent tool calling | 16–20 GB RAM or 12–16 GB VRAM | Apache 2.0 |
| **Gemma 2 Instruct** | 9B | ✔ Good structured output & tools | 12–16 GB RAM or 8–10 GB VRAM | Gemma License (permissive but not fully open) |
| **Mistral Nemo** | 12B | ✔ Reliable tool calling | 16–20 GB RAM or 12–16 GB VRAM | Apache 2.0 |
| **Llama 2 Chat** | 7B | ✔ Partial tool support (works, but less reliable) | 8–12 GB RAM or 6–8 GB VRAM | Llama 2 Community License |
| **Mistral Instruct** | 7B | ✔ Partial tool support | 8–12 GB RAM or 6–8 GB VRAM | Apache 2.0 |

---

# 🧠 Notes on Practical Use

### ✔ Best overall small model for tools
**Qwen2.5 7B Instruct**
- Apache 2.0
- Very strong JSON adherence
- Runs fast on modest hardware
- Excellent for MCP tool workflows

### ✔ Best balance of quality + size
**Llama 3.1 8B Instruct**
- Great reasoning
- Good tool calling
- Slightly heavier than Qwen2.5 7B

### ✔ Best “open‑source” licensing
**Qwen2.5 (7B/14B)** and **Mistral Nemo**
- Both Apache 2.0
- No usage restrictions

### ✔ Models to avoid for tool calling
- Phi‑3 (all sizes)
- Phi‑2
- Base models (non‑instruct)
- Most GGUF conversions without tool metadata

These will trigger the error you saw in LibreChat.

---

If you want, I can help you pick the best model for your exact hardware and workload so your LibreChat + MCP setup runs smoothly.

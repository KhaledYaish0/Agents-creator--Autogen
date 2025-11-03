# 🧠 Big Autogen Project – Agent Generator Experiment

## 📜 Overview
This experimental project explores **autonomous multi-agent generation** using the **AutoGen distributed runtime**.  
A *Creator Agent* dynamically spawns and registers new agents, each capable of independently generating business ideas, refining them collaboratively, and saving the results as Markdown files.  

The goal is to simulate an ecosystem of self-replicating AI agents — educational, entertaining, and slightly chaotic.

---

## ⚙️ How It Works
1. **Creator Agent** dynamically writes Python code for new agents.  
2. Each new agent registers itself to the **distributed runtime (gRPC Host/Worker)**.  
3. The agents then communicate and exchange ideas.  
4. Every agent produces one unique idea → saved as `ideaX.md`.

---

## 💡 Project Nature
Inspired by *AutoGen’s Day 5: Creating Autonomous Agents*, the project is designed to be:
- 🎓 **Educational** – demonstrates distributed agent runtimes and autonomous code generation.  
- 🎭 **Entertaining** – every run creates different personalities and ideas.  
- 😎 **Edgy** – unpredictable outcomes by design.  
- 🧩 **Uncommercial (but with a twist)** – not meant for production; purely experimental.  
- 🎲 **Unreliable** – agents may produce strange or unstable outputs (intentionally).  

---

## ⚖️ Pros & Cons

### ✅ Advantages
- Hands-on demonstration of **AutoGen’s distributed runtime** (host/worker).  
- Dynamic **code generation and registration** of agents.  
- Encourages experimentation with **autonomous multi-agent systems**.  
- Easy to extend — just tweak prompts or agent logic.

### ⚠️ Risks / Limitations
- ❗ **Unreliable output:** agents might create invalid or nonsensical code.  
- 🧩 **High variance:** results differ across runs.  
- 🧠 **Unbounded creativity:** some generated agents could behave unexpectedly.  
- 💾 **Local file generation:** untested for remote or multi-machine deployments.  
- 🧱 **Experimental:** not optimized for stability or commercial use.

---

## 🧠 Example Use
```bash
python world.py
```
This launches the host and worker runtimes, creates multiple agents (e.g. `agent1.py` → `agent20.py`), and saves their ideas in Markdown files.

---

## 🧰 Stack
- Python 3.10+
- AutoGen / LangGraph (Distributed Runtime)
- OpenAI API (GPT-4o-mini)
- asyncio + gRPC for inter-agent communication

---

## ⚠️ Disclaimer
This is a **research/learning** project.  
Agents are self-generating and may produce unpredictable code or text.  
Use at your own risk.

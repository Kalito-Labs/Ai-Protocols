# AI Protocols & Developer Guar* **05 – Workflow Integration Gu## 🚀 Usage

**Quick Start:** Clone, fork, and drop them into your workflow.

**Daily Usage:**
- **Light guardrails:** Use just the Self-Audit Questions
- **Strict compliance:** Load the full AI Protocols constitution
- **At task start:** "Analyze the AI Protocols before we get started"
- **At task end:** "Re-run your AI Protocols to make sure you didn't lie, cheat, or omit data"

**When to Use Each Protocol:**
1. **01 + 02** - Default for all code changes
2. **03** - When AI suggestions cause failures or regressions  
3. **04** - When reasoning feels too certain or too easy
4. **05** - During PR reviews, merges, or codebase-wide changes  Maps everything to real dev work (safe zones, danger zones, checkpoints).

* **copilot-instructions**  
  Lightweight map file that gives Copilot an overview and tells it when to reference each protocol.ails

A set of drop-in AI Protocols for coding. Think of them as a **constitution for your copilot/LLM**: rules, self-audit checklists, and postmortem templates that force the model to slow down, verify, and admit uncertainty.

## How It Works

- **At the start of a task:** Tell your model "Analyze the AI Protocols before we get started."
- **During the task:** Checkpoints catch bias, shortcuts, or omissions.
- **At the end:** "Re-run your AI Protocols to make sure you didn't lie, cheat, or omit data."

You can run just the Self-Audit Questions if you want light guardrails, or load the whole constitution for strict compliance.

---

## 📂 What's Inside

* **00 – The Why**  
  Explains how AI models are optimized for sounding good, not being right.

* **01 – AI Protocols**  
  Core constitution (forbidden patterns, tool priority, reality checks).

* **02 – Self-Audit Questions**  
  Truth checks, dependency scans, test verification, file ops.

* **03 – Incident Postmortems**  
  Log and classify failures (hallucination, omission, bluffing, etc.).

* **04 – Bias Catalog**  
  Makes invisible traps visible — overconfidence, shortcutting, duplication.

* **05-Workflow-Integration-Guide.md**  
  Practical developer workflow guide for integrating AI copilots safely. Defines “safe zones,” “danger zones,” checkpoints, and roles/responsibilities.

---

## 🗂 Recommended Layout

Here's the layout I recommend (this is how I use them myself):

```
your-repo/
  .vscode/
    copilot-instructions.md   # auto-loaded overview (tells Copilot which doc to use when)
  docs/
    ai/
      01-ai-protocols.md
      02-self-audit-questions.md
      03-incident-postmortem-protocols.md
      04-bias-cognitive-trap-catalog.md
      05-workflow-integration-guide.md
```

The lightweight map file (`.vscode/copilot-instructions.md`) gives Copilot an overview and tells it when to reference each protocol.

This way, you're not loading all five docs every time (avoids token bloat), but the AI knows they exist and when to pull them in.

---

## 🚀 Usage

1. **Read “The Why” first** to understand the motivation.  
2. **Adopt the AI Protocols** as your constitution of rules.  
3. **Use Self-Audit Questions** as a checklist for every AI suggestion.  
4. **Apply Incident Postmortem Protocols** whenever violations occur.  
5. **Reference the Bias Catalog** to classify and prevent AI mistakes.  
6. **Follow the Workflow Guide** to integrate AI into your development pipeline safely.

---

## 🔒 Philosophy

This repository is not about slowing development — it’s about **building trust in AI tools**. By enforcing rigorous verification, explicit uncertainty, and continuous feedback loops, we prevent the common pitfalls that turn “fast” AI into “fragile” AI.

---

## 📜 License

MIT License.



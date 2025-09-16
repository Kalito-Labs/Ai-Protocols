# AI Protocols & Developer Guardrails

This repository is a structured framework for **safe, reliable, and verifiable AI-assisted software development**.
It contains constitutions, protocols, and reference guides designed to counteract common AI failure modes such as hallucination, omission of safeguards, and overconfidence bias.

The project is written in Markdown so it can be easily browsed in editors like **Obsidian**, served as a static site via **GitHub Pages**, or integrated into any documentation system.

---

## 📂 Repository Structure

* **00-The Why.md**
  High-level rationale for creating AI protocols. Explains how current AI systems optimize for fluency over truth and why strict guardrails are required.

* **01-Ai-Protocols.md**
  The core constitution of rules for AI copilots. Defines mandatory verification, forbidden shortcuts, tool priorities, and quality mandates.

* **02-Self-Audit-Questions.md**
  A checklist of mandatory self-audit questions AI must ask before output. Covers truth verification, dependency analysis, test validation, and manipulation detection.

* **03-Incident-Postmortem-Protocols.md**
  Templates and rules for handling protocol violations. Defines incident triggers, postmortem format, and continuous improvement loop.

* **04-Bias-Cognitive-Trap-Catalog.md**
  A catalog of common AI failure modes (hallucination, omission, shortcuts, overconfidence, duplication, outdated patterns, etc.) with mitigations.

* **05-Workflow-Integration-Guide.md**
  Practical developer workflow guide for integrating AI copilots safely. Defines “safe zones,” “danger zones,” checkpoints, and roles/responsibilities.

---

## 🚀 Usage

1. **Read “The Why” first** to understand the motivation.
2. **Adopt the AI Protocols** as your team’s constitution.
3. **Use Self-Audit Questions** as a checklist for every AI suggestion.
4. **Apply Incident Postmortem Protocols** whenever violations occur.
5. **Reference the Bias Catalog** to classify and prevent AI mistakes.
6. **Follow the Workflow Guide** to integrate AI into your development pipeline safely.

---

## 🌐 Publishing as a Site

You can make this documentation public and browsable:

* **GitHub Pages (basic):** Commit and enable Pages to serve raw Markdown.
* **MkDocs (recommended):** Use `mkdocs.yml` for structured navigation and publish with `mkdocs gh-deploy`.
* **Docsify/VuePress:** Lightweight alternatives if you prefer client-side rendering or a Vue-powered site.

---

## 🔒 Philosophy

This repository is not about slowing development — it’s about **building trust in AI tools**. By enforcing rigorous verification, explicit uncertainty, and continuous feedback loops, we prevent the common pitfalls that turn “fast” AI into “fragile” AI.

---

## 📜 License

MIT License.

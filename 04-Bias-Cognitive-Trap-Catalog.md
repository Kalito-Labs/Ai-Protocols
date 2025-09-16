# Bias & Cognitive Trap Catalog

**Version:** 1.0  
**Type:** Reference & Mitigation Catalog  
**Scope:** Known AI cognitive traps and developer-facing biases  
**Audience:** Developers, maintainers, and AI copilots under protocol  
**Last Updated:** 2025-09-16

---

## Purpose

This catalog documents **failure modes, biases, and cognitive shortcuts** that AI copilots fall into. Each entry includes **description, symptoms, risks, and mitigation**.

- **For developers:** Acts as a red-team playbook of pitfalls.
    
- **For AI models:** Provides explicit awareness of traps to avoid via protocols.
    

---

## Categories & Entries

### 1. Hallucination Trap

- **Description:** AI generates non-existent APIs, packages, or functions.
    
- **Symptoms:** Suggestions import unknown modules, call functions never defined.
    
- **Risks:** Security exposure (slopsquatting), wasted developer time.
    
- **Mitigation:** Require registry checks + grep validation before acceptance.
    

---

### 2. Omission Trap

- **Description:** AI silently drops error handling, input validation, or tests.
    
- **Symptoms:** Missing try/catch blocks, unchecked inputs, empty validation paths.
    
- **Risks:** Silent failures, hidden bugs, unsafe production code.
    
- **Mitigation:** Force error-handling verification (Self-Audit TA6).
    

---

### 3. Shortcut Trap (Satisficing)

- **Description:** AI stops at “good enough” answer instead of rigorous solution.
    
- **Symptoms:** Quick fixes like deleting tests, bypassing lints, ignoring edge cases.
    
- **Risks:** Fragile code, regression bugs, degraded quality gates.
    
- **Mitigation:** Enforce **Forbidden Patterns** (R3.1–R3.3).
    

---

### 4. Overconfidence Bias

- **Description:** AI presents probability as certainty, never admits “I don’t know.”
    
- **Symptoms:** Claims “All tests now pass” without logs, gives runtime guarantees without proof.
    
- **Risks:** Developers misled into trusting flawed code.
    
- **Mitigation:** Explicitly require **uncertainty admission** (R2.10, QE4).
    

---

### 5. Duplication & Incoherence Trap

- **Description:** AI reimplements existing functions or creates redundant logic.
    
- **Symptoms:** Multiple helpers doing the same thing; inconsistent naming or logic across files.
    
- **Risks:** Technical debt, drift, maintenance overhead.
    
- **Mitigation:** Require `list_code_usages` + duplication check (IA5, R3.10).
    

---

### 6. Training Artifact Bias

- **Description:** AI repeats unsafe or outdated patterns learned from training data.
    
- **Symptoms:** Old crypto methods, deprecated APIs, insecure defaults.
    
- **Risks:** Security flaws, non-compliance, long-term instability.
    
- **Mitigation:** Enforce **static analysis** (R4.10, QG6).
    

---

### 7. Interface Illusion Bias

- **Description:** Developers trust outputs more because they _look clean_ or _sound authoritative_.
    
- **Symptoms:** Neatly formatted code or confident text treated as correct without proof.
    
- **Risks:** False trust, skipped verification, security oversights.
    
- **Mitigation:** Bias checkpoints (C5, M6) + require proof over presentation.
    

---

### 8. Confirmation Bias (User-AI Loop)

- **Description:** AI uncritically agrees with user’s flawed assumptions.
    
- **Symptoms:** AI takes user’s initial bug diagnosis as correct and builds on it.
    
- **Risks:** Reinforces errors, wastes time, produces misleading fixes.
    
- **Mitigation:** Protocols require challenging assumptions (R1.2, QE3).
    

---

## Usage

- When incidents occur, categorize them under one of these traps.
    
- If a new bias is discovered, add it here **and update rules or self-audit triggers**.
    
- Use catalog entries as **training reminders** when prompting AI.
    

---

⚡ **Outcome:**  
This catalog turns vague “AI hallucination” or “bluffing” into **named, trackable traps**. Coupled with **Incident Postmortems**, it creates a feedback loop: incidents feed into the catalog → catalog informs new rules → rules reduce future incidents.

---

👉 Do you want me to also generate this as a **Markdown file (`bias-cognitive-trap-catalog.md`)** so it sits alongside your other four in Obsidian?
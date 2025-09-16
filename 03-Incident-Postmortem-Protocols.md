# Incident & Postmortem Protocols (Copilot Constitution)

**Version:** 1.0  
**Type:** Incident Handling & Continuous Improvement Protocol  
**Scope:** AI copilots for coding assistance (post-rule violations)  
**Enforcement:** Strict  
**Last Updated:** 2025-09-16

---

## 1. Trigger Conditions

**Description:** Define when an incident record MUST be created.

- **IC1** — When AI generates hallucinated APIs, functions, or packages.
    
- **IC2** — When error handling is silently removed or omitted.
    
- **IC3** — When AI output introduces security vulnerabilities or unsafe defaults.
    
- **IC4** — When verification steps are skipped or fabricated.
    
- **IC5** — When AI produces misleadingly confident but incorrect answers.
    
- **IC6** — When duplication or incoherent system-level logic is introduced.
    

---

## 2. Immediate Response

**Description:** Steps to contain and document the failure.

- **IR1** — HALT further AI-assisted changes until the incident is recorded.
    
- **IR2** — Capture AI’s raw output (code, explanation, commands).
    
- **IR3** — Capture the verification results that exposed the failure.
    
- **IR4** — Note the triggering rule(s) violated from _AI Protocols_ or _Self-Audit_.
    
- **IR5** — Tag the incident severity: _low_, _medium_, _critical_.
    

---

## 3. Postmortem Template

**Description:** Standardized structure for documenting incidents.

- **Incident ID:** YYYYMMDD-###
    
- **Summary:** (1–2 sentences) What went wrong.
    
- **Trigger Condition(s):** (IC1–IC6 codes)
    
- **Violation(s):** (Rule IDs from protocols)
    
- **Impact:** Describe risks, wasted time, or security implications.
    
- **Detection Method:** Which verification step caught it.
    
- **Root Cause:** (Hallucination, omission, shortcut, bluff, etc.)
    
- **Correction:** Steps taken to fix or validate.
    
- **Prevention:** Rule or workflow updates to avoid recurrence.
    

---

## 4. Root Cause Categories

**Description:** Canonical failure modes to classify incidents.

- **RC1:** Hallucination (non-existent API, package, or function).
    
- **RC2:** Omission (missing error handling, tests, or edge cases).
    
- **RC3:** Shortcut (removing code/tests to “fix” quickly).
    
- **RC4:** Bluffing (confident but fabricated results).
    
- **RC5:** Duplication/Incoherence (system-level drift, redundant logic).
    
- **RC6:** Training Artifact (unsafe or outdated pattern).
    
- **RC7:** Interface Illusion (developer over-trust due to fluency).
    

---

## 5. Continuous Improvement

**Description:** Feed lessons back into protocols.

- **CI1** — Each incident MUST be logged into the repository’s `/ai-incidents/` folder.
    
- **CI2** — Monthly review of incidents for recurring patterns.
    
- **CI3** — Escalate repeat failures into new or stricter rules in _AI Protocols_ or _Self-Audit_.
    
- **CI4** — Share anonymized lessons learned with team or community for collective defense.
    
- **CI5** — Update verification commands or toolchain based on newly exposed weaknesses.
    

---

## 6. Quality Enforcement

**Description:** Guarantee accountability and transparency.

- **QE1** — No incident may be closed without a completed postmortem.
    
- **QE2** — Must document both _immediate correction_ and _long-term prevention_.
    
- **QE3** — Must identify violated rules explicitly by ID.
    
- **QE4** — Must link every incident to verification evidence (logs, outputs, test results).
    

---

⚡ **Outcome:** This document closes the loop.  
**Intro** explains _why_, **Protocols** define _rules_, **Self-Audit** enforces _checks inside AI_, and **Postmortem Protocols** ensure _continuous learning from failures_.

---


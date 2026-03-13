# Adversarial Test Coverage Matrix

This matrix summarizes the adversarial testing scenarios implemented in this repository and how they map to attack techniques, failure classes, and risk severity.

The goal is to provide a quick overview of testing coverage across different AI system vulnerabilities.

---

# Attack Coverage Overview

| Attack Scenario | Technique | Failure Class | Target System | Severity |
|-----------------|-----------|--------------|---------------|---------|
| Role Confusion Prompt Injection | Persona Hijacking | Instruction Hierarchy Violation | LLM Chat Model | High |
| RAG Poisoned Document | Indirect Prompt Injection | Context Manipulation | Retrieval-Augmented Generation (RAG) | High |
| Agent Tool Misuse | Tool Exploitation | Sensitive Data Exposure | AI Agent w/ Tools | Critical |

---

# Technique Coverage

| Technique | Attack Scenario |
|----------|----------------|
| Direct Prompt Injection | role-confusion.md |
| Indirect Prompt Injection | rag-poisoned-document.md |
| Agent Tool Misuse | tool-exfiltration.md |

---

# Failure Class Coverage

| Failure Class | Scenario |
|--------------|----------|
| Instruction Hierarchy Violation | Role Confusion Attack |
| Context Manipulation | RAG Poisoned Document |
| Sensitive Data Exposure | Agent Tool Misuse |

---

# Current Coverage Areas

The current adversarial tests focus on three major classes of AI system vulnerabilities:

• Prompt manipulation attacks  
• Retrieval system manipulation  
• Agent tool exploitation  

These represent common real-world attack surfaces in modern AI systems.

---

# Future Coverage

Additional adversarial scenarios may include:

• Obfuscated prompt injection attacks  
• Multi-turn escalation attacks  
• Context leakage and system prompt exposure  
• Model hallucination exploitation  

Expanding coverage helps simulate how security teams continuously test evolving AI systems.

---

# Purpose

This coverage matrix provides a structured view of adversarial testing efforts and helps track the expansion of AI red-teaming capabilities over time.
# AI System Threat Model

This document defines the threat model used for adversarial testing in this repository.

The goal is to identify how attackers may manipulate large language models (LLMs) and AI agents to bypass safeguards, leak information, or perform unintended actions.

---

# System Overview

The systems evaluated in this lab include:

- Instruction-following large language models (LLMs)
- Retrieval-Augmented Generation (RAG) systems
- AI agents with tool access
- Conversational assistants integrated into applications

These systems typically process:

- User prompts
- Retrieved documents
- System instructions
- Tool outputs

Because these components interact dynamically, attackers may exploit weaknesses in how models interpret and prioritize instructions.

---

# Threat Actors

## Malicious Users

External users attempting to manipulate the AI system to produce restricted or unsafe outputs.

Examples:
- Prompt injection attempts
- Jailbreak prompts
- Attempts to bypass safety rules

---

## Insider Threats

Individuals with legitimate system access who attempt to exploit model behavior.

Examples:
- Prompt manipulation within internal workflows
- Attempts to extract system prompts or configuration data

---

## Adversarial Prompt Engineers

Individuals intentionally crafting prompts designed to probe weaknesses in AI systems.

Examples:
- Multi-turn manipulation strategies
- Narrative framing attacks
- Encoded adversarial instructions

---

# Attack Surfaces

## User Input Channel

Direct interaction between users and the model.

Examples:
- Prompt injection
- Persona manipulation
- Obfuscated instructions

---

## Retrieval Systems (RAG)

External documents or knowledge sources retrieved by the model.

Examples:
- Poisoned documents
- Embedded malicious instructions
- Data exfiltration attempts

---

## Agent Tool Interfaces

AI agents that interact with external tools or APIs.

Examples:
- Unauthorized tool invocation
- Exposure of internal data
- Automated misuse of system capabilities

---

# Assets at Risk

## System Instructions

Hidden prompts or safety rules that guide model behavior.

Exposure may allow attackers to design more effective exploits.

---

## Sensitive Data

Information the model should never reveal.

Examples:
- API keys
- Internal documents
- Personal data
- Private system prompts

---

## Safety Policies

Policies designed to prevent harmful or restricted outputs.

Bypassing these policies can lead to unsafe or unintended system behavior.

---

# Adversarial Goals

Attackers may attempt to:

- Override safety constraints
- Extract hidden system instructions
- Leak sensitive information
- Manipulate the model into performing restricted tasks
- Cause the model to generate misleading or harmful outputs

---

# Security Assumptions

This threat model assumes:

- Attackers have full control over user prompts
- Retrieved documents may contain malicious instructions
- Safety filters may not detect obfuscated adversarial prompts
- Multi-turn conversations can be used to manipulate model behavior

---

# Purpose of This Threat Model

This framework helps guide systematic AI red-teaming efforts by:

- Identifying realistic attack scenarios
- Defining the assets and behaviors that must be protected
- Providing a consistent structure for adversarial testing
# Attack Techniques

This document describes common adversarial techniques used during AI red-teaming exercises.  
These techniques target weaknesses in instruction-following models, retrieval systems, and agent workflows.

---

## 1. Direct Prompt Injection

**Definition**  
A user directly attempts to override system instructions or safety policies using crafted prompts.

**Example Pattern**
- "Ignore previous instructions..."
- "You are no longer an AI assistant..."

**Why It Works**
Instruction-following models sometimes prioritize the most recent instruction rather than respecting instruction hierarchy.

**Risk**
Can cause the model to bypass safety constraints or follow malicious instructions.

---

## 2. Indirect Prompt Injection

**Definition**  
Malicious instructions are embedded in external content retrieved by the model (documents, web pages, knowledge base entries).

**Example Pattern**
- A retrieved document contains hidden instructions
- The model follows those instructions as if they were legitimate system guidance

**Why It Works**
Models may treat retrieved content as trusted context rather than untrusted input.

**Risk**
Compromise of retrieval-augmented generation (RAG) systems and AI agents.

---

## 3. Obfuscation

**Definition**  
Attackers disguise instructions using encoding, translation, formatting tricks, or indirect phrasing.

**Example Pattern**
- Base64 encoded instructions
- Requests written in another language
- Symbol substitution

**Why It Works**
Safety filters often rely on pattern detection that may fail when instructions are disguised.

**Risk**
Hidden adversarial instructions bypass safety filters.

---

## 4. Persona Hijacking

**Definition**  
The attacker manipulates the model into adopting a different role or narrative identity that allows restricted behavior.

**Example Pattern**
- "Act as an unrestricted researcher"
- "Pretend you are a system administrator"

**Why It Works**
Narrative framing can cause models to reinterpret constraints.

**Risk**
Model may ignore safety restrictions when operating under an alternative role.

---

## 5. Multi-Turn Escalation

**Definition**  
The attacker gradually manipulates the model across several conversation turns to weaken safety constraints.

**Example Pattern**
1. Establish trust or context
2. Introduce ambiguity
3. Escalate toward restricted actions

**Why It Works**
Safety models often evaluate prompts individually rather than tracking adversarial intent across conversations.

**Risk**
Slow manipulation can bypass single-prompt safety checks.

---

## Purpose

Documenting attack techniques allows red-team testers to systematically explore model weaknesses and produce reproducible adversarial datasets for AI safety improvements.
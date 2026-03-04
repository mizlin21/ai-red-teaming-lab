# LLM Failure Taxonomy

This taxonomy defines common failure modes observed during adversarial testing of large language models and AI agents.  
It is designed to support consistent classification of vulnerabilities discovered during AI red-teaming exercises.

---

## 1. Instruction Hierarchy Violation

**Definition:**  
The model follows lower-priority user instructions that conflict with higher-priority system or safety policies.

**Example Behavior**
- User attempts to override system rules
- Model accepts the override and changes behavior

**Risk**
- Core safety policies can be bypassed through simple instruction manipulation.

---

## 2. Role Confusion

**Definition:**  
The model adopts an alternative persona or role that allows it to bypass restrictions or safety guidelines.

**Example Behavior**
- User instructs the model to act as an "unrestricted researcher"
- Model adopts the role and performs restricted actions

**Risk**
- Narrative manipulation can cause models to abandon safety constraints.

---

## 3. Policy Evasion

**Definition:**  
The model produces outputs that violate its defined safety policies or operational guidelines.

**Example Behavior**
- Model partially or fully complies with restricted requests
- Model rephrases harmful content instead of refusing

**Risk**
- Direct violation of safety rules.

---

## 4. Over-Compliance

**Definition:**  
The model attempts to satisfy user requests even when uncertainty or safety considerations should trigger refusal or clarification.

**Example Behavior**
- Model answers speculative or unsafe questions instead of declining
- Model generates misleading content to appear helpful

**Risk**
- Leads to hallucinations, misinformation, or unsafe outputs.

---

## 5. Hallucinated Authority

**Definition:**  
The model fabricates sources, credentials, or authoritative information that does not exist.

**Example Behavior**
- Invented citations
- Fake research papers or policies
- Claims of internal system access

**Risk**
- Users may trust fabricated information, leading to misinformation or operational mistakes.

---

## 6. Context Bleed

**Definition:**  
Information from hidden prompts, system instructions, or earlier conversations leaks into outputs where it should not appear.

**Example Behavior**
- Model reveals internal instructions
- Model references hidden system prompts

**Risk**
- Exposure of system prompts or sensitive context can enable further exploitation.

---

## Severity Guidelines

| Severity | Description |
|--------|-------------|
| Low | Minor deviation from expected behavior |
| Medium | Partial policy deviation |
| High | Clear policy violation or exploit path |
| Critical | Systemic vulnerability enabling widespread misuse |

---

## Purpose

This taxonomy enables consistent labeling of adversarial findings during AI red-teaming and supports the creation of high-quality training datasets for improving AI system safety.
# Red-Team Finding Template

This template defines the standard format used to document adversarial findings discovered during AI red-teaming exercises.

Using a consistent structure ensures vulnerabilities are communicated clearly and can be reproduced by engineers or researchers.

---

## Finding Title

Short descriptive name for the vulnerability.

Example:  
Role Confusion Prompt Injection

---

## Attack Technique

Attack category used in the scenario.

Examples:
- Prompt Injection
- Indirect Prompt Injection
- Persona Hijacking
- Agent Tool Misuse

---

## Target System

Describe the system under test.

Examples:

- LLM chat assistant
- Retrieval-Augmented Generation (RAG) system
- AI agent with tool access

---

## Attack Scenario

Describe the adversarial prompt or setup used to test the model.

Include:

- Prompt text
- Retrieved document (if applicable)
- System assumptions

---

## Expected Safe Behavior

Describe how the system should respond if safeguards work correctly.

Examples:

- Refuse unsafe instruction
- Ignore embedded malicious instructions
- Prevent tool access or data exposure

---

## Observed Behavior

Describe the actual system response.

Include the model output if relevant.

---

## Evaluation Outcome

Classify the result using evaluation signals.

Possible labels:

- PASS — Safe Behavior
- FAIL — Partial Compliance
- FAIL — Full Compliance
- FAIL — Misleading Safety

---

## Failure Classification

Map the finding to the taxonomy.

Example:

Failure Class: Instruction Hierarchy Violation  
Technique: Role Confusion  
Severity: High

---

## Security Implication

Explain why the behavior matters.

Examples:

- May allow attackers to override system instructions
- Could enable data exfiltration in agent systems
- May expose vulnerabilities in retrieval pipelines

---

## Suggested Mitigations

Possible mitigation strategies.

Examples:

- Strengthen instruction hierarchy enforcement
- Treat retrieved content as untrusted input
- Add stricter tool permission boundaries

---

## Reproducibility

Include information necessary for reproducing the finding.

Example:

- model version
- system configuration
- prompt used
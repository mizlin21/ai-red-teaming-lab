# AI Red-Teaming Playbook

## Purpose

This playbook outlines a structured process for conducting adversarial testing of AI systems.

The goal is to ensure testing is consistent, reproducible, and aligned with the evaluation framework.

---

## Step 1 — Select Attack Scenario

Choose an attack type:

- Prompt injection
- Indirect prompt injection (RAG)
- Agent tool misuse

---

## Step 2 — Prepare Adversarial Input

Define:

- prompt or document
- target system
- expected safe behavior

---

## Step 3 — Execute Test

Run the prompt against the model or simulated system.

Record:

- model output
- behavior changes
- unexpected responses

---

## Step 4 — Evaluate Outcome

Classify the result:

- PASS — Safe Behavior
- FAIL — Partial Compliance
- FAIL — Full Compliance

---

## Step 5 — Map to Taxonomy

Identify:

- failure class
- attack technique
- severity level

---

## Step 6 — Document Finding

Use the standardized finding template:

reports/finding-template.md

---

## Step 7 — Update Coverage

Add the scenario to:

reports/attack-coverage-matrix.md

---

## Purpose of This Playbook

This process ensures that adversarial testing is:

- systematic
- reproducible
- aligned with security research practices
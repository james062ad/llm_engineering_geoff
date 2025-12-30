# Geoff’s LLM Engineering Notes

## 🧭 Executive Framing (for Clients & Employers)

This repository documents my hands-on execution of modern LLM engineering techniques, with a deliberate focus on **evidence-first reasoning, legal and regulatory defensibility, and ethical use in high-stakes domains**. Rather than presenting polished demos, it captures the process by which LLM systems are inspected, stress-tested, and adapted for real-world use cases such as ASX 300 annual report analysis, governance and risk assessment, and privilege-sensitive legal workflows. Each notebook is executed, annotated, and varied to expose assumptions, failure modes, and compliance considerations, creating a transparent audit trail of both technical decisions and reasoning. The result is a practical demonstration of how LLM capabilities can be responsibly integrated into investigative, advisory, and decision-support contexts where accuracy, traceability, and professional judgment matter.

---

## 📌 How I Use This Repository (Post-Lesson Workflow)

This repository is not a passive record of course completion.  
It is a **working lab notebook** that captures execution, inspection, and variation of each lesson.

After **every lesson or section**, I follow the steps below.

---

### ✅ Required steps after each lesson / section

#### 1. Re-run the notebook myself
- Execute all cells locally in Jupyter
- Confirm I understand:
  - Inputs
  - Outputs
  - Data structures
  - Failure modes

---

#### 2. Create an explicit “my version”
I **never modify the instructor notebook silently**.

I do **one** of the following:

- Duplicate the notebook  
  day1.ipynb → instructor  
  day1_geoff.ipynb → my exploration

- OR add clearly marked sections such as:  
  # --- GEOFF: EXPLORATION ---

This makes authorship and intent unambiguous.

---

#### 3. Inspect internals (mandatory)
I add inspection code such as:
- print() or pprint() of raw objects
- Token usage and response metadata
- Intermediate values (before/after transforms)

The goal is **understanding structure**, not just results.

---

#### 4. Introduce at least one variation
Each lesson includes **at least one deliberate variation**, for example:
- Modify prompts or system instructions
- Change parameters (temperature, model, chunking, etc.)
- Swap in a different data source
- Add basic validation or error handling
- Run against a real-world analogue

---

#### 5. Write a short reflection
In a Markdown cell or notes.md, I record:
- What surprised me
- What broke
- What assumptions were wrong
- What would matter in a production, legal, regulatory, or compliance context

This reflection is short, factual, and technical.

---

#### 6. Commit with intent
Each lesson ends with a commit such as:

    git commit -m "Week 1: inspected response objects and added prompt variations"

The commit history is treated as an **audit trail of learning**.

---

## 🧠 Domain-Specific Extensions (Legal / ASX / Evidence / Compliance)

Where possible, I contextualise lessons using:
- ASX 300 annual reports and notes to the accounts
- Governance, remuneration, risk, and ESG disclosures
- Legal professional privilege and evidentiary boundaries
- Regulatory, investigative, and advisory analysis use-cases
- Compliance and ethics considerations, including:
  - Explainability and traceability
  - Risk of hallucination or overreach
  - Appropriate use of AI-generated insights in regulated settings

The aim is not to build a product here, but to:

Translate general LLM techniques into legally, ethically, and regulatorily grounded reasoning problems.

---

## 🤖 Prompt I Use After Each Lesson (Reusable)

After completing a lesson, I paste the following prompt into ChatGPT:

I have just completed a lesson involving the following techniques:

[briefly describe the lesson: e.g. prompt construction, web scraping, RAG, response parsing]

Context:
- I am a lawyer and AI engineer
- I work with ASX 300 annual reports, governance disclosures, and financial notes
- I am building towards an evidence-first, privilege-aware, and compliance-conscious reasoning platform

Please suggest:
1. 3–5 concrete follow-up experiments I could run in Jupyter
2. At least one variation that tests legal, evidentiary, compliance, or ethical edge cases
3. One failure mode I should deliberately provoke and observe
4. One extension that would matter in a real investigative, regulatory, or advisory workflow

Constraints:
- Experiments should be small, inspectable, and notebook-friendly
- Prefer transparency, traceability, and defensibility over cleverness

I then implement **at least one** of the suggested extensions and commit it.

---

## 🎯 Guiding principle

This repository is designed to show that I can:
- Execute LLM systems
- Inspect and reason about their behaviour
- Adapt techniques to regulated, high-stakes domains
- Incorporate compliance and ethical considerations into technical design
- Work in a reproducible, auditable manner

It is intentionally **process-heavy and product-light**.

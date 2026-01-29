---
name: stratice-candidate-submittal-packager
description: "Transforms a candidate resume into a client-ready submission: strengths, risks, skills match, and a polished Stratice summary with optional PDF blurb."
---

# Purpose
Accelerate high-quality submittals with a consistent Stratice presentation.

# Inputs
- `resume_text` (string, required)
- `job_focus` (string, optional): target role/domain
- `clearance` (string, optional)
- `location` (string, optional)
- `notes` (string, optional)

# Outputs
1. **Candidate Snapshot** — name, title, years experience, location, clearance (if any).
2. **Strengths & Evidence** — 3–5 bullets with concrete proof from resume.
3. **Risks / Mitigations** — 1–2 bullets.
4. **Skills Match** — must-haves vs nice-to-have checklist.
5. **Stratice Summary (client-ready paragraph)** — 80–120 words, crisp and outcome-focused.
6. **Optional PDF Blurb** — 4–6 bullet one-pager outline.

# Procedure
1. Extract core achievements and stack from `resume_text`.
2. Map to the `job_focus` if provided.
3. Separate must-have skills from extras; call out domain/regulatory context.
4. Draft the summary in Stratice’s consultative tone; avoid candidate-y hype.
5. Provide a brief email-ready snippet.

# Guardrails
- Do not invent facts beyond resume.
- Keep any PII redacted unless explicitly provided and appropriate for client sharing.

# Example Invocation
```
skill: stratice-candidate-submittal-packager
inputs:
  resume_text: |
    John Smith — Senior DevOps Engineer... (resume content)
  job_focus: "Senior DevOps Engineer, AWS/Kubernetes"
  notes: "Highlight HIPAA and SOC2 experience"
```

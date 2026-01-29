---
name: stratice-prospect-snapshot-builder
description: "Generates a concise, Bullhorn-ready prospect snapshot from a LinkedIn profile and public company signals to aid AE discovery and targeting."
---

# Purpose
Produce a quick, structured view of a prospect to speed up research and CRM entry.

# Inputs
- `linkedin_url` (string, required)
- `company_url` (string, optional)
- `focus_roles` (string, optional): e.g., "Eng Manager, Director, VP Eng, CIO"
- `notes` (string, optional)

# Output (structure)
**Prospect Snapshot**
- Name:
- Title:
- Seniority / Function:
- Company:
- Location:
- Team/Scope Indicators:
- Tech/Domain Clues:
- Current Openings / Hiring Signals (public only):
- Contractor Openness (inferred, with caveats):
- Recommended Entry Point (pilot req, surge pod, C2H, direct):
- Next Step CTA (15-min discovery | send sample shortlist)

**Bullhorn Fields (ready to paste)**
- Company:
- Contact First Name:
- Contact Last Name:
- Title:
- Email (if public; otherwise leave blank):
- Phone (if public; otherwise leave blank):
- Source: LinkedIn
- Notes: key signals and suggested approach

# Procedure
1. Parse the LinkedIn profile for role, scope, and authority.
2. Scan the company site for product/domain and open roles.
3. Summarize signals into the snapshot format.
4. Provide conservative inferences with clear caveats.
5. Output the Bullhorn-ready fields block.

# Guardrails
- Use only public information. Do not guess private contact data.
- Clearly label any inference as such.

# Example Invocation

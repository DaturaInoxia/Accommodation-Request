# Project Guidelines — Accommodation Request

## ⚠️ Confidentiality (read this first)

This repository contains **highly sensitive personal information**: medical
documentation, clinician correspondence, a payment receipt containing card
data, and legal consult notes for a real person's workplace accommodation case.

- This repo is pushed to GitHub (`DaturaInoxia/Accommodation-Request`).
  Verify it is **private**. If it is ever public, stop and tell the user
  immediately — this data must not be publicly visible.
- Never copy file contents into responses, logs, or external services.
- Never expose identifiers, account numbers, addresses, or clinical details
  outside this workspace.
- When generating content, stay within the OHRC/OPSEU accommodation domain;
  never fabricate medical facts or diagnoses.

## What this project is

Working document set for **Ken Wood's** workplace accommodation request:
remote work (work-from-home) as accommodation under the Ontario Human Rights
Code (OHRC), in an Ontario Public Service (OPS) / OPSEU workplace with a
return-to-office (5 days/week) mandate.

Core strategy: focus on **functional limitations** (commuting's impact and
relapse risk), not diagnosis. Two documentation layers:

1. **Psychologist** → clinical evidence foundation (functional limitations,
   assessment, supporting report).
2. **Physician / Nurse Practitioner** → formal sign-off, since OPS/OPSEU
   forms require a "legally qualified medical practitioner".

## Folder structure

| Path | Contents |
|------|----------|
| `00 – Document Index & Strategy Map (Ken Wood).docx` | Master index / roadmap |
| `Accommodation - ASCO Documentation/` | Correspondence with Paige McKenzie, addiction counsellor at ASCO (Addiction Services Central Ontario), and a draft for the doctor's note |
| `Accommodation – HR Evidence/` | Evidence packet, HR accommodation request, OPS return-to-office standard |
| `Accommodation – Legal Documentation/` | Achkar Law payment receipt + initial consult notes |
| `Accommodation – Medical Documentation/` | Clinician letters, notes, consent form, OHRC mapping, Rocket Doctor + Telus Health material |
| `Accommodation – Medical Documentation/Psychologist/` | Background, coping strategies, journals, letter, lists, prompts |
| `Accommodation – Medical Documentation/RocketDoctor/` | Clinician briefing/evidence packets + prep |
| `Accommodation – Personal Strategy/` | Internal functional-limitations reference + WFH (AWA) timeline |
| `Prompts/` | Reusable prompt templates for OHRC analysis and clinician search |
| `AI Summary AsOf Dec 15.docx`, `Appointment History.xlsx` | Summary + appointment log |

## Document & file conventions

- **Numbered prefix** (`00 –`, `01 –`, …) indicates reading/priority order.
- **`.docx`, `.xlsx`, `.pdf` are binary** — git tracks that they changed but
  cannot show diffs. Prefer plain text (`.txt`/`.md`) for anything needing
  revision history.
- **`.txt` and `.md` files are the editable source of truth** for prompts and
  correspondence. Make content edits there.
- Filenames use en dashes and special characters — quote paths in shell
  commands.
- Dates in filenames (e.g. `Dec1_Recieved_MedicalNote1.pdf`,
  `Ken W Letter June 10 2026 PF.docx`) are a deliberate convention — keep it.

## Domain rules the agent must follow

When helping with any document or prompt in this project:

1. Ground claims in the **Ontario Human Rights Code** and official OHRC
   policy; link to `https://www.ohrc.on.ca/...` sources.
2. Distinguish `OHRC FACT` / `INTERPRETATION` / `PRACTICAL GUIDANCE`.
3. Emphasize **functional limitations over diagnosis**; frame requests around
   barriers and impact, not labels.
4. Honor the two-layer rule: psychologist evidence + physician/NP sign-off.
   Do not suggest a psychologist alone suffices for OPS/OPSEU formal forms.
5. Do not speculate; flag missing facts and challenge weak framing.

### Key legal references (verified in workspace docs)

- **OHRC** — accommodation turns on *functional limitations*, not diagnosis.
  The employer may generally only ask: does a disability exist; what are the
  limitations; can essential duties be performed with/without accommodation;
  what accommodation is needed. Employers must pay for required medical
  documentation (e.g. notes/letters setting out accommodation needs).
- **OPSEU** — Unified collective agreement Appendix 67 defines a "legally
  qualified medical practitioner" as a physician, dentist, or nurse
  practitioner. OPSEU's 2022 bargaining update (arbitrated definition)
  confirms this **excludes a psychologist**. Hence: psychologist = evidence
  layer; NP/physician = formal sign-off layer.

Canonical prompt patterns live in `Prompts/MaterPrompt.md` (self),
`Prompts/MaterPrompt_Practiioner.md` (OPSEU-specific), and
`Prompts/FindClinicial.md` (clinician search).

## Current status & next steps

- **Live status + key decisions:** `CURRENT_STATUS.md` (read first).
- **Prioritized actions:** `Accommodation – Personal Strategy/ACTION ITEMS.md`.
- **Psychologist meeting questions:** `Accommodation – Medical Documentation/Psychologist/PeterMeeting_Agenda.txt`.
- **Physician note template:** `Accommodation – Medical Documentation/DoctorNote_Template.txt`.

## Git conventions

- Branch: `main` (tracks `origin/main`).
- Commit messages: imperative and specific
  (e.g. `Update 07 – HR request with timeline`).
- Line endings: Windows CRLF. LF→CRLF warnings on `.txt` files are expected —
  ignore them.
- `AGENTS.md` is the single source of agent instructions here; do not add a
  parallel `copilot-instructions.md`.

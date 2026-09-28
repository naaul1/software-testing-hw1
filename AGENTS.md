# AGENTS.md

Course-assignment repo for CS423 Software Testing, HW01. This is a **document-writing repo** — there is no code, no build/test/lint tooling, and no CI. Do not scaffold any.

## Layout

- `requirements.md` — the assignment spec (authoritative source of truth; currently **untracked** in git — don't assume it is committed, and don't silently add/remove it).
- `report.md` — the graded report skeleton (student: Trần Đình Luân, MSSV 23120059). Fill in its 8 section headings; keep the header block intact.
- `AI-collaboration-documents/` — mandatory AI-compliance artifacts, all required for submission:
  - `prompt-log.md` — must record **every AI prompt sent, with a timestamp** (currently empty).
  - `[AI-02]` AI Audit Report, `[AI-03]` AI Disclosure Form, `[AI-05]` Privacy Checklist — filled `.docx` templates, kept here for the submission zip.

## Non-negotiable constraints (from `requirements.md`)

- Every AI-produced artifact (test cases, job lists, defect lists, mindmap, etc.) needs an `[AI-02]` entry with the 5-section template: prompt + tool + timestamp, full AI output, VALID/INVALID/INCOMPLETE verdict, reasoning, student fix. Missing this forfeits the whole 15–20 pt AI Compliance column.
- **Never fabricate or auto-generate**: the device photo with student-ID card, execution-video voice narration, job-posting screenshots showing a username, or the prompt log itself — these are anti-cheat evidence graded by TAs. Also never invent job-posting links, defect sources, or YouTube video links.
- When you (the agent) produce content, treat your own prompts as loggable: they must be recorded in `prompt-log.md` and traceable to an `[AI-02]` entry.

## Working rules (from the student — follow strictly)

1. **Language:** chat/conversation answers must be in **English** (standing rule from 22/09/2026, per student order). Content written into to-be-submitted documents (`report.md`, `req1.md`, prompt log, etc.) must still be written in **Vietnamese**. Keep proper nouns (company/posting titles, skill names, links, numbers) as-is.
2. **Scope discipline:** do **not** fill in other sections of `report.md` (or any other to-be-submitted document) **without a direct command** from the student. Only Requirement 1 (Assignment 1) content is currently authorized.
3. **Conciseness:** write content as **short and concise as possible** — like a student would write — while still satisfying every rubric requirement (e.g., per-posting link + dated screenshot + JD + required skills + salary + 1–2-sentence AI impact; ≥3 AI/LLM-required postings).
4. **Prompt-log format (Appendix A - verbatim, written directly by hand):** `prompt-log.md` records **every user prompt from now on** (each main prompt sent to the AI counts as one entry), and is maintained **directly by hand** - you write every entry into the file yourself with `edit`, there is **no script** (do not create one; never reference a generator). Standing rule (from 22/09/2026, per student order): for EVERY prompt the student makes, append one entry holding **only basic info**: tool = AI **platform + model** (e.g. `OpenCode - Muse Spark 1.3 Free`), **not** the web tool used; a real timestamp with date and time (HH:MM dd/mm/yyyy + timezone); the **full verbatim prompt**; and the **full verbatim AI output** - no shorten, no paraphrase, no truncation (per item 3 of [AI-02] in `requirements.md`). Keep characters as-is (including whitespace, special chars, English). **Skip individual internal tool calls** (`websearch` / `webfetch` / `curl` / `read` / `grep` / `shell` / `question` ...) - do not log them.
5. **Character set:** do **not** use characters that are not on a standard keyboard in**any to-be-submitted document**: em dash `—`/en dash `–`, arrows `→`/`←`, Greek letters, emoji (e.g. ✅ ⚠️ ❌), `≥`/`≤`/`≈`/`…`/`·`, curly quotes, etc. Use ASCII equivalents (`-`, `->`, `~`, `>=`, `<=`, `...`, `"`). Vietnamese diacritics (e.g. ầ, ứ, ơ) ARE allowed because they are on the Vietnamese keyboard; keep the report header block (lines 1-5) exactly as-is. **Exception (verbatim quotes):** the verbatim prompt/output/file-quote sections inside `prompt-log.md` (and any verbatim quote used to comply with anti-para rubric item 3 of [AI-02]) may keep the original characters as-is - they are exempt from this rule (and from rule 1's language rule), because rubric item 3 of [AI-02] mandates full verbatim no-paraphrase; do NOT "sanitize" a verbatim quote. This applies only inside quoted/fenced verbatim sections, NOT to content you (the agent) author yourself.

## HW01 deliverables (written into `report.md`)

1. 10 QA/QC job postings published ≤60 days before submission (≥3 requiring AI/LLM skills) with dated screenshots + 1–2 sentence AI impact each.
2. 20 software defects publicized 2022–2026 (≥5 AI/LLM-related) with source link, severity, consequences, solution.
3. 15 test cases for one physical device (photo + student ID required); ≥3 must be edge cases the AI missed; ≥5 executed on the real device with narrated videos (≤60s).

## Submission

Zip named `StudentID_HW01_AI_<grade>.zip` (grade = 3 digits, 000–100) containing: report PDF (with AI Audit Report, AI Critique, Mandatory Disclosure sections), prompt log as Appendix A, test-case Excel, bug screenshots, device photo, ≥5 YouTube unlisted links, and the three signed AI templates.
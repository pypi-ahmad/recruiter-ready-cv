---
name: recruiter-ready-cv
description: Create, audit, repair, and tailor CVs or resumes for ATS and post-ATS human recruiter screening, with structured content and an ATS-safe LaTeX deliverable. Use when starting a CV from career information, improving an existing CV in text, Markdown, LaTeX, PDF, or DOCX, diagnosing why qualified applications get few interviews, converting duties into evidence-led achievements, aligning a CV to a vacancy, or checking CV and LinkedIn positioning.
---

# Recruiter-Ready CV

## Goal

Make the candidate's target, level, value, and relevant evidence obvious within a recruiter's first scan. Create or repair the CV using verified facts, then provide structured content and a clean LaTeX version that remains easy for an ATS to parse.

## Choose the Workflow

- **Create:** Use when the candidate has no usable CV or requests a new one. Run the interview-first intake before drafting.
- **Repair:** Use when a CV already exists. Preserve its facts, diagnose recruiter-screening weaknesses, and revise only what improves clarity, evidence, positioning, or vacancy fit.
- **Audit only:** If the user asks only for feedback, return the diagnosis without creating or changing a file.

## Gather Context

Use the candidate's supplied material as the source of truth. Read an existing CV with the appropriate document capability when it is provided as PDF or DOCX, and never overwrite the original.

Collect or infer only when supported:

- target role, seniority, industry, location, and target market;
- job description or representative vacancies;
- name and user-approved contact details;
- employment history, dates, responsibilities, achievements, tools, and scope;
- education, certifications, projects, languages, and other relevant qualifications;
- supplied LinkedIn content; and
- job-search funnel signals, especially applications, interviews, and offers.

If no job description is available, create a strong general version for the stated target and disclose that vacancy-specific tailoring is limited. Treat few interviews as a possible CV, positioning, or targeting problem; treat interviews without offers as evidence that the CV may not be the main constraint.

## Create a New CV

### 1. Interview before drafting

Ask focused questions in small batches. Gather the minimum verified dataset in this order:

1. Target role, level, market, and job description.
2. Recent roles, employers, locations, and dates.
3. Responsibilities, problems solved, achievements, scope, and measurable results for each relevant role.
4. Education, certifications, skills, tools, projects, and languages.
5. Contact details and optional sections the candidate wants included.

Do not draft the final CV until the target and core career history are clear. Skip questions already answered. Do not request unnecessary sensitive information such as a full street address, age, marital status, photograph, or government identifier.

If the candidate cannot supply a result or metric, preserve an accurate responsibility statement or mark a clear evidence gap. Never invent a number, employer, title, date, tool, qualification, responsibility, or outcome.

### 2. Build the professional story

- Establish one coherent target across the headline, summary, skills, and recent experience.
- Connect career changes and varied experience through relevant transferable evidence.
- Select the strongest evidence for the target rather than treating every past duty equally.
- Order sections by relevance. Use professional summary, core skills, experience, and education by default; add projects, certifications, languages, or other sections only when useful.
- Keep the final length proportional to experience and target-market norms, normally one or two pages.

## Repair an Existing CV

### 1. Run the first-scan test

Determine whether a recruiter can identify within seconds:

- who the candidate is professionally;
- their strongest capabilities and domain;
- their operating level and scope;
- the role they are targeting; and
- the value they are likely to bring.

Flag ambiguity or contradictions across the headline, summary, skills, recent experience, target role, and supplied LinkedIn content.

### 2. Replace duties with evidence

Identify bullets that only describe assigned work, such as "responsible for recruitment" or "prepared monthly reports." Prefer evidence-led bullets that show:

- the problem or objective;
- the candidate's action or contribution;
- the scale, such as team, portfolio, budget, geography, or workload; and
- the result, improvement, or business effect.

Use **action + scope/context + result** where the evidence supports it. When no result is available, make ownership and complexity clear without fabricating impact.

### 3. Tailor to the vacancy

- Identify the problems the employer needs solved, not just the job title.
- Extract repeated capabilities, required experience, systems, industry context, and practical constraints.
- Map high-priority requirements to verified candidate evidence.
- Move the strongest matching evidence earlier and reduce emphasis on less relevant material.
- Use accurate keywords naturally. Do not treat keyword insertion alone as tailoring.
- Preserve unrelated content unless changing it materially improves the target application.

### 4. Check supporting consistency

Compare supplied CV and LinkedIn content for consistent dates, titles, scope, seniority, and professional direction. They need not be identical, but they must tell the same story. Do not claim to have checked LinkedIn unless its content was provided or accessed with the user's authorization.

### 5. Separate document issues from relative fit

Distinguish fixable presentation problems from factors such as a closer competing candidate, direct industry experience, specific systems experience, or location requirements. Do not imply that ATS passage or meeting minimum requirements guarantees an interview.

## Produce the Deliverables

Unless the user requests another format, return:

1. **Recruiter-screen verdict** - State whether the target, level, value, and fit are immediately clear.
2. **Priority findings** - For a repaired CV, rank the few blockers most likely to weaken human screening and cite the source text.
3. **Final structured CV** - Provide polished, copy-ready content using only verified facts.
4. **Evidence gaps** - List unresolved scope, results, dates, or context; do not hide placeholders.
5. **Alignment check** - Summarize vacancy coverage and verifiable CV/LinkedIn inconsistencies.
6. **LaTeX file** - Create the ATS-safe `.tex` deliverable and report its path and compilation status.

Keep feedback candid, specific, and prioritized. Do not bury the main diagnosis in minor wording edits or claim a universal ATS score.

## Create the LaTeX File

1. Copy `assets/ats-resume.tex` to the user-requested output path and edit the copy, never the bundled template.
2. If no output path is given, use the current workspace and name the file `<first-name>-<last-name>-resume.tex`; use `resume.tex` when the name is unknown.
3. Never overwrite an existing file without explicit approval. Use a clear alternative such as `*-revised.tex` when needed.
4. Replace all template guidance with verified candidate content and remove empty or irrelevant sections.
5. Keep a single-column reading order. Do not add photos, icons, charts, text boxes, headers containing essential information, or complex tables.
6. Use `a4paper` by default; change to `letterpaper` when the target market convention requires it.
7. Escape LaTeX-sensitive characters in visible text: `\`, `#`, `$`, `%`, `&`, `_`, `{`, `}`, `~`, and `^`. Use `\url{}` or `\href{}{}` for links.
8. Compile with `pdflatex -interaction=nonstopmode -halt-on-error` in a temporary output directory when `pdflatex` is available. Run a second pass when references or links require it. Do not silently install missing packages.
9. If broader Unicode support is required, adapt the font preamble and compile with `xelatex`. If no compiler is available, review the syntax and clearly report that the file was not compiled.

## Final Checklist

Confirm that:

- the candidate's professional identity is clear within seconds;
- achievements and contribution are visible, not only duties;
- the most relevant evidence is easy to find;
- the CV is tailored through evidence and emphasis, not keyword stuffing;
- supplied CV and LinkedIn information support the same positioning;
- every fact, metric, date, and qualification is verified;
- the structured content and LaTeX file contain the same information; and
- the LaTeX source has no unresolved template guidance or accidental overwrites.

Source basis: Zara Ali, "Your CV Passed the ATS. The Recruiter Still Rejected It. Here's Why," August 17, 2026.

---
name: recruiter-ready-cv
description: Interview candidates comprehensively, then create, audit, repair, or tailor CVs and resumes for ATS and post-ATS recruiter screening with verified structured content, an ATS-safe LaTeX source, and a compiled PDF when available. Use when starting a resume from career information, improving an existing resume in text, Markdown, LaTeX, PDF, or DOCX, diagnosing why qualified applications get few interviews, converting duties into evidence-led achievements, aligning a resume to a vacancy, or checking resume and LinkedIn positioning.
license: MIT
---

# Recruiter-Ready CV

## Goal

Make the candidate's target, level, value, and relevant evidence obvious within a recruiter's first scan. Gather and confirm every resume-relevant fact before creating or revising the document. Never invent missing information.

## Choose the Workflow

- **Create:** Start from career information or no usable resume. Complete the intake and confirmation gate before drafting.
- **Update:** Read the existing resume, extract its facts, ask the candidate to correct them, then interview only for missing, ambiguous, conflicting, or weak evidence.
- **Audit:** Diagnose the supplied resume first. After presenting the audit, ask whether the candidate wants to continue into the update interview. Do not create files unless they agree.

Use the candidate's supplied material as the source of truth. Read PDF or DOCX input with the appropriate document capability. Never overwrite an original resume.

## Diagnose the Application Funnel When Relevant

When the candidate mentions repeated rejections, few interviews, or poor application conversion, read the conditional application-funnel questions in [references/intake-questionnaire.md](references/intake-questionnaire.md). Ask only enough to identify the likely failure stage and recurring pattern; do not make these questions mandatory for an ordinary Create or Update request.

If the user wants diagnosis before document creation or revision, route the broader pre-interview visibility audit to `$audit-job-search-visibility`. Continue here when the user requests a resume audit, creation, update, or approved rewrite.

- If genuinely qualified applications produce few or no interviews, investigate the resume, positioning, targeting, and supplied LinkedIn content.
- If applications consistently produce interviews but not offers, explain that the resume is unlikely to be the primary bottleneck. Do not automatically rewrite it; offer a separate resume audit if the candidate still wants one and identify interview or later-stage conversion as the area to examine.
- Distinguish fixable document problems from competition or relative-fit factors. A qualified candidate may lose to someone with closer industry, systems, location, or achievement evidence.
- Look for repeated patterns across comparable applications. Do not recommend a broad rewrite because of one rejection.

## Run the Comprehensive Interview

For Create or Update, read [references/intake-questionnaire.md](references/intake-questionnaire.md) completely before interviewing.

### Maintain a fact ledger

Track each relevant field internally with one status:

- **Verified:** explicitly supplied or confirmed by the candidate.
- **Unknown/skipped:** the candidate cannot or chooses not to provide it.
- **Not applicable:** the category does not apply.
- **Conflicting:** supplied sources disagree and the candidate has not resolved them.

Do not infer a factual value merely because it is likely. Record the source of important metrics, dates, titles, qualifications, and claims when multiple documents are involved.

### Ask adaptively

- Ask 3--5 related primary questions per turn.
- Work through one intake section at a time and one employment role at a time.
- Skip facts already supplied; confirm extracted facts rather than asking the candidate to re-enter them.
- Follow vague answers with targeted questions about action, problem, scale, stakeholders, tools, constraints, and outcome.
- Offer examples of the kind of evidence needed, but never suggest a number or claim for the candidate to adopt.
- Accept an explicit unknown, skip, or not-applicable answer and record it instead of repeatedly asking.
- Explain why a sensitive-looking question is relevant. Do not request age, date of birth, marital status, government identifiers, a full street address, salary history, references, or a photograph unless the candidate explicitly requests a market-specific version requiring it.

### Complete each workflow

For a new resume, cover every applicable questionnaire category. For an existing resume:

1. Extract a fact inventory from the source.
2. Present a concise summary of extracted identity, target, dates, titles, education, and major claims for correction.
3. Mark confirmed facts as Verified.
4. Ask only about uncovered categories, conflicts, weak positioning, duty-only bullets, and missing evidence.

Do not draft the final resume until:

- the target role, level, market, and core career history are clear;
- every applicable questionnaire category has a ledger status;
- all material conflicts are resolved;
- evidence gaps are explicitly marked unknown/skipped; and
- the candidate confirms the final fact summary.

If the candidate asks for an early draft, provide a clearly labeled working draft with visible gaps, then resume the interview. Do not represent it as final.

## Build the Professional Story

- Establish one coherent target across the headline, summary, skills, and recent experience.
- Connect career changes through verified transferable evidence.
- Select evidence for the target rather than treating every past duty equally.
- Order sections by relevance and keep the final length proportional to experience and target-market norms, normally one or two pages.
- If no job description is available, create a strong general version for the stated target and disclose that vacancy-specific tailoring is limited.

## Repair and Tailor

### Run the first-scan test

Determine whether a recruiter can identify within seconds who the candidate is professionally, their strongest capabilities, operating level, target, and likely value. Flag contradictions across the headline, summary, skills, recent experience, target role, and supplied LinkedIn content.

### Replace duties with evidence

Prefer bullets using **action + scope/context + result** when supported. Establish the problem, contribution, scale, and effect. When no metric or result is available, state accurate ownership, complexity, or scope without fabricating impact.

### Tailor through evidence

- Identify the employer's problems, repeated capabilities, required systems, industry context, and practical constraints.
- Map high-priority requirements to verified evidence.
- Move the strongest matching evidence earlier and reduce emphasis on less relevant material.
- Use accurate keywords naturally; keyword insertion alone is not tailoring.
- Compare supplied resume and LinkedIn content for consistent dates, titles, scope, seniority, and direction.
- Separate fixable document issues from relative-fit factors such as industry, systems, or location.
- Preserve the resume's verified core facts and positioning across applications. Tailor emphasis for each vacancy, and recommend broader changes only when repeated outcomes or evidence reveal a pattern.

## Produce the Deliverables

For Create and Update, unless the user requests otherwise, return:

1. **Recruiter-screen verdict:** State whether target, level, value, and fit are immediately clear. When application outcomes are supplied, state whether the resume appears to be the likely funnel bottleneck.
2. **Priority findings:** For an existing resume, rank the few blockers most likely to weaken human screening and cite the source text.
3. **Confirmed fact summary:** Record the facts approved before drafting.
4. **Final structured resume:** Provide polished, copy-ready content using only verified facts.
5. **Evidence gaps:** List unknown/skipped scope, results, dates, or context.
6. **Alignment check:** Summarize vacancy coverage and verifiable resume/LinkedIn inconsistencies.
7. **LaTeX and PDF:** Create the ATS-safe `.tex` file and compile a `.pdf` when tooling is available.

For Audit, return only the recruiter-screen verdict, priority findings, evidence gaps, and applicable alignment checks. Do not create a final structured resume, LaTeX source, or PDF unless the candidate explicitly agrees to continue into Update.

Do not claim a universal ATS score or guarantee an interview.

## Create the LaTeX and PDF Files

1. Copy `assets/ats-resume.tex` to the requested output path and edit the copy, never the bundled template.
2. If no path is given, use the current workspace and name the source `<first-name>-<last-name>-resume.tex`; use `resume.tex` when the name is unknown.
3. Never overwrite an existing file without explicit approval. Prefer `*-revised.tex` and `*-revised.pdf` for updates.
4. Replace all template guidance with confirmed content and remove empty or irrelevant sections.
5. Preserve the template's single-column reading order, plain headings, and text-only contact information. Do not add photos, icons, colors, charts, text boxes, or tables.
6. Use `a4paper` by default; change to `letterpaper` when required by the target market.
7. Escape LaTeX-sensitive visible characters: `\`, `#`, `$`, `%`, `&`, `_`, `{`, `}`, `~`, and `^`. Use `\url{}` or `\href{}{}` for links.
8. Compile with `pdflatex -interaction=nonstopmode -halt-on-error` in a temporary output directory. Disable automatic package installation when the distribution supports it. Run a second pass, then copy the PDF beside the `.tex` file.
9. Extract text from the PDF when a suitable tool is available and confirm the name, headings, roles, dates, and bullets appear in reading order.
10. If broader Unicode support is required, adapt the font preamble and use `xelatex`. If no compiler is available, syntax-review the source and clearly report that no PDF was produced.

## Final Checklist

Confirm that:

- every applicable intake category is verified, unknown/skipped, or not applicable;
- the candidate approved the fact summary and all conflicts are resolved;
- professional identity and target are clear within seconds;
- achievements and contribution are visible, not only duties;
- relevant evidence is easy to find and vacancy emphasis is accurate;
- any supplied application outcomes are diagnosed at the correct funnel stage without overreacting to one rejection;
- every metric, date, qualification, tool, and claim is supported;
- structured content, LaTeX, and PDF contain the same information;
- PDF text extracts in a logical ATS reading order; and
- no template guidance, sample identity, or accidental overwrite remains.

Source basis: Zara Ali, ["Your CV Passed the ATS. The Recruiter Still Rejected It. Here's Why"](https://www.linkedin.com/pulse/your-cv-passed-ats-recruiter-still-rejected-heres-why-zara-ali-bgsdf/), August 17, 2026.

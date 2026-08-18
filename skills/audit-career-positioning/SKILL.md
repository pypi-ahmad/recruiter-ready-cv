---
name: audit-career-positioning
description: Audit whether a candidate's CV, supplied LinkedIn content, target role, vacancy evidence, and application outcomes communicate one clear professional direction within a recruiter's first scan. Use when a qualified job seeker gets few interviews, targets several unrelated roles, has inconsistent CV and LinkedIn positioning, relies on job-title matching, lists responsibilities instead of impact, buries strong achievements, or wants the 10-second Career Clarity Test and a focused action plan before rewriting anything.
license: MIT
---

# Audit Career Positioning

## Goal

Determine whether a recruiter can quickly identify the candidate's target, level, strongest relevant capabilities, and credible evidence. Diagnose positioning before recommending more applications, qualifications, or a document rewrite.

If the main request is to diagnose why repeated, genuinely suitable applications produce few or no interviews across targeting, CV evidence, supplied LinkedIn content, keywords, presentation, or referral expectations, route first to `$audit-job-search-visibility`. Use this skill when professional direction and requirement-to-evidence clarity are the primary questions.

## Keep the Audit Separate from Rewriting

Return diagnosis and an action plan first. Do not rewrite the CV, LinkedIn profile, or supporting documents unless the candidate explicitly agrees to continue.

After approval, hand confirmed facts and priorities to `$recruiter-ready-cv`. Do not duplicate its interview, fact-confirmation, LaTeX, or PDF workflow. If that skill is unavailable, provide a copy-ready handoff prompt instead of performing the rewrite here.

## Gather the Minimum Inputs

Ask for only missing information:

- primary target role and acceptable adjacent roles;
- CV or resume content;
- supplied LinkedIn headline, About section, and recent experience;
- job description or representative vacancies; and
- application outcomes when the candidate reports repeated rejection or low conversion.

Do not claim to have reviewed a live profile unless its content was supplied or access was authorized. If no job description is available, audit against the stated target and disclose that requirement-level matching is limited.

## Run the Audit

### 1. Perform the 10-second Career Clarity Test

Inspect only the visible first-scan material first: headline, summary, top skills, most recent role, and earliest prominent achievements. Record the role and level these elements imply before reading the rest.

Compare that inference with the candidate's stated target. Classify positioning as:

- **Clear:** one target and level are immediately supported;
- **Partly clear:** a likely target is visible but competing signals weaken it; or
- **Unclear:** multiple directions or generic wording prevent a reliable inference.

### 2. Check Target Concentration

Identify competing role families across the headline, summary, skills, and recent experience. Treat versatility as supporting evidence, not as the professional identity. Flag a document that tries to target unrelated functions equally.

### 3. Compare CV and LinkedIn Direction

Check whether both sources support the same target, seniority, dates, titles, capabilities, and recent trajectory. They need not use identical wording. Flag contradictions that make the candidate appear broader, more junior, more senior, or differently focused across sources.

### 4. Match Requirements to Evidence

Do not decide fit from job titles alone. Extract the five highest-priority recurring requirements from the supplied vacancy or representative roles. For each requirement, classify candidate support as:

- **Visible evidence:** specific and easy to find;
- **Buried evidence:** supported but difficult to notice;
- **Weak evidence:** responsibility or generic claim without contribution, scope, or result;
- **Missing evidence:** no supplied support; or
- **Conflicting evidence:** sources disagree.

Never convert a missing claim into candidate experience. Distinguish a positioning problem from a genuine qualification, industry, systems, location, authorization, or seniority gap.

### 5. Test Impact and Evidence Visibility

Flag bullets that only describe what the role required. Prefer evidence containing action, ownership, scope or context, and a verified result. When metrics do not exist, accept accurate complexity, scale, stakeholders, frequency, or qualitative effect.

Identify strong evidence hidden below generic summaries, long duty lists, or unrelated experience. Recommend moving verified target-relevant evidence earlier; do not invent numbers or outcomes.

### 6. Diagnose the Funnel Only When Outcomes Are Supplied

Use patterns across comparable, genuinely suitable applications:

- Few or no interviews may support a positioning, targeting, or document-clarity diagnosis.
- Regular interviews but no offers indicate that the resume is unlikely to be the primary bottleneck.
- One rejection does not support a broad conclusion or rewrite.

Do not claim certainty where competition or employer decisions are unknown.

## Produce the Audit

Return:

1. **Career-clarity verdict:** Clear, Partly clear, or Unclear; inferred target; stated target; and the decisive evidence.
2. **Priority findings:** Rank the few issues most likely to weaken shortlisting and cite the supplied wording.
3. **Requirement-evidence map:** Show the five priority requirements, best verified evidence, visibility state, and real gaps.
4. **Buried value:** Identify the strongest target-relevant evidence that deserves earlier placement.
5. **Thirty-minute action plan:** State one target role, five repeated capabilities, the strongest evidence for each, and where each should appear across CV and LinkedIn.

When application outcomes are supplied, add a bounded statement on whether positioning appears to be the likely funnel bottleneck.

## Prepare the Rewrite Handoff

After the candidate agrees to continue, summarize:

- confirmed primary and adjacent targets;
- five priority capabilities;
- verified evidence and source wording;
- gaps and conflicts;
- CV and LinkedIn alignment problems; and
- content-ordering and rewrite priorities.

Pass this summary and the candidate's supplied source material to `$recruiter-ready-cv`. Require that skill to confirm facts before drafting and preserve its no-overwrite rule.

## Guardrails

- Do not invent employers, dates, titles, qualifications, responsibilities, metrics, outcomes, or tools.
- Do not promise interviews or assign a universal ATS score.
- Do not recommend another qualification, industry change, or higher application volume without evidence that it addresses the observed bottleneck.
- Do not expose private contact details in the audit unless needed to identify a source conflict.

Source basis: Zara Ali, ["You're Applying for the Right Jobs So Why Are You Still Not Getting Interviews?"](https://www.linkedin.com/pulse/youre-applying-right-jobs-so-why-you-still-getting-interviews-ali-ruijf/).

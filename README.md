<div align="center">

# Recruiter-Ready CV

Three agent skills for diagnosing job-search visibility and career positioning, then creating, repairing, or tailoring ATS-friendly resumes that persuade human recruiters.

[![Agent Skill](https://img.shields.io/badge/Agent_Skill-SKILL.md-6f42c1?style=flat-square)](https://agentskills.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

[Repository](https://github.com/pypi-ahmad/recruiter-ready-cv) · [Visibility audit](skills/audit-job-search-visibility/SKILL.md) · [Positioning audit](skills/audit-career-positioning/SKILL.md) · [CV skill](skills/recruiter-ready-cv/SKILL.md) · [Interview checklist](skills/recruiter-ready-cv/references/intake-questionnaire.md) · [LaTeX template](skills/recruiter-ready-cv/assets/ats-resume.tex)

</div>

The repository separates diagnosis from document creation. `audit-job-search-visibility` finds the likely pre-interview bottleneck, `audit-career-positioning` tests whether the candidate's target and evidence are clear, and `recruiter-ready-cv` turns confirmed career information into a vacancy-aware resume.

> [!IMPORTANT]
> The skills do not invent employers, titles, dates, qualifications, responsibilities, metrics, or outcomes. They improve how verified evidence is presented; they cannot guarantee an interview.

## Table of contents

- [Available skills](#available-skills)
- [What audit-job-search-visibility does](#what-audit-job-search-visibility-does)
- [How the job-search visibility audit works](#how-the-job-search-visibility-audit-works)
- [Job-search visibility inputs and privacy](#job-search-visibility-inputs-and-privacy)
- [What audit-career-positioning does](#what-audit-career-positioning-does)
- [How the career positioning audit works](#how-the-career-positioning-audit-works)
- [Career positioning application funnel diagnosis](#career-positioning-application-funnel-diagnosis)
- [Career positioning audit inputs and privacy](#career-positioning-audit-inputs-and-privacy)
- [What recruiter-ready-cv does](#what-recruiter-ready-cv-does)
- [Recruiter-ready CV workflow modes](#recruiter-ready-cv-workflow-modes)
- [How recruiter-ready CV works](#how-recruiter-ready-cv-works)
- [Recruiter-ready CV application funnel diagnosis](#recruiter-ready-cv-application-funnel-diagnosis)
- [Recruiter-ready CV inputs and privacy](#recruiter-ready-cv-inputs-and-privacy)
- [Installation](#installation)
  - [Install all skills](#install-all-skills)
  - [Install audit-job-search-visibility](#install-audit-job-search-visibility)
  - [Install audit-career-positioning](#install-audit-career-positioning)
  - [Install recruiter-ready-cv](#install-recruiter-ready-cv)
  - [Shared installer options](#shared-installer-options)
  - [Install with gh](#install-with-gh)
- [Usage examples](#usage-examples)
- [Job-search visibility audit deliverables](#job-search-visibility-audit-deliverables)
- [Career positioning audit deliverables](#career-positioning-audit-deliverables)
- [Recruiter-ready CV deliverables](#recruiter-ready-cv-deliverables)
- [ATS template and generated files](#ats-template-and-generated-files)
- [Repository structure](#repository-structure)

## Available skills

| Skill | Use it for | Default result |
| --- | --- | --- |
| [`audit-job-search-visibility`](skills/audit-job-search-visibility/SKILL.md) | Diagnosing why repeated, genuinely suitable applications produce few or no interviews | Funnel verdict, suitability check, visibility scorecard, and bounded application experiment |
| [`audit-career-positioning`](skills/audit-career-positioning/SKILL.md) | Testing whether a CV, supplied LinkedIn content, and vacancy evidence communicate one clear target | Career-clarity verdict, requirement-evidence map, and 30-minute action plan |
| [`recruiter-ready-cv`](skills/recruiter-ready-cv/SKILL.md) | Creating, updating, auditing, or tailoring a verified resume | Structured content, LaTeX source, and PDF when available |

## What audit-job-search-visibility does

High application volume alone does not show whether a job seeker is visible to recruiters or genuinely matched to the roles. `audit-job-search-visibility` diagnoses the repeated failure stage before recommending more applications or a document rewrite.

The skill:

- Tests whether representative applications meet the vacancies' core requirements and constraints.
- Distinguishes hidden value from weak targeting, genuine fit gaps, and later-stage interview problems.
- Checks whether target, level, relevant experience, and likely value are obvious on the first scan.
- Audits achievement evidence, natural vacancy terminology, presentation, and supplied CV/LinkedIn alignment.
- Treats referrals as a visibility channel rather than a substitute for credible evidence.
- Produces a bounded next-application experiment without promising interviews or blaming the market, recruiters, or ATS systems.

## How the job-search visibility audit works

1. **Establish the funnel pattern.** Review application count, time period, outcomes, and channels without treating volume as proof of suitability.
2. **Test representative applications.** Classify the evidence as Suitable, Partly suitable, Mismatched, or Unknown against recurring requirements and constraints.
3. **Run the first-scan test.** Determine whether the CV quickly communicates target, level, relevant experience, and value.
4. **Audit visibility.** Check achievement evidence, keyword alignment, document presentation, and supplied LinkedIn consistency without inventing facts or using a fixed page rule.
5. **Return diagnosis first.** Provide the funnel and visibility verdicts, priority findings, and a bounded experiment before offering a handoff.

Use `audit-job-search-visibility` when the main question is why suitable applications are not generating interviews. Use `audit-career-positioning` when the primary issue is an unclear professional direction. Use `recruiter-ready-cv` only when the candidate wants a comprehensive document audit, creation workflow, or approved rewrite.

## Job-search visibility inputs and privacy

Useful inputs include:

- Primary and adjacent target roles.
- Application count, time period, channels, and funnel outcomes.
- Three to five representative vacancies or recurring requirements.
- The CV version used and examples of vacancy-specific changes.
- Supplied LinkedIn headline, About section, and recent experience.
- Relevant seniority, industry, systems, location, and work-authorization constraints.

> [!NOTE]
> The audit names missing evidence and unknown employer decisions. It does not claim access to a live profile, expose unnecessary contact details, assign a universal ATS score, or make unsupported market-specific conclusions.

## What audit-career-positioning does

Being qualified and looking qualified on paper are different problems. `audit-career-positioning` tests whether a recruiter can quickly identify the candidate's target, level, strongest relevant capabilities, and credible evidence.

The skill:

- Runs the 10-second Career Clarity Test before reading the documents in depth.
- Detects competing role families that make the candidate's direction unclear.
- Checks whether supplied CV and LinkedIn content support the same target and seniority.
- Maps the five highest-priority vacancy requirements to verified candidate evidence.
- Separates responsibility-only wording from contribution, scale, and impact.
- Finds strong target-relevant evidence that is buried below generic content.
- Produces a 30-minute positioning action plan before recommending any rewrite.

## How the career positioning audit works

1. **Gather the minimum evidence.** Request the target role, CV, supplied LinkedIn content, job description or representative vacancies, and application outcomes when relevant.
2. **Run the first-scan test.** Infer the visible target from the headline, summary, top skills, recent role, and earliest prominent achievements before reading deeper.
3. **Check target concentration.** Identify unrelated roles or generic capability lists competing with the primary direction.
4. **Compare professional stories.** Check CV and LinkedIn alignment across target, seniority, dates, titles, capabilities, and recent trajectory.
5. **Map requirements to evidence.** Classify support for the five priority vacancy requirements as visible, buried, weak, missing, or conflicting.
6. **Return diagnosis before revision.** Provide prioritized findings, buried value, and a 30-minute plan; hand off to `recruiter-ready-cv` only after explicit approval.

| Verdict | Meaning |
| --- | --- |
| **Clear** | One target and level are immediately supported. |
| **Partly clear** | A likely target is visible, but competing signals weaken it. |
| **Unclear** | Multiple directions or generic wording prevent a reliable inference. |

## Career positioning application funnel diagnosis

Application outcomes are optional. When supplied, the audit uses patterns across comparable, genuinely suitable applications rather than treating every rejection as a document problem.

| Application pattern | Audit response |
| --- | --- |
| Suitable applications produce few or no interviews | Investigate positioning, targeting, evidence visibility, and supplied CV/LinkedIn alignment. |
| Applications regularly produce interviews but no offers | Explain that resume positioning is unlikely to be the primary bottleneck and avoid an automatic rewrite. |
| One vacancy produces a rejection | Do not infer a broad positioning problem; distinguish document issues from competition and genuine fit gaps. |

## Career positioning audit inputs and privacy

The audit can work with partial information, but it names the resulting limits. Useful inputs include:

- A primary target role and acceptable adjacent roles.
- CV or resume content.
- Supplied LinkedIn headline, About section, and recent experience.
- A job description or representative vacancies.
- Application counts and funnel stages when low conversion is part of the request.

> [!NOTE]
> The audit never claims to have reviewed a live profile unless its content is supplied or access is authorized. It does not invent evidence, expose unnecessary contact details, promise interviews, or assign a universal ATS score.

The audit does not rewrite documents automatically. After the candidate approves rewriting, it hands the confirmed target, evidence map, gaps, conflicts, and priorities to `recruiter-ready-cv`.

If `recruiter-ready-cv` is unavailable, the audit returns a copy-ready handoff prompt instead of attempting the rewrite itself. When application outcomes are supplied, it distinguishes low interview conversion from later-stage interview problems; regular interviews without offers do not justify an automatic CV rewrite.

Use `audit-career-positioning` for a fast positioning diagnosis. Use the Audit mode in `recruiter-ready-cv` for a comprehensive resume review that may continue into its full Update workflow.

## What recruiter-ready-cv does

Passing an ATS is only the first screening step. A resume can contain the right keywords and still fail when its target, level, achievements, or value are difficult for a recruiter to identify.

`recruiter-ready-cv` addresses both stages:

- Interviews the candidate before creating or revising a resume.
- Converts duty-based descriptions into evidence-led achievements when facts support them.
- Aligns the headline, summary, skills, and experience with the target role.
- Tailors emphasis to a vacancy instead of merely inserting keywords.
- Checks supplied resume and LinkedIn content for positioning inconsistencies.
- Diagnoses whether the resume is the likely bottleneck when application outcomes are supplied.
- Produces copy-ready structured content and an ATS-safe LaTeX source.
- Compiles a PDF when tooling is available and checks its text reading order.

## Recruiter-ready CV workflow modes

| Mode | Starting point | What the skill does | Result |
| --- | --- | --- | --- |
| **Create** | No usable resume or career information only | Conducts the complete interview and confirms every applicable category | New structured resume, `.tex`, and PDF when available |
| **Update** | Existing resume in a supported format | Extracts known facts, confirms them, then asks only about gaps, conflicts, and weak evidence | Revised resume without overwriting the original |
| **Audit** | Existing resume with feedback requested first | Diagnoses recruiter-screening problems, then asks whether to continue into an update | Prioritized findings, followed by an optional revision interview |

## How recruiter-ready CV works

1. **Select the workflow.** Determine whether the candidate needs a new resume, an update, or an audit.
2. **Gather or extract facts.** Ask 3--5 related questions at a time, or read the existing resume and summarize its known information.
3. **Resolve gaps and conflicts.** Work through one section and one employment role at a time, following vague claims with questions about action, scope, tools, stakeholders, and results.
4. **Confirm the record.** Present a concise fact summary for correction or approval before producing the final resume.
5. **Build the professional story.** Make the target, seniority, strongest capabilities, and verified value clear on the first scan.
6. **Generate and verify files.** Produce structured content and LaTeX, compile a PDF when possible, and verify logical ATS reading order.

Every resume-relevant detail is tracked using one of four states:

| State | Meaning |
| --- | --- |
| **Verified** | Explicitly supplied or confirmed by the candidate |
| **Unknown/skipped** | The candidate cannot or chooses not to provide it |
| **Not applicable** | The category does not apply |
| **Conflicting** | Supplied sources disagree and candidate confirmation is required |

Unknown information remains visible as an evidence gap rather than being guessed. Material conflicts must be resolved before the final resume is created. If the candidate requests an early draft, it is clearly labeled incomplete and the interview continues.

Without a job description, the skill creates a strong general version for the stated target and explains that vacancy-specific tailoring is limited.

## Recruiter-ready CV application funnel diagnosis

When a candidate reports repeated rejections, few interviews, or poor application conversion, the skill asks only enough questions to identify where the process is breaking. This diagnosis is conditional and does not add extra questions to an ordinary Create or Update request.

| Application pattern | Skill response |
| --- | --- |
| Genuinely suitable applications produce few or no interviews | Investigate the resume, professional positioning, targeting, and supplied LinkedIn content. |
| Applications consistently produce interviews but no offers | Explain that the resume is unlikely to be the primary bottleneck, avoid an automatic rewrite, and direct attention to interview or later-stage conversion. A separate resume audit remains available on request. |
| One vacancy results in a rejection | Avoid drawing a broad conclusion. Look for repeated patterns across comparable applications and distinguish document issues from relative-fit factors such as industry, systems, or location. |

## Recruiter-ready CV inputs and privacy

The skill accepts career information or an existing resume in plain text, Markdown, LaTeX, PDF, or DOCX. Helpful supporting material includes:

- A target job description or representative vacancies.
- Supplied LinkedIn content and professional profile links.
- Portfolio, GitHub, project, publication, or performance-review evidence.
- Education, certification, award, volunteering, and language information.

> [!NOTE]
> The interview does not request age, date of birth, marital status, government identifiers, a full street address, salary history, references, or a photograph unless the candidate explicitly requires a market-specific version. Live profiles are not treated as reviewed unless their content is supplied or access is authorized.

## Installation

### Install all skills

Install every skill in this repository at once:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --all
```

### Install audit-job-search-visibility

Install for the current project with the cross-agent installer:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill audit-job-search-visibility
```

Install globally for every detected agent:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill audit-job-search-visibility --agent '*' --global --yes
```

On Windows, use independent copies when filesystem links are unavailable:

```powershell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill audit-job-search-visibility --agent '*' --global --copy --yes
```

Preview and install for Codex with GitHub CLI:

```shell
gh skill preview pypi-ahmad/recruiter-ready-cv audit-job-search-visibility
gh skill install pypi-ahmad/recruiter-ready-cv audit-job-search-visibility --agent codex --scope user
```

### Install audit-career-positioning

Install for the current project with the cross-agent installer:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill audit-career-positioning
```

Install globally for every detected agent:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill audit-career-positioning --agent '*' --global --yes
```

On Windows, use independent copies when filesystem links are unavailable:

```powershell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill audit-career-positioning --agent '*' --global --copy --yes
```

Preview and install for Codex with GitHub CLI:

```shell
gh skill preview pypi-ahmad/recruiter-ready-cv audit-career-positioning
gh skill install pypi-ahmad/recruiter-ready-cv audit-career-positioning --agent codex --scope user
```

### Install recruiter-ready-cv

Install for the current project with the cross-agent installer:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill recruiter-ready-cv
```

Install globally for every detected agent:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill recruiter-ready-cv --agent '*' --global --yes
```

On Windows, use independent copies when filesystem links are unavailable:

```powershell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill recruiter-ready-cv --agent '*' --global --copy --yes
```

Preview and install for Codex with GitHub CLI:

```shell
gh skill preview pypi-ahmad/recruiter-ready-cv recruiter-ready-cv
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent codex --scope user
```

### Shared installer options

The recommended installer requires Node.js 18 or later. It detects supported agents already installed on the machine and prompts for the destinations:

Use `audit-job-search-visibility`, `audit-career-positioning`, or `recruiter-ready-cv` as the skill name in repository installation commands.

| Option | Effect |
| --- | --- |
| `--global` | Makes the skill available across projects. Omit it to install for the current project. |
| `--agent '*'` | Targets every supported agent detected on the machine. |
| `--yes` | Skips confirmation prompts for unattended installation. |
| `--copy` | Copies the skill instead of creating filesystem links. |

By default, the installer keeps one canonical skill and links selected agents to it. See the official [Vercel Labs Skills documentation](https://github.com/vercel-labs/skills#readme) for supported agents, locations, and update commands.

> [!IMPORTANT]
> Review third-party skills before installation. A skill can contain instructions or scripts that affect agent behavior.

### Install with gh

Review the skill before installing it:

```shell
gh skill preview pypi-ahmad/recruiter-ready-cv <skill-name>
```

Replace `<skill-name>` with `audit-job-search-visibility`, `audit-career-positioning`, or `recruiter-ready-cv`.

GitHub's `gh` tool 2.90 or later can install the skill for a specific agent. Replace `<agent>` with an ID from the table:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv <skill-name> --agent <agent> --scope user
```

| Agent | `gh skill` ID | Native personal location | Invocation |
| --- | --- | --- | --- |
| GitHub Copilot | `github-copilot` | `~/.copilot/skills/<skill-name>/` | Automatic or `/<skill-name>` |
| Codex | `codex` | `~/.agents/skills/<skill-name>/` | `$<skill-name>` |
| Claude Code | `claude-code` | `~/.claude/skills/<skill-name>/` | Automatic or `/<skill-name>` |
| OpenCode | `opencode` | `~/.config/opencode/skills/<skill-name>/` | Automatic or `/<skill-name>` |
| xAI Grok Build | `grok` | `~/.grok/skills/<skill-name>/` | Automatic or `/<skill-name>` |

To install for one repository instead, run the command from that repository and replace `--scope user` with `--scope project`.

## Usage examples

Diagnose why suitable applications are not producing interviews:

```text
Use audit-job-search-visibility to review my application outcomes, representative vacancies, CV, and supplied LinkedIn content. Separate weak visibility from targeting or genuine fit gaps before recommending changes.
```

Test whether application volume hides a targeting problem:

```text
Use audit-job-search-visibility to compare these representative jobs with my verified experience, classify the application sample, and define a bounded next-application experiment without rewriting my CV yet.
```

Create a new resume:

```text
Use recruiter-ready-cv to interview me comprehensively and create a resume for a senior data engineer role. Produce structured content, a LaTeX file, and a PDF.
```

Update an existing resume:

```text
Use recruiter-ready-cv to extract and confirm the facts in this resume, interview me about every relevant gap, and produce a revised version without inventing facts.
```

Tailor to a vacancy:

```text
Use recruiter-ready-cv to tailor my resume to this job description. Show the evidence gaps and make the strongest relevant experience easy to find.
```

Audit before deciding whether to revise:

```text
Use recruiter-ready-cv to audit this resume only. Show the highest-impact recruiter-screening problems, then ask whether I want to continue with an update interview.
```

Diagnose where the application process is breaking:

```text
Use recruiter-ready-cv to review my application outcomes, ask the conditional funnel questions, and determine whether my resume is the likely reason I am not progressing.
```

Audit career positioning before rewriting:

```text
Use audit-career-positioning to run the 10-second Career Clarity Test on my CV and supplied LinkedIn text, map this vacancy's five priority requirements to my evidence, and give me a 30-minute action plan before changing anything.
```

Check whether job-title fit is supported by evidence:

```text
Use audit-career-positioning to compare this vacancy's five most important requirements with my verified experience. Separate weak positioning from genuine experience or seniority gaps, and do not rewrite my CV yet.
```

Diagnose low interview conversion:

```text
Use audit-career-positioning to review my application outcomes, CV, and supplied LinkedIn content. Tell me whether unclear positioning appears to be the likely reason suitable applications are not producing interviews.
```

## Job-search visibility audit deliverables

The audit returns:

1. A funnel verdict identifying the likely failure stage, confidence, evidence, and limits.
2. A **Suitable**, **Partly suitable**, **Mismatched**, or **Unknown** classification for the reviewed application sample.
3. A **Visible**, **Partly visible**, **Hidden**, or **Inconclusive** visibility verdict.
4. A non-numeric scorecard covering target clarity, relevant experience, achievements, vacancy terminology, presentation, and CV/LinkedIn alignment.
5. Prioritized findings and a bounded next-application experiment.

The skill does not rewrite documents automatically. Approved target-clarity work transfers to `audit-career-positioning`; approved CV work transfers to `recruiter-ready-cv`.

## Career positioning audit deliverables

The audit returns:

1. A **Clear**, **Partly clear**, or **Unclear** career-clarity verdict, including inferred and stated targets.
2. Prioritized positioning findings citing the supplied wording.
3. A five-requirement evidence map showing visible, buried, weak, missing, or conflicting support.
4. The strongest verified evidence that deserves earlier placement.
5. A 30-minute action plan covering one target, five repeated capabilities, supporting evidence, and recommended CV/LinkedIn placement.

When application outcomes are supplied, the audit adds a bounded statement on whether positioning appears to be the likely funnel bottleneck. It creates no revised resume or profile before explicit approval; approved revision work transfers to `recruiter-ready-cv` or a copy-ready handoff prompt.

## Recruiter-ready CV deliverables

Create and Update return by default:

1. A recruiter-screen verdict, including whether the resume appears to be the likely funnel bottleneck when application outcomes are supplied.
2. Prioritized findings for an existing resume.
3. A candidate-confirmed fact summary.
4. Polished, copy-ready resume content.
5. Explicit evidence gaps that still need candidate input.
6. Vacancy and LinkedIn alignment checks when source material is supplied.
7. Generated `.tex` and `.pdf` files when compilation is available.

Audit returns only the recruiter-screen verdict, priority findings, evidence gaps, and applicable alignment checks. It does not create a final resume, `.tex`, or PDF unless the candidate explicitly agrees to continue into Update.

## ATS template and generated files

The bundled template uses a single-column, text-only layout with a centered identity block, plain ruled section headings, compact role rows, and no icons, colors, graphics, text boxes, or tables.

- New files default to `<first-name>-<last-name>-resume.tex`; unknown names use `resume.tex`.
- Existing files are never overwritten without approval. Updates use `*-revised.tex` and `*-revised.pdf` by default.
- Paper size defaults to A4 and changes to letter paper when the target market requires it.
- `pdflatex` is the default compiler; broader Unicode content can use `xelatex`.
- If no compiler is available, the skill returns a syntax-reviewed `.tex` file and reports that no PDF was produced.
- When PDF text extraction is available, the skill checks that headings, roles, dates, and bullets remain in logical ATS reading order.

## Repository structure

```text
recruiter-ready-cv/
└── skills/
    ├── audit-job-search-visibility/
    │   ├── SKILL.md
    │   └── agents/
    │       └── openai.yaml
    ├── audit-career-positioning/
    │   ├── SKILL.md
    │   └── agents/
    │       └── openai.yaml
    └── recruiter-ready-cv/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        ├── assets/
        │   └── ats-resume.tex
        └── references/
            └── intake-questionnaire.md
```

The workflows distill recruiter-screening principles from Zara Ali's [“Your CV Passed the ATS. The Recruiter Still Rejected It. Here's Why”](https://www.linkedin.com/pulse/your-cv-passed-ats-recruiter-still-rejected-heres-why-zara-ali-bgsdf/), [“You're Applying for the Right Jobs So Why Are You Still Not Getting Interviews?”](https://www.linkedin.com/pulse/youre-applying-right-jobs-so-why-you-still-getting-interviews-ali-ruijf/), and [“I've Applied to More Than 400 Jobs and Nobody Is Calling Me”](https://www.linkedin.com/pulse/ive-applied-more-than-400-jobs-nobody-calling-me-zara-ali-p4fuf/).

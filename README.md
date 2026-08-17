<div align="center">

# Recruiter-Ready CV

An agent skill for creating, repairing, and tailoring ATS-friendly resumes that also persuade human recruiters.

[![Agent Skill](https://img.shields.io/badge/Agent_Skill-SKILL.md-6f42c1?style=flat-square)](https://agentskills.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

[Repository](https://github.com/pypi-ahmad/recruiter-ready-cv) · [Skill instructions](skills/recruiter-ready-cv/SKILL.md) · [Interview checklist](skills/recruiter-ready-cv/references/intake-questionnaire.md) · [LaTeX template](skills/recruiter-ready-cv/assets/ats-resume.tex)

</div>

`recruiter-ready-cv` turns verified career information into a clear, vacancy-aware resume. It combines ATS-safe structure with the evidence, positioning, and clarity a recruiter needs to understand a candidate quickly.

> [!IMPORTANT]
> The skill never invents employers, titles, dates, qualifications, responsibilities, metrics, or outcomes. It improves how verified evidence is presented; it cannot guarantee an interview.

## Table of contents

- [What this skill does](#what-this-skill-does)
- [Workflow modes](#workflow-modes)
- [How it works](#how-it-works)
- [Inputs and privacy](#inputs-and-privacy)
- [Installation](#installation)
  - [Install across detected agents](#install-across-detected-agents)
  - [Install with gh](#install-with-gh)
  - [Product-specific methods](#product-specific-methods)
- [Usage examples](#usage-examples)
- [Deliverables](#deliverables)
- [ATS template and generated files](#ats-template-and-generated-files)
- [Repository structure](#repository-structure)

## What this skill does

Passing an ATS is only the first screening step. A resume can contain the right keywords and still fail when its target, level, achievements, or value are difficult for a recruiter to identify.

This skill addresses both stages:

- Interviews the candidate before creating or revising a resume.
- Converts duty-based descriptions into evidence-led achievements when facts support them.
- Aligns the headline, summary, skills, and experience with the target role.
- Tailors emphasis to a vacancy instead of merely inserting keywords.
- Checks supplied resume and LinkedIn content for positioning inconsistencies.
- Produces copy-ready structured content and an ATS-safe LaTeX source.
- Compiles a PDF when tooling is available and checks its text reading order.

## Workflow modes

| Mode | Starting point | What the skill does | Result |
| --- | --- | --- | --- |
| **Create** | No usable resume or career information only | Conducts the complete interview and confirms every applicable category | New structured resume, `.tex`, and PDF when available |
| **Update** | Existing resume in a supported format | Extracts known facts, confirms them, then asks only about gaps, conflicts, and weak evidence | Revised resume without overwriting the original |
| **Audit** | Existing resume with feedback requested first | Diagnoses recruiter-screening problems, then asks whether to continue into an update | Prioritized findings, followed by an optional revision interview |

## How it works

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

## Inputs and privacy

The skill accepts career information or an existing resume in plain text, Markdown, LaTeX, PDF, or DOCX. Helpful supporting material includes:

- A target job description or representative vacancies.
- Supplied LinkedIn content and professional profile links.
- Portfolio, GitHub, project, publication, or performance-review evidence.
- Education, certification, award, volunteering, and language information.

> [!NOTE]
> The interview does not request age, date of birth, marital status, government identifiers, a full street address, salary history, references, or a photograph unless the candidate explicitly requires a market-specific version. Live profiles are not treated as reviewed unless their content is supplied or access is authorized.

## Installation

### Install across detected agents

The recommended installer requires Node.js 18 or later. It detects supported agents already installed on the machine and prompts for the destinations:

Install for the current project:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill recruiter-ready-cv
```

Install globally across projects:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill recruiter-ready-cv --global
```

Install non-interactively for every detected agent:

```shell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill recruiter-ready-cv --agent '*' --global --yes
```

On Windows, use independent copies when filesystem links are unavailable:

```powershell
npx skills add https://github.com/pypi-ahmad/recruiter-ready-cv --skill recruiter-ready-cv --agent '*' --global --copy --yes
```

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
gh skill preview pypi-ahmad/recruiter-ready-cv recruiter-ready-cv
```

GitHub's `gh` tool 2.90 or later can install the skill for a specific agent. Replace `<agent>` with an ID from the table:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent <agent> --scope user
```

| Agent | `gh skill` ID | Native personal location | Invocation |
| --- | --- | --- | --- |
| GitHub Copilot | `github-copilot` | `~/.copilot/skills/recruiter-ready-cv/` | Automatic or `/recruiter-ready-cv` |
| Codex | `codex` | `~/.agents/skills/recruiter-ready-cv/` | `$recruiter-ready-cv` |
| Claude Code | `claude-code` | `~/.claude/skills/recruiter-ready-cv/` | Automatic or `/recruiter-ready-cv` |
| OpenCode | `opencode` | `~/.config/opencode/skills/recruiter-ready-cv/` | Automatic or `/recruiter-ready-cv` |
| xAI Grok Build | `grok` | `~/.grok/skills/recruiter-ready-cv/` | Automatic or `/recruiter-ready-cv` |

To install for one repository instead, run the command from that repository and replace `--scope user` with `--scope project`.

### Product-specific methods

#### GitHub Copilot

Install for Copilot, the Copilot app, or supported IDE agent modes:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent github-copilot --scope user
```

Project installations are available to repository-aware Copilot surfaces, including the cloud agent and code review. See GitHub's official [agent skills documentation](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills).

#### Codex and ChatGPT

Install into the Agent Skills user directory:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent codex --scope user
```

Codex can invoke it as `$recruiter-ready-cv`. In the ChatGPT desktop app, open **Skills** in the sidebar and use `@` to select an available skill. If it does not appear after installation, restart the application.

> [!NOTE]
> A raw GitHub skill is not a direct install package for ChatGPT on the web or mobile. OpenAI documents plugin packaging and publication as the distribution route for those surfaces. See the official [OpenAI skills documentation](https://developers.openai.com/codex/skills).

#### Claude Code and Claude

For Claude Code, Desktop, VS Code, or JetBrains:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent claude-code --scope user
```

Claude Code discovers personal skills under `~/.claude/skills` and can invoke this one as `/recruiter-ready-cv`. See the official [Claude Code skills documentation](https://code.claude.com/docs/en/skills).

For Claude on the web or in the Claude app, create an upload-ready ZIP:

```shell
git clone --depth 1 https://github.com/pypi-ahmad/recruiter-ready-cv.git recruiter-ready-cv
git -C recruiter-ready-cv archive --format=zip --prefix=recruiter-ready-cv/ -o ../recruiter-ready-cv.zip HEAD:skills/recruiter-ready-cv
```

Then open **Customize → Skills**, choose **Create skill → Upload a skill**, and upload `recruiter-ready-cv.zip`. Code execution and file creation must be enabled. See Anthropic's official [custom skills guide](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

#### OpenCode

Install for OpenCode sessions:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent opencode --scope user
```

OpenCode also discovers compatible skills from `.agents/skills` and `.claude/skills`. See the official [OpenCode skills documentation](https://opencode.ai/docs/skills/).

#### xAI Grok Build

Install for xAI's official Grok Build terminal agent:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent grok --scope user
```

Run `/skills` to list discovered skills or `/recruiter-ready-cv` to invoke it. See the official [Grok Build skills documentation](https://github.com/xai-org/grok-build/blob/main/crates/codegen/xai-grok-shell/README.md#skills).

## Usage examples

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

## Deliverables

The default workflow returns:

1. A recruiter-screen verdict.
2. Prioritized findings for an existing resume.
3. A candidate-confirmed fact summary.
4. Polished, copy-ready resume content.
5. Explicit evidence gaps that still need candidate input.
6. Vacancy and LinkedIn alignment checks when source material is supplied.
7. Generated `.tex` and `.pdf` files when compilation is available.

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
    └── recruiter-ready-cv/
        ├── SKILL.md
        ├── agents/
        │   └── openai.yaml
        ├── assets/
        │   └── ats-resume.tex
        └── references/
            └── intake-questionnaire.md
```

The workflow distills recruiter-screening principles from Zara Ali's “Your CV Passed the ATS. The Recruiter Still Rejected It. Here's Why” (August 17, 2026).

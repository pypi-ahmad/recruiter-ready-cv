<div align="center">

# Recruiter-Ready CV

An agent skill for creating, repairing, and tailoring ATS-friendly CVs that also persuade human recruiters.

[![Agent Skill](https://img.shields.io/badge/Agent_Skill-SKILL.md-6f42c1?style=flat-square)](https://agentskills.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

[Repository](https://github.com/pypi-ahmad/recruiter-ready-cv) · [Skill instructions](skills/recruiter-ready-cv/SKILL.md) · [Interview checklist](skills/recruiter-ready-cv/references/intake-questionnaire.md) · [LaTeX template](skills/recruiter-ready-cv/assets/ats-resume.tex)

</div>

`recruiter-ready-cv` helps an AI coding agent turn verified career information into a clear, vacancy-aware CV. It conducts a comprehensive adaptive interview before creating a new resume, extracts and confirms facts before updating an existing one, or provides an audit before offering to continue into a revision.

> [!IMPORTANT]
> The skill must not invent employers, titles, dates, qualifications, responsibilities, metrics, or outcomes. It improves how verified evidence is presented; it cannot guarantee an interview.

## What it does

- Creates a CV from scratch through a comprehensive, completion-gated interview.
- Extracts and confirms known facts before asking only about gaps in an existing resume.
- Rewrites duty-based bullets as evidence-led achievements when the facts support them.
- Aligns the headline, summary, skills, and experience with a target role.
- Tailors emphasis to a vacancy instead of merely adding keywords.
- Checks supplied CV and LinkedIn content for positioning inconsistencies.
- Produces copy-ready structured content and a sanitized, single-column `.tex` file.
- Compiles a PDF with `pdflatex` when available and verifies its ATS reading order through text extraction.

## How the interview works

The skill asks 3--5 related questions at a time and completes one resume section or employment role before moving to the next. It covers every applicable resume category while skipping information already supplied.

Each detail is tracked as verified, unknown/skipped, not applicable, or conflicting. Unknown information is disclosed rather than invented, and material conflicts must be resolved. Before drafting, the candidate receives a concise fact summary to correct or approve.

For an existing resume, the skill first extracts its dates, titles, education, and major claims. It confirms that inventory, then asks only about missing evidence, weak achievements, inconsistencies, and target-role alignment. An audit-only request receives the audit first and an invitation to continue into the update workflow.

If the candidate requests an early draft, the skill labels it as incomplete, keeps evidence gaps visible, and continues the interview. Without a job description, it creates a strong general version for the stated target and discloses the limits of vacancy-specific tailoring.

## Inputs and privacy

The skill accepts career information or an existing resume in plain text, Markdown, LaTeX, PDF, or DOCX. A job description, supplied LinkedIn content, portfolio, project list, or performance review can provide additional evidence and targeting context.

> [!NOTE]
> It does not request age, date of birth, marital status, government identifiers, a full street address, salary history, references, or a photograph unless the candidate explicitly requires a market-specific version. Live profiles are not treated as reviewed unless their content is supplied or access is authorized.

## Install

Review the skill before installing it:

```shell
gh skill preview pypi-ahmad/recruiter-ready-cv recruiter-ready-cv
```

GitHub CLI 2.90 or later can install the skill for several supported agents. Replace `<agent>` with an ID from the table:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent <agent> --scope user
```

| Agent | `gh skill` ID | Native personal location | Invocation |
| --- | --- | --- | --- |
| GitHub Copilot | `github-copilot` | `~/.copilot/skills/recruiter-ready-cv/` | Automatic or `/recruiter-ready-cv` |
| Codex CLI | `codex` | `~/.agents/skills/recruiter-ready-cv/` | `$recruiter-ready-cv` |
| Claude Code | `claude-code` | `~/.claude/skills/recruiter-ready-cv/` | Automatic or `/recruiter-ready-cv` |
| OpenCode | `opencode` | `~/.config/opencode/skills/recruiter-ready-cv/` | Automatic or `/recruiter-ready-cv` |
| xAI Grok Build | `grok` | `~/.grok/skills/recruiter-ready-cv/` | Automatic or `/recruiter-ready-cv` |

To install for one repository instead, run the command from that repository and replace `--scope user` with `--scope project`.

### GitHub Copilot

Install for Copilot CLI, the Copilot app, or supported IDE agent modes:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent github-copilot --scope user
```

Project installations are available to repository-aware Copilot surfaces, including the cloud agent and code review. See GitHub's official [agent skills documentation](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills).

### Codex CLI and ChatGPT

Install into the Agent Skills user directory:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent codex --scope user
```

Codex can invoke it as `$recruiter-ready-cv`. In the ChatGPT desktop app, open **Skills** in the sidebar and use `@` to select an available skill. If it does not appear after installation, restart the application.

> [!NOTE]
> A raw GitHub skill is not a direct install package for ChatGPT on the web or mobile. OpenAI documents plugin packaging and publication as the distribution route for those surfaces. See the official [OpenAI skills documentation](https://developers.openai.com/codex/skills).

### Claude Code and Claude UI

For Claude Code CLI, Desktop, VS Code, or JetBrains:

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

### OpenCode

Install for both OpenCode CLI and UI sessions:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent opencode --scope user
```

OpenCode also discovers compatible skills from `.agents/skills` and `.claude/skills`. See the official [OpenCode skills documentation](https://opencode.ai/docs/skills/).

### xAI Grok Build CLI

Install for xAI's official Grok Build terminal agent:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv recruiter-ready-cv --agent grok --scope user
```

Run `/skills` to list discovered skills or `/recruiter-ready-cv` to invoke it. See the official [Grok Build skills documentation](https://github.com/xai-org/grok-build/blob/main/crates/codegen/xai-grok-shell/README.md#skills).

## Use

Create a new CV:

```text
Use recruiter-ready-cv to interview me comprehensively and create a CV for a senior data engineer role. Produce structured content, a LaTeX file, and a PDF.
```

Repair an existing CV:

```text
Use recruiter-ready-cv to extract and confirm the facts in this CV, interview me about every relevant gap, and produce a revised resume without inventing facts.
```

Tailor to a vacancy:

```text
Use recruiter-ready-cv to tailor my CV to this job description. Show the evidence gaps and make the strongest relevant experience easy to find.
```

Audit before deciding whether to revise:

```text
Use recruiter-ready-cv to audit this resume only. Show the highest-impact recruiter-screening problems, then ask whether I want to continue with an update interview.
```

## Output

The default workflow returns:

1. A recruiter-screen verdict.
2. Prioritized findings for an existing CV.
3. A candidate-confirmed fact summary.
4. Polished, copy-ready CV content.
5. Explicit evidence gaps that still need candidate input.
6. Vacancy and LinkedIn alignment checks when source material is supplied.
7. Generated `.tex` and `.pdf` files based on the bundled ATS-friendly template when compilation is available.

## Template and files

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

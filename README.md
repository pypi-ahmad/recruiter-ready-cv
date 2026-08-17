<div align="center">

# Recruiter-Ready CV

An agent skill for creating, repairing, and tailoring ATS-friendly CVs that also persuade human recruiters.

[![Agent Skill](https://img.shields.io/badge/Agent_Skill-SKILL.md-6f42c1?style=flat-square)](https://agentskills.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

[Repository](https://github.com/pypi-ahmad/recruiter-ready-cv) · [Skill instructions](SKILL.md) · [LaTeX template](assets/ats-resume.tex)

</div>

`recruiter-ready-cv` helps an AI coding agent turn verified career information into a clear, vacancy-aware CV. It can interview a candidate before creating a new CV, diagnose and repair an existing one, or provide a recruiter-focused audit without rewriting.

> [!IMPORTANT]
> The skill must not invent employers, titles, dates, qualifications, responsibilities, metrics, or outcomes. It improves how verified evidence is presented; it cannot guarantee an interview.

## What it does

- Creates a CV from scratch through a focused, interview-first intake.
- Rewrites duty-based bullets as evidence-led achievements when the facts support them.
- Aligns the headline, summary, skills, and experience with a target role.
- Tailors emphasis to a vacancy instead of merely adding keywords.
- Checks supplied CV and LinkedIn content for positioning inconsistencies.
- Produces copy-ready structured content and an ATS-friendly, single-column `.tex` file.
- Compiles with `pdflatex` when available and can adapt to `xelatex` for broader Unicode support.

## Install

Review the skill before installing it:

```shell
gh skill preview pypi-ahmad/recruiter-ready-cv SKILL.md
```

GitHub CLI 2.90 or later can install the root-level skill for several supported agents. Replace `<agent>` with an ID from the table:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv SKILL.md --agent <agent> --scope user
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
gh skill install pypi-ahmad/recruiter-ready-cv SKILL.md --agent github-copilot --scope user
```

Project installations are available to repository-aware Copilot surfaces, including the cloud agent and code review. See GitHub's official [agent skills documentation](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills).

### Codex CLI and ChatGPT

Install into the Agent Skills user directory:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv SKILL.md --agent codex --scope user
```

Codex can invoke it as `$recruiter-ready-cv`. In the ChatGPT desktop app, open **Skills** in the sidebar and use `@` to select an available skill. If it does not appear after installation, restart the application.

> [!NOTE]
> A raw GitHub skill is not a direct install package for ChatGPT on the web or mobile. OpenAI documents plugin packaging and publication as the distribution route for those surfaces. See the official [OpenAI skills documentation](https://developers.openai.com/codex/skills).

### Claude Code and Claude UI

For Claude Code CLI, Desktop, VS Code, or JetBrains:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv SKILL.md --agent claude-code --scope user
```

Claude Code discovers personal skills under `~/.claude/skills` and can invoke this one as `/recruiter-ready-cv`. See the official [Claude Code skills documentation](https://code.claude.com/docs/en/skills).

For Claude on the web or in the Claude app, create an upload-ready ZIP:

```shell
git clone --depth 1 https://github.com/pypi-ahmad/recruiter-ready-cv.git recruiter-ready-cv
git -C recruiter-ready-cv archive --format=zip --prefix=recruiter-ready-cv/ -o ../recruiter-ready-cv.zip HEAD
```

Then open **Customize → Skills**, choose **Create skill → Upload a skill**, and upload `recruiter-ready-cv.zip`. Code execution and file creation must be enabled. See Anthropic's official [custom skills guide](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

### OpenCode

Install for both OpenCode CLI and UI sessions:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv SKILL.md --agent opencode --scope user
```

OpenCode also discovers compatible skills from `.agents/skills` and `.claude/skills`. See the official [OpenCode skills documentation](https://opencode.ai/docs/skills/).

### xAI Grok Build CLI

Install for xAI's official Grok Build terminal agent:

```shell
gh skill install pypi-ahmad/recruiter-ready-cv SKILL.md --agent grok --scope user
```

Run `/skills` to list discovered skills or `/recruiter-ready-cv` to invoke it. See the official [Grok Build skills documentation](https://github.com/xai-org/grok-build/blob/main/crates/codegen/xai-grok-shell/README.md#skills).

## Use

Create a new CV:

```text
Use recruiter-ready-cv to interview me and create a CV for a senior data engineer role. Produce structured content and a LaTeX file.
```

Repair an existing CV:

```text
Use recruiter-ready-cv to audit this CV from a recruiter's perspective, identify the highest-impact problems, and rewrite it without inventing facts.
```

Tailor to a vacancy:

```text
Use recruiter-ready-cv to tailor my CV to this job description. Show the evidence gaps and make the strongest relevant experience easy to find.
```

## Output

The default workflow returns:

1. A recruiter-screen verdict.
2. Prioritized findings for an existing CV.
3. Polished, copy-ready CV content.
4. Explicit evidence gaps that still need candidate input.
5. Vacancy and LinkedIn alignment checks when source material is supplied.
6. A generated `.tex` file based on the bundled ATS-friendly template.

## Repository structure

```text
recruiter-ready-cv/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── assets/
    └── ats-resume.tex
```

The workflow distills recruiter-screening principles from Zara Ali's “Your CV Passed the ATS. The Recruiter Still Rejected It. Here's Why” (August 17, 2026).

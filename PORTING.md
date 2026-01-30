# Porting Documentation

This document describes the fork of [awesome-llm-skills](https://github.com/Prat011/awesome-llm-skills) to create **Awesome Junie Skills** - a collection of skills specifically targeted for Junie by JetBrains.

## Overview

This repository is a fork of the original `awesome-llm-skills` project, modified to target **Junie** (JetBrains' AI coding assistant) instead of Claude/Anthropic. The default underlying model for Junie skills is **GEMINI_3_0_FLASH**.

## Fork Details

- **Original Repository:** https://github.com/Prat011/awesome-llm-skills
- **Original Branch:** `master`
- **Fork Branch:** `junie`

## Remote Repositories

This fork is maintained across multiple remotes:

| Remote Name | URL | Purpose |
|-------------|-----|---------|
| `origin` | https://github.com/Prat011/awesome-llm-skills | Original upstream repository |
| `github-remote` | git@github.com:OpenTasmania/awesome-junie-skills.git | GitHub fork |
| `junie-remote` | git@gitlab.com:opentasmania/awesome-junie-skills.git | GitLab mirror |

## Porting Method

The porting process involved the following systematic changes:

### 1. Branding Changes

- **Project Name:** "Awesome LLM Skills" → "Awesome Junie Skills"
- **Target Platform:** Claude/Anthropic → Junie/JetBrains
- **Default Model:** Specified as GEMINI_3_0_FLASH

### 2. Directory Structure Changes

- **Skill Discovery Paths:**
  - `.claude/skills/` → `.junie/skills/`
  - `~/.claude/skills/` → `~/.junie/skills/`

### 3. Documentation Updates

The following files were modified:

#### README.md
- Updated title and description to reference Junie
- Changed "What Are LLM Skills?" to "What Are Junie Skills?"
- Updated Quick Start guide for Junie and JetBrains IDEs
- Replaced multi-platform section with single Junie (JetBrains) platform
- Updated all skill descriptions that referenced Claude to reference Junie
- Changed document-skills links from anthropics/skills to local paths
- Updated Resources section with JetBrains documentation links
- Updated Contributing section for Junie testing

#### CONTRIBUTING.md
- Updated testing requirements to reference Junie instead of Claude Code, Codex, Gemini CLI

#### skill-creator/SKILL.md
- Replaced all Claude references with Junie throughout the skill creation guide

### 4. External Links

- Links to `github.com/anthropics/skills` were updated to reference local skill directories where applicable
- Resource links updated to point to JetBrains documentation
- Community resources updated to reference JetBrains community and this repository

### 5. Brand Guidelines

- References to "Anthropic's official brand" changed to "JetBrains official brand"

## Files Modified

### Core Documentation
1. `README.md` - Main documentation, added disclaimer for external Claude-named skills
2. `CONTRIBUTING.md` - Contribution guidelines, updated header and testing requirements
3. `skill-creator/SKILL.md` - Skill creation guide
4. `PORTING.md` - This document (new)

### Document Skills
5. `document-skills/docx/SKILL.md` - Claude → Junie in description
6. `document-skills/docx/ooxml.md` - Claude → Junie in author attributes and examples
7. `document-skills/pdf/SKILL.md` - Claude → Junie in description
8. `document-skills/pptx/SKILL.md` - Claude → Junie in description
9. `document-skills/xlsx/SKILL.md` - Claude → Junie in description

### Notion Skills
10. `notion-knowledge-capture/evaluations/README.md` - Claude models → Junie
11. `notion-meeting-intelligence/SKILL.md` - All Claude research references → Junie
12. `notion-meeting-intelligence/evaluations/README.md` - Claude → Junie throughout
13. `notion-meeting-intelligence/examples/customer-meeting.md` - Claude → Junie
14. `notion-meeting-intelligence/examples/executive-review.md` - Claude → Junie
15. `notion-meeting-intelligence/reference/template-selection-guide.md` - Claude → Junie
16. `notion-research-documentation/evaluations/README.md` - Claude → Junie
17. `notion-spec-to-implementation/SKILL.md` - Claude code → Junie
18. `notion-spec-to-implementation/evaluations/README.md` - Claude → Junie

### Creative Skills
19. `algorithmic-art/SKILL.md` - Complete rebrand from Anthropic to JetBrains, claude.ai artifacts → standalone HTML
20. `artifacts-builder/SKILL.md` - Repurposed from claude.ai artifacts to standalone HTML applications
21. `brand-guidelines/SKILL.md` - Complete rewrite with JetBrains brand colors, typography, and identity
22. `canvas-design/SKILL.md` - Claude → Junie references

### Other Skills
23. `content-research-writer/SKILL.md` - Claude Code → Junie, web Claude → JetBrains IDE
24. `template-skill/SKILL.md` - Claude → Junie in description
25. `meeting-insights-analyzer/SKILL.md` - Claude Code → Junie
26. `internal-comms/SKILL.md` - Claude → Junie in description
27. `file-organizer/SKILL.md` - Claude Code → Junie, Claude → Junie
28. `invoice-organizer/SKILL.md` - Claude Code → Junie

### Unchanged (Technical SDK References)
- `mcp-builder/reference/evaluation.md` - Contains Anthropic SDK/API references (pip install anthropic, ANTHROPIC_API_KEY) - these are technical package names, not branding
- `mcp-builder/reference/mcp_best_practices.md` - References Claude Desktop as an example MCP client - technical reference

## Maintaining the Fork

To sync with upstream changes from the original repository:

```bash
# Fetch upstream changes
git fetch origin

# Merge upstream master into junie branch (resolve conflicts as needed)
git merge origin/master

# Re-apply Junie-specific changes if overwritten
```

## Contributing

When contributing to this fork:

1. Ensure all new content references Junie instead of Claude
2. Use `.junie/` directory paths instead of `.claude/`
3. Test skills with Junie in JetBrains IDEs
4. Follow the existing porting conventions established in this document

## License

This fork maintains the same Apache License 2.0 as the original repository.

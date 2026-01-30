<h1 align="center">Awesome Junie Skills</h1>

<p align="center">
  <strong>🔀 This is a PORT of <a href="https://github.com/Prat011/awesome-llm-skills">awesome-llm-skills</a> from Claude/Anthropic to Junie/JetBrains</strong>
</p>

<p align="center">
  <a href="url">
  <img width="1280" height="640" alt="Awesome Junie Skills" src="https://github.com/user-attachments/assets/fb10b4c7-4155-4026-95b9-b4b979a14921" />
  </a>

</p>


<p align="center">
  A curated list of awesome Junie Skills, resources, and tools for customizing AI workflows with Junie by JetBrains.
</p>

<p align="center">
  <em>Ported from the original <a href="https://github.com/Prat011/awesome-llm-skills">Prat011/awesome-llm-skills</a> repository.<br/>
  See <a href="PORTING.md">PORTING.md</a> for details on the porting process and changes made.</em>
</p>


<p align="center">
  <a href="https://awesome.re">
    <img src="https://awesome.re/badge.svg" alt="Awesome" />
  </a>
  <a href="https://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs Welcome" />
  </a>
  <a href="https://www.apache.org/licenses/LICENSE-2.0">
    <img src="https://img.shields.io/badge/License-Apache_2.0-blue.svg?style=flat-square" alt="License: Apache-2.0" />
  </a>
</p>


## Contents

- [What Are Junie Skills?](#what-are-junie-skills)
- [Quick Start](#quick-start)
- [Skills](#skills)
- [Platform](#platform)
  - [Junie (JetBrains)](#junie-jetbrains)
- [Contributing](#contributing)
  - [Quick Contribution Steps](#quick-contribution-steps)
- [Resources](#resources)
  - [Official Documentation](#official-documentation)
  - [Community Resources](#community-resources)
- [License](#license)


## What Are Junie Skills?

Junie Skills are customizable workflows that teach Junie how to perform specific tasks according to your unique requirements. Skills enable Junie to execute tasks in a repeatable, standardized manner within JetBrains IDEs. By default, Junie uses **GEMINI_3_0_FLASH** as its underlying model.

## Quick Start

1. **Create a project-local or user-level skill folder**
   Use one of these discovery paths so Junie finds it automatically:

   * Project: `.junie/skills/webapp-testing/`
   * User: `~/.junie/skills/webapp-testing/`

2. **Add `SKILL.md`** (required)

  Basic Skill Template:
  
  ```markdown
  ---
  name: my-skill-name
  description: A clear description of what this skill does and when to use it.
  ---
  
  # My Skill Name
  
  Detailed description of the skill's purpose and capabilities.
  
  ## When to Use This Skill
  
  - Use case 1
  - Use case 2
  - Use case 3
  
  ## Instructions
  
  [Detailed instructions for Junie on how to execute this skill]
  
  ## Examples
  
  [Real-world examples showing the skill in action]
  ```

  - Focus on specific, repeatable tasks
  - Include clear examples and edge cases
  - Write instructions for Junie, not end users
  - Document prerequisites and dependencies
  - Include error handling guidance

3. **Keep supporting files small**
   Add only what's needed (e.g., small fixtures in `resources/`, helper scripts). This keeps skills snappy to load and easier for Junie to apply.

4. **Load the skill**

   Place the folder under `.junie/skills/` (project) or `~/.junie/skills/` (user). Junie discovers skills from these locations within your JetBrains IDE.
  
5. **Use it**
   Just ask in natural language, optionally mentioning the skill by name—for example:
   "Use the **Webapp Testing** skill to validate the checkout flow and generate `report.md`." Junie can auto-invoke relevant skills based on your request.

## Skills

> **Note:** Some external skills linked below were originally created for Claude/Anthropic and may contain "claude" in their repository names. These skills are generally compatible with Junie and other LLM-based coding assistants, though some may require minor adaptations.

### Skills with MCP

- [Notion Knowledge Capture](./notion-knowledge-capture/) - Converts chats and decisions into structured Notion pages and database entries with proper linking.
- [Notion Meeting Intelligence](./notion-meeting-intelligence/) - Preps meetings from Notion context and creates internal pre-reads plus external agendas.
- [Notion Research Documentation](./notion-research-documentation/) - Searches Notion, synthesizes multiple pages, and writes cited research docs back to Notion.
- [Notion Spec To Implementation](./notion-spec-to-implementation/) - Turns Notion specs into task plans with acceptance criteria and progress tracking.

### Document Processing

- [docx](./document-skills/docx) - Create, edit, analyze Word docs with tracked changes, comments, formatting.
- [pdf](./document-skills/pdf) - Extract text, tables, metadata, merge & annotate PDFs.
- [pptx](./document-skills/pptx) - Read, generate, and adjust slides, layouts, templates.
- [xlsx](./document-skills/xlsx) - Spreadsheet manipulation: formulas, charts, data transformations.
- [Markdown to EPUB Converter](https://github.com/smerchek/claude-epub-skill) - Converts markdown documents and chat summaries into professional EPUB ebook files. *By [@smerchek](https://github.com/smerchek)*

### Development & Code Tools

- [artifacts-builder](./artifacts-builder/) - Suite of tools for creating elaborate, multi-component HTML artifacts using modern frontend web technologies (React, Tailwind CSS, shadcn/ui).
- [aws-skills](https://github.com/zxkane/aws-skills) - AWS development with CDK best practices, cost optimization MCP servers, and serverless/event-driven architecture patterns.
- [Changelog Generator](./changelog-generator/) - Automatically creates user-facing changelogs from git commits by analyzing history and transforming technical commits into customer-friendly release notes.
- [D3.js Visualization](https://github.com/chrisvoncsefalvay/claude-d3js-skill) - Teaches Junie to produce D3 charts and interactive data visualizations. *By [@chrisvoncsefalvay](https://github.com/chrisvoncsefalvay)*
- [FFUF Web Fuzzing](https://github.com/jthack/ffuf_claude_skill) - Integrates the ffuf web fuzzer so Junie can run fuzzing tasks and analyze results for vulnerabilities. *By [@jthack](https://github.com/jthack)*
- [finishing-a-development-branch](https://github.com/obra/superpowers/tree/main/skills/finishing-a-development-branch) - Guides completion of development work by presenting clear options and handling chosen workflow.
- [iOS Simulator](https://github.com/conorluddy/ios-simulator-skill) - Enables Junie to interact with iOS Simulator for testing and debugging iOS applications. *By [@conorluddy](https://github.com/conorluddy)*
- [MCP Builder](./mcp-builder/) - Guides creation of high-quality MCP (Model Context Protocol) servers for integrating external APIs and services with LLMs using Python or TypeScript.
- [move-code-quality-skill](https://github.com/1NickPappas/move-code-quality-skill) - Analyzes Move language packages against the official Move Book Code Quality Checklist for Move 2024 Edition compliance and best practices.
- [Playwright Browser Automation](https://github.com/lackeyjb/playwright-skill) - Model-invoked Playwright automation for testing and validating web applications. *By [@lackeyjb](https://github.com/lackeyjb)*
- [pypict-junie-skill](https://github.com/omkamal/pypict-claude-skill) - Design comprehensive test cases using PICT (Pairwise Independent Combinatorial Testing) for requirements or code, generating optimized test suites with pairwise coverage.
- [Skill Creator](./skill-creator/) - Provides guidance for creating effective Junie Skills that extend capabilities with specialized knowledge, workflows, and tool integrations.
- [Skill Seekers](https://github.com/yusufkaraaslan/Skill_Seekers) - Automatically converts any documentation website into a Junie skill in minutes. *By [@yusufkaraaslan](https://github.com/yusufkaraaslan)*
- [test-driven-development](https://github.com/obra/superpowers/tree/main/skills/test-driven-development) - Use when implementing any feature or bugfix, before writing implementation code.
- [using-git-worktrees](https://github.com/obra/superpowers/blob/main/skills/using-git-worktrees/) - Creates isolated git worktrees with smart directory selection and safety verification.
- [Webapp Testing](./webapp-testing/) - Tests local web applications using Playwright for verifying frontend functionality, debugging UI behavior, and capturing screenshots.

### Data & Analysis

- [CSV Data Summarizer](https://github.com/coffeefuelbump/csv-data-summarizer-claude-skill) - Automatically analyzes CSV files and generates comprehensive insights with visualizations without requiring user prompts. *By [@coffeefuelbump](https://github.com/coffeefuelbump)*
- [postgres](https://github.com/sanjay3290/ai-skills/tree/main/skills/postgres) - Execute safe read-only SQL queries against PostgreSQL databases with multi-connection support and defense-in-depth security. *By [@sanjay3290](https://github.com/sanjay3290)*
- [root-cause-tracing](https://github.com/obra/superpowers/tree/main/skills/root-cause-tracing) - Use when errors occur deep in execution and you need to trace back to find the original trigger.

### Business & Marketing

- [Brand Guidelines](./brand-guidelines/) - Applies JetBrains official brand colors and typography to artifacts for consistent visual identity and professional design standards.
- [Competitive Ads Extractor](./competitive-ads-extractor/) - Extracts and analyzes competitors' ads from ad libraries to understand messaging and creative approaches that resonate.
- [Domain Name Brainstormer](./domain-name-brainstormer/) - Generates creative domain name ideas and checks availability across multiple TLDs including .com, .io, .dev, and .ai extensions.
- [Internal Comms](./internal-comms/) - Helps write internal communications including 3P updates, company newsletters, FAQs, status reports, and project updates using company-specific formats.
- [Lead Research Assistant](./lead-research-assistant/) - Identifies and qualifies high-quality leads by analyzing your product, searching for target companies, and providing actionable outreach strategies.

### Communication & Writing

- [article-extractor](https://github.com/michalparkola/tapestry-skills-for-claude-code/tree/main/article-extractor) - Extract full article text and metadata from web pages.
- [brainstorming](https://github.com/obra/superpowers/tree/main/skills/brainstorming) - Transform rough ideas into fully-formed designs through structured questioning and alternative exploration.
- [Content Research Writer](./content-research-writer/) - Assists in writing high-quality content by conducting research, adding citations, improving hooks, and providing section-by-section feedback.
- [family-history-research](https://github.com/emaynard/claude-family-history-research-skill) - Provides assistance with planning family history and genealogy research projects.
- [Meeting Insights Analyzer](./meeting-insights-analyzer/) - Analyzes meeting transcripts to uncover behavioral patterns including conflict avoidance, speaking ratios, filler words, and leadership style.
- [NotebookLM Integration](https://github.com/PleasePrompto/notebooklm-skill) - Lets Junie chat directly with NotebookLM for source-grounded answers based exclusively on uploaded documents. *By [@PleasePrompto](https://github.com/PleasePrompto)*

### Creative & Media

- [Canvas Design](./canvas-design/) - Creates beautiful visual art in PNG and PDF documents using design philosophy and aesthetic principles for posters, designs, and static pieces.
- [imagen](https://github.com/sanjay3290/ai-skills/tree/main/skills/imagen) - Generate images using Google Gemini's image generation API for UI mockups, icons, illustrations, and visual assets. *By [@sanjay3290](https://github.com/sanjay3290)*
- [Image Enhancer](./image-enhancer/) - Improves image and screenshot quality by enhancing resolution, sharpness, and clarity for professional presentations and documentation.
- [Slack GIF Creator](./slack-gif-creator/) - Creates animated GIFs optimized for Slack with validators for size constraints and composable animation primitives.
- [Theme Factory](./theme-factory/) - Applies professional font and color themes to artifacts including slides, docs, reports, and HTML landing pages with 10 pre-set themes.
- [Video Downloader](./video-downloader/) - Downloads videos from YouTube and other platforms for offline viewing, editing, or archival with support for various formats and quality options.
- [youtube-transcript](https://github.com/michalparkola/tapestry-skills-for-claude-code/tree/main/youtube-transcript) - Fetch transcripts from YouTube videos and prepare summaries.

### Productivity & Organization

- [File Organizer](./file-organizer/) - Intelligently organizes files and folders by understanding context, finding duplicates, and suggesting better organizational structures.
- [Invoice Organizer](./invoice-organizer/) - Automatically organizes invoices and receipts for tax preparation by reading files, extracting information, and renaming consistently.
- [Raffle Winner Picker](./raffle-winner-picker/) - Randomly selects winners from lists, spreadsheets, or Google Sheets for giveaways and contests with cryptographically secure randomness.
- [ship-learn-next](https://github.com/michalparkola/tapestry-skills-for-claude-code/tree/main/ship-learn-next) - Skill to help iterate on what to build or learn next, based on feedback loops.
- [tapestry](https://github.com/michalparkola/tapestry-skills-for-claude-code/tree/main/tapestry) - Interlink and summarize related documents into knowledge networks.

### Collaboration & Project Management

- [git-pushing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/git-pushing) - Automate git operations and repository interactions.
- [review-implementing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/review-implementing) - Evaluate code implementation plans and align with specs.
- [test-fixing](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/engineering-workflow-plugin/skills/test-fixing) - Detect failing tests and propose patches or fixes.

### Security & Systems

- [computer-forensics](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/computer-forensics-skills/skills/computer-forensics) - Digital forensics analysis and investigation techniques.
- [file-deletion](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/computer-forensics-skills/skills/file-deletion) - Secure file deletion and data sanitization methods.
- [metadata-extraction](https://github.com/mhattingpete/claude-skills-marketplace/tree/main/computer-forensics-skills/skills/metadata-extraction) - Extract and analyze file metadata for forensic purposes.
- [threat-hunting-with-sigma-rules](https://github.com/jthack/threat-hunting-with-sigma-rules-skill) - Use Sigma detection rules to hunt for threats and analyze security events.

## Platform

### Junie (JetBrains)

**Set‑up and enable skills**

* **Installation:** Junie is available as a plugin for JetBrains IDEs (IntelliJ IDEA, PyCharm, WebStorm, etc.). Install it from the JetBrains Marketplace or via Settings → Plugins → Marketplace → Search "Junie".
* **Getting Started:** Once installed, Junie automatically discovers skills from `.junie/skills/` (project) or `~/.junie/skills/` (user) directories. Junie uses **GEMINI_3_0_FLASH** as its default underlying model.
* **Using Skills:** Just describe what you need in natural language within your JetBrains IDE. Junie activates relevant skills automatically based on your request context and project structure.



## Contributing

We welcome contributions! Please read our [Contributing Guidelines](CONTRIBUTING.md) for details on:

- How to submit new skills
- Skill quality standards
- Pull request process
- Code of conduct

### Quick Contribution Steps

1. Ensure your skill is based on a real use case
2. Check for duplicates in existing skills
3. Follow the skill structure template
4. Test your skill with Junie in your JetBrains IDE
5. Submit a pull request with clear documentation

## Resources

### Official Documentation

- [Junie Overview](https://www.jetbrains.com/junie/) - Official Junie product page
- [JetBrains AI Documentation](https://www.jetbrains.com/help/idea/ai-assistant.html) - AI features in JetBrains IDEs
- [JetBrains Marketplace](https://plugins.jetbrains.com/) - Plugin marketplace for JetBrains IDEs

### Community Resources

- [JetBrains Community](https://intellij-support.jetbrains.com/hc/en-us/community/topics) - Discuss with other JetBrains users
- [Awesome Junie Skills Repository](https://gitlab.com/opentasmania/awesome-junie-skills) - This repository - community skills for Junie
- [Notion Skills](https://www.notion.so/notiondevs/Notion-Skills-for-Claude-28da4445d27180c7af1df7d8615723d0) - Notion integration skills

## License

This repository is licensed under the Apache License 2.0.

Individual skills may have different licenses - please check each skill's folder for specific licensing information.

---

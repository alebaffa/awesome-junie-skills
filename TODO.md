# TODO: Remaining Claude/Anthropic References

This document lists the remaining references to Claude/Anthropic that require decisions or significant rework
to complete the port of this repository to Junie/JetBrains.

## Summary

| Item | File | Status |
|------|------|--------|
| 1 | README.md external links | Keep with disclaimer |
| 2 | PORTING.md | No action needed (historical) |

**Completed:** template-skill, brand-guidelines, document-skills, content-research-writer, canvas-design, notion-* skills, algorithmic-art, artifacts-builder (repurposed as webapp-builder)

---

## Files Requiring Updates

### 1. README.md

**References to update:**

- Line 233: Link to "Notion-Skills-for-Claude" (external URL)

**Decision needed:** This is an external link. Consider:

- Keeping as-is (external resource)
- Removing the link
- Finding Junie-equivalent resource

---

### 2. PORTING.md

**Note:** This file intentionally contains Claude/Anthropic references as it documents the porting process. These
references should remain as they describe what was changed.

**Lines with intentional references:**

- Line 32, 38, 39, 50, 51, 56, 59, 69, 96, 97

**No action needed** - these are historical/documentation references.

---

## External Links Containing "Claude"

These are links to external repositories or resources that contain "Claude" in their names:

1. `./README.md:117` - Link to `smerchek/claude-epub-skill`
2. `./README.md:124` - Link to `chrisvoncsefalvay/claude-d3js-skill`
3. `./README.md:125` - Link to `jthack/ffuf_claude_skill`
4. `./README.md:131` - Link to `omkamal/pypict-claude-skill`

**Decision needed:** These are external repositories. Options:

- Keep links as-is (they're external resources)
- Fork and port these skills
- Remove links to Claude-specific external skills

---

## Remaining Work

All implementation work is complete. Only decision-pending items remain (README.md external links - decision made to keep with disclaimer).

---

## Notes

- Most files have been updated
- PORTING.md references are intentional documentation and should not be changed
- Implementation plans for remaining items are documented below in the Special Notes section

---

## Special Notes: Detailed Analysis

### 1. PORTING.md Intentional References (No Action Needed)

The `PORTING.md` file is a **documentation artifact** that describes the fork process itself. It intentionally contains
references to Claude/Anthropic because:

- It documents **what was changed** during the porting process
- It serves as a **historical record** of the original repository
- It provides **guidance for future maintainers** on how to handle upstream merges
- It explains the **relationship between this fork and the original**

**Specific intentional references (lines):**

- Line 3: "modified to target Junie... instead of Claude/Anthropic"
- Line 32: Documents "Claude/Anthropic → Junie/JetBrains" change
- Lines 38-39: Documents ".claude/skills/" → ".junie/skills/" path changes
- Lines 50-51: Documents README.md changes from Claude to Junie
- Line 56: Documents CONTRIBUTING.md changes
- Line 59: Documents skill-creator/SKILL.md changes
- Line 69: Documents brand guideline changes
- Lines 96-97: Contributing guidelines reference the porting conventions

**Action:** Leave all PORTING.md references unchanged. They are essential documentation.

---

### 2. External Repository Links (Decision Required)

The README.md contains links to external GitHub repositories that have "claude" in their names. These are third-party
skills not controlled by this repository.

#### Links identified:

| Line | Repository                                      | Description                  |
|------|-------------------------------------------------|------------------------------|
| 117  | `smerchek/claude-epub-skill`                    | Markdown to EPUB converter   |
| 124  | `chrisvoncsefalvay/claude-d3js-skill`           | D3.js visualization skill    |
| 125  | `jthack/ffuf_claude_skill`                      | FFUF web fuzzing integration |
| 131  | `omkamal/pypict-claude-skill`                   | PICT test case design        |
| 157  | `emaynard/claude-family-history-research-skill` | Family history research      |

#### Additional external link:

| Line | URL                      | Description              |
|------|--------------------------|--------------------------|
| 233  | Notion Skills for Claude | External Notion resource |

**Options for handling:**

1. **Keep links as-is**
    - Pros: Skills may still work with Junie; maintains comprehensive resource list
    - Cons: "Claude" in URLs may confuse users; skills may have Claude-specific code

2. **Fork and port external skills**
    - Pros: Full control; consistent branding
    - Cons: Significant effort; maintenance burden; may violate original licenses

3. **Remove Claude-specific external links**
    - Pros: Clean, Junie-focused repository
    - Cons: Loses potentially useful resources

4. **Add disclaimer/note**
    - Pros: Transparency; keeps resources available
    - Cons: May still cause confusion

**Decision: ADD DISCLAIMER** - A note will be added in README.md explaining that some external skills were
originally designed for Claude but may work with Junie. This maintains the resource value while setting appropriate
expectations.

**Suggested disclaimer text:**

```markdown
> **Note:** Some external skills linked below were originally created for Claude.
> They may require adaptation to work optimally with Junie. Check each skill's
> repository for compatibility information.
```

---

### 3. Anthropic Branding in brand-guidelines/SKILL.md

The `brand-guidelines/SKILL.md` skill applies "Anthropic's official brand colors and typography." This requires complete
replacement with JetBrains branding:

**Current Anthropic brand elements to replace:**

- Color palette (specific hex values)
- Typography (font families)
- Design guidelines
- Brand voice/tone references

**Required JetBrains brand elements:**

- JetBrains official colors (refer to https://www.jetbrains.com/company/brand/)
- JetBrains typography guidelines
- JetBrains design system references

**Decision: REWRITE** - This skill needs complete content replacement, not just text substitution. The actual brand guidelines,
colors, and fonts must be researched and updated to reflect JetBrains' official brand identity.

---

### 4. CONTRIBUTING.md Header Inconsistency

**Decision: UPDATE** - The `CONTRIBUTING.md` file still has the header "Contributing to Awesome LLM Skills" (line 1) which will be
updated to "Contributing to Awesome Junie Skills" for consistency with the rest of the repository.

---

## Summary of Decisions (Final)

| Item                    | Decision                              | Status    |
|-------------------------|---------------------------------------|-----------|
| algorithmic-art skill   | **Created** Junie-native skill        | ✓ Done    |
| artifacts-builder skill | **Repurposed** as webapp-builder      | ✓ Done    |
| External Claude links   | **Add disclaimer** noting origins     | Pending   |
| brand-guidelines skill  | **Rewritten** with JetBrains brand    | ✓ Done    |
| PORTING.md              | No changes (intentional references)   | ✓ Done    |
| CONTRIBUTING.md header  | **Updated** title accordingly         | ✓ Done    |

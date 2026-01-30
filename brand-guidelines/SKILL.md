---
name: brand-guidelines
description: Applies JetBrains official brand colors and typography to any sort of artifact that may benefit from having JetBrains' look-and-feel. Use it when brand colors or style guidelines, visual formatting, or company design standards apply.
license: Complete terms in LICENSE.txt
---

# JetBrains Brand Styling

## Overview

To access JetBrains' official brand identity and style resources, use this skill.

**Keywords**: branding, corporate identity, visual identity, post-processing, styling, brand colors, typography, JetBrains brand, visual formatting, visual design

**Reference**: [JetBrains Brand Guidelines](https://www.jetbrains.com/company/brand/)

## Brand Guidelines

### Colors

**Primary Colors:**

- JetBrains Black: `#000000` - Primary text and dark backgrounds
- JetBrains White: `#FFFFFF` - Light backgrounds and text on dark
- JetBrains Gray: `#27282C` - Dark UI elements
- Light Gray: `#F4F4F4` - Subtle backgrounds

**Brand Gradient Colors:**

- Purple: `#7B5CFA` - Primary brand accent
- Pink: `#FC318E` - Secondary brand accent
- Orange: `#FE8A00` - Tertiary brand accent
- Blue: `#07C3F2` - Quaternary brand accent

**Product Colors (for context):**

- IntelliJ IDEA: `#FE315D` to `#F97A12` gradient
- PyCharm: `#21D789` to `#FCF84A` gradient
- WebStorm: `#07C3F2` to `#087CFA` gradient

### Typography

- **Headings**: JetBrains Sans (with Inter or Arial fallback)
- **Body Text**: JetBrains Sans (with Inter or Arial fallback)
- **Code/Monospace**: JetBrains Mono (with Consolas fallback)
- **Note**: JetBrains fonts are free and open source - download from https://www.jetbrains.com/lp/mono/

## Features

### Smart Font Application

- Applies JetBrains Sans to headings (24pt and larger)
- Applies JetBrains Sans to body text
- Applies JetBrains Mono to code blocks and technical content
- Automatically falls back to Inter/Arial if custom fonts unavailable
- Preserves readability across all systems

### Text Styling

- Headings (24pt+): JetBrains Sans Bold
- Body text: JetBrains Sans Regular
- Code snippets: JetBrains Mono
- Smart color selection based on background
- Preserves text hierarchy and formatting

### Shape and Accent Colors

- Non-text shapes use brand gradient colors
- Cycles through purple, pink, orange, and blue accents
- Maintains visual interest while staying on-brand
- Supports gradient fills for modern look

## Technical Details

### Font Management

- Uses system-installed JetBrains Sans and JetBrains Mono when available
- Provides automatic fallback to Inter (headings/body) and Consolas (code)
- No font installation required - works with existing system fonts
- For best results, pre-install JetBrains fonts from https://www.jetbrains.com/lp/mono/

### Color Application

- Uses RGB color values for precise brand matching
- Applied via python-pptx's RGBColor class
- Maintains color fidelity across different systems
- Supports gradient backgrounds for hero sections

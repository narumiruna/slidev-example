# Slidev Roman History Deck

A Slidev presentation project for a Traditional Chinese deck about Ancient Rome.

## Generation Workflow

This deck was generated with Codex CLI using the Slidev skill.

Slidev skill reference: [Work with AI](https://sli.dev/guide/work-with-ai)

Install the Slidev skill with:

```bash
npx skills add slidevjs/slidev
```

## Prerequisites

- Node.js 18+
- pnpm

## Quick Start

```bash
pnpm install
pnpm dev
```

Then open <http://localhost:3030>.

Main deck file:
- `slides.md`

## Common Commands

```bash
pnpm dev      # Run local preview
pnpm build    # Build static site into dist/
pnpm export   # Export slides (default: PDF)
```

## Export to PDF or PPTX

Slide export depends on Playwright Chromium.

```bash
pnpm add -D playwright-chromium
pnpm exec playwright install chromium
```

Examples:

```bash
pnpm export --format pdf --output Roman-History.pdf
pnpm export --format pptx --output Roman-History.pptx
```

## Notes

- If ports are occupied, stop other Slidev dev servers before running `pnpm dev`.
- For Mermaid diagrams, prefer English labels when exporting to PPTX to avoid missing CJK glyphs in rendered diagrams.

## Reference

- Slidev docs: <https://sli.dev/>

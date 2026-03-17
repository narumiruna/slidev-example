# Repository Guidelines

## Project Structure & Module Organization
This repository is a Slidev deck project. Keep presentation content and reusable code separated:
- `slides.md`: main entry deck (frontmatter, slide flow, speaker notes).
- `pages/`: imported slide segments (e.g., `pages/imported-slides.md`).
- `components/`: Vue slide components used inside Markdown slides.
- `snippets/`: external code snippets embedded in slides.
- `netlify.toml` and `vercel.json`: deployment settings.
- `package.json`: build/dev/export scripts and dependency source of truth.

Use small, single-purpose files. Put shared UI logic in `components/` rather than repeating complex inline Vue blocks in `slides.md`.

## Build, Test, and Development Commands
Install dependencies and run Slidev locally:
- `pnpm install`: install dependencies from `pnpm-lock.yaml`.
- `pnpm dev`: start local deck preview at `http://localhost:3030`.
- `pnpm build`: build static output for hosting.
- `pnpm export`: export slides (PDF/PPTX) via Slidev export pipeline.

Run commands from repository root. Prefer `pnpm` to keep lockfile consistency.

## Coding Style & Naming Conventions
Use concise Markdown and predictable naming:
- Indentation: 2 spaces for YAML/frontmatter and nested lists.
- Language: documentation and slide text should be clear and audience-appropriate.
- Vue components: PascalCase filenames (e.g., `TopicTimeline.vue`).
- Snippets: descriptive lowercase or kebab-case names by topic (e.g., `snippets/roman-law.ts`).

Keep slides readable: short headings, focused bullets, and one core idea per slide.

## Testing Guidelines
There is no dedicated automated test suite yet. Validate changes with:
- `pnpm dev` for visual and interaction checks.
- `pnpm build` to catch build-time errors.
- `pnpm export` when changing print/export-sensitive layouts.

For component additions, verify rendering in both normal view and presenter flow.

## Commit & Pull Request Guidelines
Current history is minimal (`Initial commit`), so adopt Conventional Commits going forward:
- Examples: `feat: add roman timeline slide`, `fix: correct export layout overflow`.

PRs should include:
- Clear scope summary and why the change is needed.
- Linked issue (if available).
- Screenshots or exported sample pages for visual changes.
- Notes on any follow-up work.

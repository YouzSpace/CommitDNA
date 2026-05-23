---
name: readme-gen
description: >
  Generate or update README.md with a professional, minimalist,
  engineering-grade style.
  Inspired by Vercel, Turbo, TailwindCSS, Next.js, and other
  top-tier open-source projects.
  Triggered when the user mentions: update readme, 更新 readme,
  generate readme, /readme, or before pushing to remote.
---

# readme-gen

You are a **senior open-source maintainer** and **technical writer**.

Your job is to generate or update `README.md` so that it:
- looks like a Vercel / TailwindCSS / Turbo repo
- is minimalist and engineering-grade
- has zero fluff
- is readable in 30 seconds

---

## README Structure (template)

```markdown
# <project-name>

<p align="center">
  <strong><one-line description></strong>
</p>

<p align="center">
  <a href="https://img.shields.io/badge/...">...</a>
</p>

---

## Why <project-name>?

<2-3 sentences explaining the core value prop>

## Features

- <feature 1>
- <feature 2>
- <feature 3>

## Quick Start

```bash
# install
<install command>

# run
<run command>
```

## Project Structure

```
<concise tree, max 10 entries>
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first.

## License

<license, default: MIT>
```

---

## Rules

### Tone & Style

- Engineering-grade, not marketing-grade
- No: "Welcome to our amazing project ⭐"
- No: emojis in headings
- No: "Feel free to reach out!"
- Yes: dry, precise, factual

### Badges (optional, keep minimal)

Only include if they add signal:
- CI status
- npm / pip version
- license
- coverage (if ≥ 80%)

### Code blocks

- Always specify language (`bash`, `ts`, `python`)
- Always include comments for non-obvious commands

### One-line description

Must answer:
> "What does this do, and why would I use it instead of X?"

Examples:
- `cognee`: "Simplify AI memory management with a minimal API."
- `turbo`: "Incremental bundler and build system optimized for monorepos."
- `tailwindcss`: "A utility-first CSS framework for rapid UI development."

---

## Behavior

### When triggered

1. Scan the project:
   ```bash
   ls -la
   cat package.json   # or pyproject.toml, Cargo.toml, etc.
   cat tsconfig.json  # or equivalent config
   find . -name "*.md" | head -5
   ```

2. Identify:
   - Project name
   - One-line description
   - Tech stack
   - Key features
   - Quick start commands

3. Generate `README.md` following the template above.

4. If `README.md` already exists:
   - Read it first
   - Preserve valid content
   - Restructure to match the template
   - Remove fluff

5. Present the new README to the user and ask for confirmation before writing.

### When the user is about to push

If the user says "push", "推送", "提交远程", ask:

> 要调用 `readme-gen` Skill 更新 README 吗？

Only proceed after the user confirms.

---

## Anti-patterns (never do this)

```markdown
<!-- ❌ Don't -->

# Welcome to My Project 🚀

Thanks for checking this out!

## Installation

Clone the repo and you're good to go!

## Contributing

Open to any suggestions!
```

```markdown
<!-- ✅ Do -->

# project-name

Minimal, fast, zero-dependency X.

## Quick Start

```bash
npm install
npm run dev
```
```

---

## Notes

- Default language: Chinese, unless the repo is English-first (check existing files).
- Keep README under 80 lines if possible.
- If the project is private / internal, skip badges and license section.

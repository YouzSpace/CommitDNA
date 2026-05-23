# CommitDNA

<p align="center">
  <strong>AI Skills output specification system for Cursor, Claude Code, and OpenAI Agent</strong>
</p>

<p align="center">
  <a href="https://github.com/yourusername/CommitDNA/actions"><img src="https://img.shields.io/github/actions/workflow/status/yourusername/CommitDNA/ci.yml" alt="CI"></a>
  <a href="https://github.com/yourusername/CommitDNA/blob/main/LICENSE"><img src="https://img.shields.io/github/license/yourusername/CommitDNA" alt="License"></a>
</p>

---

## Why CommitDNA?

Standardize AI-generated output across multiple platforms (Cursor, Claude Code, OpenAI Agent).  
Provide industrial-grade, production-ready AI Skills Library with precise specification and documentation.

## Features

- Conventional Commits generator (`commit-gen`)
- Minimalist engineering-grade README generator (`readme-gen`)
- Multi-platform AI Skills specification
- Modular, reusable, and maintainable

## Quick Start

```bash
# clone
git clone https://github.com/yourusername/CommitDNA.git
cd CommitDNA

# use skills (WorkBuddy required)
workbuddy /commit
workbuddy /readme
```

## Project Structure

```
CommitDNA/
├── .workbuddy/
│   └── skills/
│       ├── commit-gen/
│       │   └── SKILL.md
│       └── readme-gen/
│           └── SKILL.md
├── README.md
└── LICENSE
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first.

## License

MIT

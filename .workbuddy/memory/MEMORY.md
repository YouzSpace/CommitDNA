# MEMORY.md - Long-term Memory

## User Preferences

- **Language**: 简体中文（简洁直接）
- **Interaction style**: 指令简短（「开始」、「明白不」），喜欢先确认理解再行动
- **Safety**: 强安全意识，使用占位符，不上传私有文件
- **Workflow**: 偏好增量修改、表格整理、API 对接文档、清理测试数据
- **Server**: 关心 VPS 状态，故障后要求确认稳定性，代码修改后需提醒重启后端

## Project Context

### CommitDNA Project
- **Goal**: AI Skills 输出规范系统，面向 Cursor / Claude Code / OpenAI Agent 多平台
- **Target**: 工业级、生产就绪的 AI Skills Library
- **Current**: 初始化阶段，尚未提交 Git 仓库

### Active Projects
- 柚子云 Store（PHP 8.5.6 NTS，架构设计）
- 食语 App（Spring Boot 3.5 + Vue/Vant 4）
- 微信活码管理系统（纯 PHP，iOS 轻质感）
- 电影感太空旅行着陆页（React + Tailwind + Framer Motion）
- DesignDNA UI 逆向工程 Skill（agentskills.io 规范）

## Workbuddy Skills

### Custom Skills Created
- `commit-gen`: 生成 Conventional Commits 风格 commit message
- `readme-gen`: 生成/更新极简工程化 README
- `design-dna`: UI 设计系统逆向工程
- `ssh-server-manager`: SSH 远程服务器管理
- `ai-dev-pipeline`: AI 项目全流程开发

## Behavior Rules

### Push Reminder (2026-05-24)
- When user says: "推送", "push", "提交远程", "push to remote"
- MUST ask:
  1. 「要调用 `commit-gen` Skill 生成规范 commit 吗？」
  2. 「要同步更新 README 保持风格统一吗？」
- Do NOT push directly without confirmation

### Commit Style
- Follow Conventional Commits: `type(scope): message`
- Allowed types: feat, fix, refactor, docs, style, perf, test, build, ci, chore, spec, workflow, agent, prompt, memory
- Allowed scopes: auth, core, api, ui, agent, workflow, spec, memory, prompt, analytics
- Forbidden words: update, fix bug, final, misc, temporary, test
- Style reference: Vercel, Next.js, TailwindCSS, OpenAI, Cognee

### README Style
- Minimalist, engineering-grade
- No emojis in headings
- No marketing fluff
- Badges only if they add signal
- Keep under 80 lines if possible

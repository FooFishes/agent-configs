# agent-configs

FooFish 的 Agent 配置 Repo

覆盖的 Agent：**Claude Code**、**Codex**、**Pi**

## 目录结构

```
agent-configs/
├── agents/            # 某个 Agent 专属的主配置
│   ├── claude-code/   # ← ~/.claude
│   ├── codex/         # ← ~/.codex
│   └── pi/            # ← ~/.pi
├── prompts/           # 可复用的提示词（跨 Agent 通用）
├── skills/            # 技能（每个技能一个目录，内含 SKILL.md）
├── MCPs/              # MCP 服务器配置片段
├── memories/          # 想长期保留的记忆 / 个人偏好
├── templates/         # 新项目用的 CLAUDE.md / AGENTS.md 等模板
└── workflows/         # 多步骤工作流脚本与说明
```

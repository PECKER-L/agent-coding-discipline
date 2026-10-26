# Agent Coding Discipline

> **12 practical engineering rules for AI coding agents.** One Markdown file. No scripts or dependencies.

**中文简介：** 面向 AI 编程助手的 12 条通用工程规范，强调编码前思考、最小化改动、目标验证、充分阅读、有效测试、遵循项目约定以及主动暴露失败。它不绑定 Claude 或任何特定模型。

## Why this skill?

AI coding agents can over-engineer, change unrelated code, skip important checks, or claim success without verification. **Agent Coding Discipline** provides a concise, reusable rule set to encourage careful, auditable work.

## The 12 rules / 十二条规则

1. **Think Before Coding** — 先思考再编码
2. **Simplicity First** — 简单优先
3. **Surgical Changes** — 精准修改
4. **Goal-Driven Execution** — 以目标和验证为导向
5. **Use the Model Only for Judgment Calls** — 确定性工作优先交给代码
6. **Token Budgets Are Not Advisory** — 重视 Token 预算
7. **Surface Conflicts, Don't Average Them** — 明确暴露冲突
8. **Read Before You Write** — 修改前先阅读
9. **Tests Verify Intent, Not Just Behavior** — 测试应验证设计意图
10. **Checkpoint After Every Significant Step** — 关键步骤设检查点
11. **Match the Codebase's Conventions** — 遵循现有代码规范
12. **Fail Loud** — 不掩盖失败和不确定性

Read the full instructions in [`SKILL.md`](./SKILL.md).

## Installation / 安装

For AI tools supported by [Skills CLI](https://skills.sh/), run:

```bash
npx skills add YOUR_GITHUB_USERNAME/agent-coding-discipline
```

Replace `YOUR_GITHUB_USERNAME` with your GitHub account or organization name after you create a public repository. Install behavior and compatible targets depend on the current version of Skills CLI.

### Manual installation / 手动使用

This repository follows the [Agent Skills specification](https://agentskills.io/specification). For supported tools, install or place this skill into the tool's skills directory according to that tool's documentation.

For tools **without** native Skill support, open [`SKILL.md`](./SKILL.md), copy the 12-rule section into the tool's project instructions, or reference it in the tool's custom-instruction system. For example, a project may use `AGENTS.md` or `CLAUDE.md` when supported.

**Compatibility note:** The instructions are model-agnostic, but a Markdown Skill is not automatically discoverable by every AI product. Manual import may be required.

## Repository structure / 项目结构

```text
agent-coding-discipline/
├── SKILL.md    # Agent Skills metadata and the 12 rules
├── README.md   # Project introduction and setup
└── LICENSE     # MIT open-source license
```

## Design notes / 说明

- The underlying 12 rules are **preserved from the original `claude-md-rules`**. The title and integration instructions have been generalized for cross-tool use.
- Rule 6 contains example limits of **4,000 tokens/task** and **30,000 tokens/session**. These are recommended template budgets, not a technical enforcement mechanism.
- Existing project rules and higher-priority instructions take precedence where applicable; resolve conflicts explicitly.
- This is an instructional Skill, not executable software.

## License / 开源许可

Released under the **MIT License** — see [`LICENSE`](./LICENSE). You may use, modify, and redistribute this work, including commercially, subject to the license terms (notably preserving the required notice).

**Publishing note / 发布前提示：** The license currently lists **Agent Coding Discipline Contributors** as the copyright holder. If you want to publish under your own name or GitHub handle, update that line in `LICENSE` before publishing.

---
name: reporting-discipline
description: Use when reporting results, summarizing long logs, documents, tool outputs, agent work, code review findings, debugging evidence, or any task where raw text could bloat the conversation context.
---

# Reporting Discipline

## 全局协作约定

- 编码、审查、重构或修 bug 时，可显式触发 `karpathy-guidelines`：先说明假设和取舍，保持改动外科式，定义可验证成功标准。
- 汇报长日志、长文档、工具输出、agent 工作或调试证据时，可显式触发 `reporting-discipline`：先给结论、关键证据、风险和下一步，不默认粘贴大段原文。
- 常用触发语：`use karpathy-guidelines and reporting-discipline`，或“用 karpathy 打底，并按 reporting discipline 汇报”。


## Core Principle

Report the useful signal, not the raw mass. Preserve evidence without dumping it into chat.

## Default Report Shape

Use this order unless the user asks for another format:

1. Conclusion or current status.
2. Key evidence, with short excerpts only when they matter.
3. Blockers, uncertainty, or risks.
4. Next action or verified completion.
5. Links or file paths for bulky raw material.

## Context Budget Rules

- Do not paste huge logs, raw documents, command output, diffs, or agent transcripts by default.
- Summarize first; include only the smallest excerpt needed to justify the claim.
- If raw material is useful, save it to an appropriate file and link or cite that file instead of flooding chat.
- When the user explicitly asks for full raw output and it is large, provide a concise warning and prefer a file artifact.
- Keep progress updates to one or two sentences unless a decision or blocker needs more context.
- In final answers, report what changed, what was verified, and what remains uncertain.

## Evidence Standards

- Do not claim success from memory or vibes. Name the verification that supports it.
- If verification was partial, say exactly what was and was not checked.
- For multi-agent or tool-heavy work, summarize the independently verified result rather than relaying every intermediate message.

## Red Flags

Stop and compress before replying if you are about to include:

- More than one screen of raw output.
- Repeated log lines or stack frames.
- Full files when a path plus summary is enough.
- Long reasoning history instead of the outcome and evidence.

# PRD Review Panel / PRD评审会模拟

[English](#english) | [中文](#中文)

---

## English

A multi-agent PRD review meeting simulator using 4 roles with adversarial feedback. Simulates a real product review meeting before formal评审会.

### Installation

```bash
cd ~/.claude/skills && git clone https://github.com/rance811-maker/prd-review-panel.git
```

### Usage

1. Open Claude Code
2. Paste your PRD content
3. Trigger: mention "prd-review-panel" or "PRD review meeting"

### Roles

| Role | Focus | Style |
|------|-------|-------|
| 🤖 Tech Lead | Implementation complexity, stability, risks | Strict, realistic, can veto |
| 🤖 Design Lead | UX, interaction consistency, understanding cost | Detail-oriented |
| 🤖 Business Lead | ROI, business value, priorities | Questions "is this worth it?" |
| 🤖 Product Lead | Summary, decision, consensus | Neutral, decisive |

### Agent PRD Review Dimensions (AI Agent Specific)

This skill is optimized for AI Agent PRD reviews, with additional focus on:

| Dimension | Key Questions |
|-----------|---------------|
| Background & Goals | Why Agent vs traditional solution? |
| Agent Identity & Boundaries | In/Out of Scope? Decision authority? |
| Input/Output Contract | Schema with confidence & evidence? |
| Behavior Rules | Anti-patterns? Hallucination prevention? |
| Evaluation Plan | Offline eval set? Failure mode monitoring? |
| Human-AI Collaboration | Human fallback entry point? |
| Launch Strategy | Gradual rollout? Rollback conditions? |
| Evolution Roadmap | V1 boundaries? Data flywheel? |
| Risks & Mitigation | Agent-specific risks (hallucination, overreach)? |

### Review Flow

```
Round 1 → Quick understanding (all roles)
Round 2 → Focused challenges (per role)
Round 3 → Adversarial debate (real pushback)
Round 4 → Final verdict (Product Lead)
```

### Output Format

```
🎯 评审结论：[❌ Not Passed / ⚠️ Conditional / ✅ Approved]
⚠️ 关键问题：
1. ...
2. ...
3. ...

💡 次要优化建议：
• ...

📅 建议进入开发排期：[Yes/No]
```

---

## 中文

使用 4 个并行 AI Agent 模拟真实 PRD 评审会。每个角色"站在自己立场说话"，有冲突、有质疑、有交锋，帮助在正式评审前发现关键问题。

### 安装方式

```bash
cd ~/.claude/skills && git clone https://github.com/rance811-maker/prd-review-panel.git
```

### 使用方式

1. 打开 Claude Code
2. 粘贴 PRD 内容
3. 触发指令：提到 "prd-review-panel" 或 "PRD评审会"

### 参与角色

| 角色 | 关注点 | 风格 |
|------|--------|------|
| 🤖 技术负责人 | 实现复杂度、稳定性、风险 | 严格、现实，有一票否决权 |
| 🤖 设计负责人 | 用户体验、交互一致性、理解成本 | 关注细节违和感 |
| 🤖 业务负责人 | ROI、业务价值、优先级 | 质疑"做这个值不值" |
| 🤖 产品负责人 | 总结收敛、推动决策 | 理性、不替人辩护 |

### Agent PRD 评审维度（AI Agent 特有）

本 skill 针对 AI Agent 类 PRD 优化，新增以下评审重点：

| 维度 | 关键问题 |
|------|----------|
| 背景与目标 | 为什么用 Agent 而不是传统方案？ |
| Agent 身份与边界 | In/Out of Scope？决策权限？ |
| 输入输出契约 | schema 含置信度和 evidence？ |
| 行为规约 | 反例清单？幻觉防范机制？ |
| 评估方案 | 离线评估集？失败模式监控？ |
| 人机协作 | 人工兜底入口？反馈回流？ |
| 上线策略 | 灰度节奏？回滚条件？ |
| 演进路线 | V1 边界？数据飞轮？ |
| 风险与应对 | Agent 特有风险（幻觉、越权）？ |

### 评审流程

```
第1轮 → 快速理解（所有角色）
第2轮 → 集中质疑（各角色）
第3轮 → 冲突交锋（真实反驳）
第4轮 → 最终结论（产品负责人）
```

### 输出格式

```
🎯 评审结论：[❌ 不通过 / ⚠️ 有条件通过 / ✅ 可以推进]
⚠️ 关键问题：
1. ...
2. ...
3. ...

💡 次要优化建议：
• ...

📅 建议进入开发排期：[是/否]
```

---

## Example 输出示例

```markdown
═══════════════════════════════════════
🎭 PRD 评审会
═══════════════════════════════════════

【第1轮】快速理解
🤖 技术负责人：...
🤖 设计负责人：...
🤖 业务负责人：...
🤖 产品负责人：...

【第2轮】集中质疑
🤖 技术负责人：是否支持推进：[有条件支持]
🤖 设计负责人：...
🤖 业务负责人：ROI判断：[待证明]

【第3轮】冲突交锋
[技术 vs 业务] [设计 vs 技术] [产品 vs 各方]

【第4轮】最终结论
🎯 评审结论：⚠️ 有条件通过
⚠️ 关键问题：
1. 知识库建设方案缺失
2. 518时间线与功能范围不匹配
3. 售前售后混合场景无解

📅 建议进入开发排期：否
```

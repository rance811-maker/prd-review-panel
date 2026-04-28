# PRD评审会模拟（多角色对抗版）

[English](#english) | [中文](#中文)

---

## English

A multi-agent PRD review meeting simulator using 4 roles with adversarial feedback.

### Installation

```bash
cd ~/.claude/skills && git clone https://github.com/rance811-maker/prd-review-panel.git
```

### Usage

1. Open Claude Code
2. Paste your PRD content
3. Trigger: mention "prd-review-panel" or "PRD评审会"

### Roles

| Role | Focus | Style |
|------|-------|-------|
| 🤖 Tech Lead | Implementation complexity, risks | Strict, realistic |
| 🤖 Design Lead | UX, interaction, consistency | Detail-oriented |
| 🤖 Business Lead | ROI, value, priorities | Questions value |
| 🤖 Product Lead | Summary, decision, consensus | Neutral, decisive |

### Review Flow

1. **Round 1**: Quick understanding (all roles)
2. **Round 2**: Focused challenges (per role)
3. **Round 3**: Adversarial debate (real pushback)
4. **Round 4**: Final verdict (Product Lead)

### Output

```
🎯 评审结论：[❌/⚠️/✅]
⚠️ 关键问题：
1. ...
2. ...
3. ...

💡 次要优化建议：
• ...

📅 建议进入开发排期：[是/否]
```

---

## 中文

基于 4 个并行 Agent 模拟真实的 PRD 评审会。每个角色"站在自己立场说话"，有冲突、有质疑、有交锋。

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
| 🤖 技术负责人 | 实现复杂度、稳定性、风险 | 严格、现实 |
| 🤖 设计负责人 | 用户体验、交互、理解成本 | 关注细节 |
| 🤖 业务负责人 | 业务价值、ROI、优先级 | 质疑值不值 |
| 🤖 产品负责人 | 总结收敛、推动决策 | 理性、不辩护 |

### 评审流程

1. **第1轮**：快速理解（所有角色）
2. **第2轮**：集中质疑（各角色）
3. **第3轮**：冲突交锋（真实反驳）
4. **第4轮**：最终结论（产品负责人）

### 输出格式

```
🎯 评审结论：[❌/⚠️/✅]
⚠️ 关键问题：
1. ...
2. ...
3. ...

💡 次要优化建议：
• ...

📅 建议进入开发排期：[是/否]
```

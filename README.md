<p align="center">
  <h1>🧠 Sharp Think</h1>
  <p><strong>结构化思考优化框架 — 让 AI 又快又好地思考</strong></p>
</p>

<p align="center">
  <a href="https://github.com/qingjian0/sharp-think"><img src="https://img.shields.io/badge/GitHub-sharp--think-black?logo=github" alt="GitHub"></a>
  <img src="https://img.shields.io/badge/Trae-Skill-2496ED?logo=visualstudiocode" alt="Trae Skill">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="MIT License">
  <img src="https://img.shields.io/badge/复杂度-L1/L2/L3-FF9900" alt="三级复杂度">
</p>

<p align="center">
  <b>English</b> | <a href="#中文文档">中文</a>
</p>

---

> [!NOTE]
> **Sharp Think** 是一个为 [Trae](https://trae.ai/) 设计的 Skill，通过注入结构化思考框架到 AI 的推理过程中，让简单问题秒答、复杂问题深度分析、永远不跑偏。

## ✨ Features

| 痛点 | Sharp Think 的解法 |
|------|-------------------|
| 🎯 **方向跑偏** | 强制「一句话复述」+ 歧义检测，理解错就追问 |
| 🐢 **过度思考** | L1/L2/L3 复杂度分级，简单问题直接回答不展开 |
| 🏊 **思考不深** | L3 强制 7 步推理 + 认知偏差自检 + 多方案对比 |
| 📝 **缺乏结构** | 统一三阶段流程 + 标准化输出格式 |

## 📋 Table of Contents

- [Features](#-features)
- [How It Works](#-how-it-works)
- [Complexity Levels](#-complexity-levels)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Reference Cards](#-reference-cards)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)

## 🔄 How It Works

```
User Query
   │
   ▼
┌──────────────────────┐
│  Phase 1: Quick Assess │  ← Complete in 10 seconds
│  · Restate intent      │
│  · Classify complexity │
│  · Detect ambiguity    │
└──────────┬───────────┘
           │
      ┌────┴────┬──────────┐
      ▼         ▼          ▼
     L1        L2         L3
   Direct    Standard    Deep
   Answer    Analysis    Analysis
      │     4 steps    7 steps
      │         │      + cards
      │         │      + bias check
      ▼         ▼          ▼
┌──────────────────────┐
│  Phase 3: Quality Gate │
│  · Right direction  ✓  │
│  · Actionable       ✓  │
│  · Edge cases       ✓  │
│  · Clear structure  ✓  │
└──────────────────────┘
```

## 📊 Complexity Levels

| Level | When to Use | Thinking Budget | Example |
|-------|------------|-----------------|---------|
| **L1 Direct** | Factual queries, single-step ops | Answer immediately | "Translate this", "Current time" |
| **L2 Standard** | 2-5 step reasoning, clear constraints | 4-step framework | "Write a weekly report", "Analyze trends" |
| **L3 Deep** | Multi-option comparison, architecture design | Full chain + reference cards | "Design growth plan", "Evaluate tech stack" |

## 📦 Installation

### Option 1: Manual Copy (Recommended)

Copy the entire project into your Trae project's `.trae/skills/` directory:

```bash
# Navigate to your Trae project root
cd /path/to/your/project

# Create skills directory if not exists
mkdir -p .trae/skills

# Copy sharp-think into it
cp -r /path/to/sharp-think .trae/skills/sharp-think
```

The final structure should look like:

```
your-project/
└── .trae/
    └── skills/
        └── sharp-think/
            ├── SKILL.md
            └── references/
                ├── cognitive-biases.md
                ├── complexity-scaling.md
                ├── decision-frameworks.md
                └── quality-checklist.md
```

### Option 2: Git Clone

```bash
# Clone to a temp directory
git clone https://github.com/qingjian0/sharp-think.git /tmp/sharp-think

# Copy to your Trae project
mkdir -p /path/to/your/project/.trae/skills
cp -r /tmp/sharp-think /path/to/your/project/.trae/skills/sharp-think

# Clean up
rm -rf /tmp/sharp-think
```

### Option 3: Direct Download

Download the [latest release](https://github.com/qingjian0/sharp-think/releases) and extract to `.trae/skills/sharp-think/`.

> [!TIP]
> After installation, the Skill will **auto-trigger** when your queries involve keywords like: 分析、方案、规划、决策、设计、评估、优化、最佳实践, etc.

## 🚀 Usage

### Trigger Keywords

The Skill auto-activates when your query contains these keywords:

| 中文 | English |
|------|---------|
| 帮我分析 / 思考 | analyze / think through |
| 写方案 / 设计 | design / plan |
| 做决策 / 对比 | decide / compare |
| 最佳实践 / 优化建议 | best practices / optimize |
| 架构设计 / 技术选型 | architecture / tech stack |
| 问题诊断 / 根因分析 | diagnose / root cause |

### Quick Examples

**L1 — Direct Answer:**

> **You**: 把这段话翻译成英文
>
> **AI**: *(Translates directly, no reasoning overhead)*

**L2 — Standard Analysis:**

> **You**: 帮我写一份项目周报
>
> **AI**: Follows 4-step framework → Goal → Constraints → Solution → Verification

**L3 — Deep Analysis:**

> **You**: 我们应该用 React 还是 Vue 重构前端？
>
> **AI**: Follows 7-step framework → Problem Definition → Root Cause → Option Exploration (2+) → Recommendation → Implementation Path → Risk Assessment → Success Criteria
>
> Automatically references cognitive bias checklist and decision matrix.

### Special Commands

| You Say | AI Response |
|---------|-------------|
| "快一点" / "简单回答" | Downgrade one complexity level (L3→L2, L2→L1) |
| "详细分析" / "深入思考" | Upgrade one complexity level (L1→L2, L2→L3) |
| "为什么？" | Trace back to reasoning chain, show derivation |
| Multiple sub-questions | Split → Classify each → Process by dependency → Synthesize |

## 📁 Project Structure

```
sharp-think/
├── SKILL.md                          # Core thinking framework (Skill entry point)
├── README.md                         # This file
├── LICENSE                           # MIT License
└── references/                       # Reference card library (loaded on demand)
    ├── cognitive-biases.md           # 12 cognitive bias detection checklist
    ├── decision-frameworks.md        # 7 decision frameworks (SWOT, 5-Why, etc.)
    ├── quality-checklist.md          # Quality checklists for 5 output types
    └── complexity-scaling.md         # Detailed complexity classification guide
```

## 🗂️ Reference Cards

| Card | Content | When to Use |
|------|---------|-------------|
| 🧩 [Cognitive Biases](references/cognitive-biases.md) | 12 common biases + self-check methods | L3 + decision/judgment tasks |
| 📊 [Decision Frameworks](references/decision-frameworks.md) | SWOT, Decision Matrix, 5-Why, First Principles, etc. | L3 + multi-option comparison |
| ✅ [Quality Checklist](references/quality-checklist.md) | Check templates for docs/analysis/plans/creative/code | All L2+ tasks before output |
| 📏 [Complexity Scaling](references/complexity-scaling.md) | Detailed L1/L2/L3 criteria, edge cases, dynamic adjustment | First use or uncertain classification |

## 🔧 Troubleshooting

| Problem | Solution |
|---------|----------|
| Skill not auto-triggering | Check that `SKILL.md` is inside `.trae/skills/sharp-think/` and the front matter is intact |
| AI still overthinking simple questions | Verify the complexity classification table is present in SKILL.md |
| Reference cards not being used | Ensure `references/` folder is in the same directory as `SKILL.md` |
| Output format inconsistent | Check that output format section in SKILL.md is not modified |

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Report bugs** — Open an [Issue](https://github.com/qingjian0/sharp-think/issues) describing the problem
2. **Suggest improvements** — Share your ideas for new reference cards or framework enhancements
3. **Submit PRs** — Fork, modify, and create a Pull Request

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

<a id="中文文档"></a>

## 🇨🇳 中文文档

### 这是什么？

Sharp Think 是一个为 [Trae](https://trae.ai/) 设计的 Skill，通过注入**结构化思考框架**到 AI 的推理过程中，解决四个常见痛点：

| 痛点 | 解法 |
|------|------|
| 🎯 方向跑偏 | 强制「一句话复述」+ 歧义检测，理解错就追问 |
| 🐢 过度思考 | L1/L2/L3 复杂度分级，简单问题直接回答不展开 |
| 🏊 思考不深 | L3 强制 7 步推理 + 认知偏差自检 + 多方案对比 |
| 📝 缺乏结构 | 统一三阶段流程 + 标准化输出格式 |

### 设计理念

- **先评估后思考** — 永远先判断问题复杂度，再决定思考深度
- **先对齐后执行** — 确保理解正确后再展开推理
- **结构化输出** — 按统一模板组织思考过程和最终输出
- **质量自检** — 输出前必须通过校验检查点

### 安装方式

将项目复制到你的 Trae 项目的 `.trae/skills/` 目录下：

```bash
# 进入你的 Trae 项目根目录
cd /path/to/your/project

# 创建 skills 目录（如果不存在）
mkdir -p .trae/skills

# 复制 sharp-think
cp -r /path/to/sharp-think .trae/skills/sharp-think
```

安装后 Skill 会在你提问涉及**分析、方案、规划、决策**等关键词时自动触发。

### 使用示例

| 你说的话 | AI 的反应 |
|---------|----------|
| "快一点" / "简单回答" | 自动降级一个复杂度 |
| "详细分析" / "深入思考" | 自动升级一个复杂度 |
| "为什么？" | 回溯推理链，展示推导过程 |

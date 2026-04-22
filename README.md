<p align="center">
  <h1>🧠 Sharp Think</h1>
  <p><strong>结构化思考优化框架 — 让 AI 又快又好地思考</strong></p>
</p>

<p align="center">
  <a href="https://github.com/qingjian0/sharp-think"><img src="https://img.shields.io/badge/GitHub-sharp--think-black?logo=github" alt="GitHub"></a>
  <img src="https://img.shields.io/badge/Trae-Skill-2496ED?logo=visualstudiocode" alt="Trae Skill">
  <a href="https://github.com/qingjian0/sharp-think/stargazers"><img src="https://img.shields.io/github/stars/qingjian0/sharp-think?style=social" alt="Stars"></a>
  <img src="https://img.shields.io/badge/License-MIT-green" alt="MIT License">
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

## 📦 安装

### 系统要求

- **Trae**：将 Skill 文件放入 `.trae/skills/` 目录即可生效
- **其他平台**：任何支持 system prompt 注入的 AI 工具都可以使用（见下方「其他平台」）

### 方式一：手动安装（推荐）

将项目复制到你的 Trae 项目的 `.trae/skills/` 目录下：

```bash
# 进入你的 Trae 项目根目录
cd /path/to/your/project

# 创建 skills 目录（如果不存在）
mkdir -p .trae/skills

# 克隆仓库到 skills 目录
git clone https://github.com/qingjian0/sharp-think.git .trae/skills/sharp-think

# 清理不需要的文件（可选）
rm -rf .trae/skills/sharp-think/.git
```

安装后的目录结构：

```
your-project/
└── .trae/
    └── skills/
        └── sharp-think/
            ├── SKILL.md              # 核心思考框架（Skill 入口）
            └── references/           # 参考卡片库（按需引用）
                ├── cognitive-biases.md
                ├── complexity-scaling.md
                ├── decision-frameworks.md
                └── quality-checklist.md
```

### 方式二：直接粘贴给 AI 安装

如果你在让 Trae、Claude Code、Cursor Agent 或其他终端型 AI 助手代你安装，可以直接粘贴下面这段：

```
请帮我安装 sharp-think：

1. 如果当前目录还没有这个仓库，执行：
   git clone https://github.com/qingjian0/sharp-think.git

2. 进入仓库目录：
   cd sharp-think

3. 将 sharp-think 的内容复制到当前项目的 .trae/skills/sharp-think/ 目录：
   mkdir -p .trae/skills/sharp-think
   cp -r SKILL.md references .trae/skills/sharp-think/

4. 安装完成后请检查以下文件是否存在且可读：
   .trae/skills/sharp-think/SKILL.md
   .trae/skills/sharp-think/references/cognitive-biases.md
   .trae/skills/sharp-think/references/decision-frameworks.md
   .trae/skills/sharp-think/references/quality-checklist.md
   .trae/skills/sharp-think/references/complexity-scaling.md

5. 告诉我安装是否成功。
```

### 方式三：直接下载

下载 [最新 Release](https://github.com/qingjian0/sharp-think/releases) 并解压到 `.trae/skills/sharp-think/`。

### 其他平台

本项目的核心是 `SKILL.md` 和 `references/` 目录下的 Markdown 文件。任何支持 system prompt 注入的 AI 工具都可以使用：

1. 将 `SKILL.md` 作为 system prompt 的一部分注入
2. 将 `references/` 下的参考卡片作为按需加载的参考文档

> [!TIP]
> 安装后 Skill 会在你提问涉及**分析、方案、规划、决策**等关键词时自动触发。

## 🚀 使用方式

### 自动触发

安装后，每次会话中 AI 会根据你的提问自动判断是否加载 Sharp Think。触发关键词：

| 中文 | English |
|------|---------|
| 帮我分析 / 思考 | analyze / think through |
| 写方案 / 设计 | design / plan |
| 做决策 / 对比 | decide / compare |
| 最佳实践 / 优化建议 | best practices / optimize |
| 架构设计 / 技术选型 | architecture / tech stack |
| 问题诊断 / 根因分析 | diagnose / root cause |

### 手动命令入口

仓库提供 `commands/` 目录下的手动命令入口。在支持 Markdown slash commands 的助手里，可直接调用：

```
/sharp-think           🧠 启动结构化思考框架
/sharp-think-l1        ⚡ 强制 L1 直接回答模式
/sharp-think-l3        🔬 强制 L3 深度分析模式
```

### 使用示例

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

### 特殊指令

| 你说的话 | AI 的反应 |
|---------|----------|
| "快一点" / "简单回答" | 自动降级一个复杂度（L3→L2，L2→L1） |
| "详细分析" / "深入思考" | 自动升级一个复杂度（L1→L2，L2→L3） |
| "为什么？" | 回溯推理链，展示推导过程 |
| 多个子问题 | 拆分 → 独立评估 → 按依赖排序 → 依次处理 → 综合结论 |

## 📁 项目结构

```
sharp-think/
├── SKILL.md                          # 核心思考框架（Skill 入口）
├── README.md                         # 本文件
├── LICENSE                           # MIT 许可证
├── .gitignore                        # Git 忽略规则
├── commands/                         # 手动 slash commands 入口
│   ├── sharp-think.md                #   🧠 启动结构化思考
│   ├── sharp-think-l1.md             #   ⚡ 强制 L1 模式
│   └── sharp-think-l3.md             #   🔬 强制 L3 模式
└── references/                       # 参考卡片库（按需引用）
    ├── cognitive-biases.md           # 12 种认知偏差检测清单
    ├── decision-frameworks.md        # 7 种决策框架速查
    ├── quality-checklist.md          # 5 类输出质量检查清单
    └── complexity-scaling.md         # 复杂度分级详细标准
```

## 🗂️ 参考卡片

| 卡片 | 内容 | 何时引用 |
|------|------|---------|
| 🧩 [认知偏差检测](references/cognitive-biases.md) | 确认偏差、锚定效应、沉没成本等 12 种偏差的自检方法 | L3 + 涉及决策/判断 |
| 📊 [决策框架速查](references/decision-frameworks.md) | SWOT、决策矩阵、5-Why、第一性原理等 7 种框架 | L3 + 多方案对比 |
| ✅ [质量检查清单](references/quality-checklist.md) | 文档/分析/方案/创意/代码 5 类输出检查模板 | 所有 L2+ 任务 |
| 📏 [复杂度分级标准](references/complexity-scaling.md) | L1/L2/L3 详细判定标准、边界案例、动态调整 | 首次使用或分级不确定时 |

## 🔧 Troubleshooting

| 问题 | 解决方案 |
|------|---------|
| Skill 未自动触发 | 检查 `SKILL.md` 是否在 `.trae/skills/sharp-think/` 内，front matter 是否完整 |
| AI 仍然过度思考简单问题 | 确认 SKILL.md 中的复杂度分级表未被修改 |
| 参考卡片未被引用 | 确保 `references/` 文件夹与 `SKILL.md` 在同一目录 |
| 输出格式不一致 | 检查 SKILL.md 中的输出格式规范章节是否完整 |

## 💡 设计理念

- **先评估后思考** — 永远先判断问题复杂度，再决定思考深度
- **先对齐后执行** — 确保理解正确后再展开推理
- **结构化输出** — 按统一模板组织思考过程和最终输出
- **质量自检** — 输出前必须通过校验检查点

## 🤝 Contributing

欢迎贡献！你可以：

1. **报告 Bug** — 提交 [Issue](https://github.com/qingjian0/sharp-think/issues) 描述问题
2. **建议改进** — 分享新参考卡片或框架优化想法
3. **提交 PR** — Fork → 修改 → Pull Request

## 📄 License

MIT License — 详见 [LICENSE](LICENSE) 文件。

# 「明思」技能重构

## Description

此次PR将原来的 `sharp-think` 技能重构为「明思」结构化思考优化框架，主要变更包括：

## Changes Made

### 1. 核心技能重构
- 将技能名称从 `sharp-think` 更名为 `mingsi`
- 重构 `SKILL.md`，采用三层架构：快速评估 → 路由调度 → 工具集
- 新增核心原则和可观测行为准则
- 建立完善的参考卡片索引系统

### 2. 新增参考文档
在 `references/` 目录下新增了12个参考文档：
- [complexity-matrix.md](file:///workspace/references/complexity-matrix.md) - L1-L5 复杂度决策矩阵
- [task-types.md](file:///workspace/references/task-types.md) - 任务类型分类
- [subtask-guide.md](file:///workspace/references/subtask-guide.md) - 子任务管理指南
- [common-patterns.md](file:///workspace/references/common-patterns.md) - 常见模式库
- [preflight-checklist.md](file:///workspace/references/preflight-checklist.md) - 前置检查清单
- [observable-rules.md](file:///workspace/references/observable-rules.md) - 可观测行为准则
- [forbidden-rules.md](file:///workspace/references/forbidden-rules.md) - 禁止事项清单
- [theoretical-basis.md](file:///workspace/references/theoretical-basis.md) - 理论依据
- [troubleshooting.md](file:///workspace/references/troubleshooting.md) - 故障排除指南
- [quick-reference.md](file:///workspace/references/quick-reference.md) - 快速参考表

### 3. 新增专项工具
在 `skills/` 目录下新增了10个专项工具：
- [l1-direct](file:///workspace/skills/l1-direct/SKILL.md) - L1 直接回答
- [l2-brief](file:///workspace/skills/l2-brief/SKILL.md) - L2 简要分析
- [l3-standard](file:///workspace/skills/l3-standard/SKILL.md) - L3 标准分析
- [l4-deep](file:///workspace/skills/l4-deep/SKILL.md) - L4 深度分析
- [l5-comprehensive](file:///workspace/skills/l5-comprehensive/SKILL.md) - L5 全面研究
- [router](file:///workspace/skills/router/SKILL.md) - 明思路由器
- [workflows](file:///workspace/skills/workflows/SKILL.md) - 工作流组合
- [contradiction-analysis](file:///workspace/skills/contradiction-analysis/SKILL.md) - 矛盾分析
- [investigation-first](file:///workspace/skills/investigation-first/SKILL.md) - 调查研究
- [concentrate-forces](file:///workspace/skills/concentrate-forces/SKILL.md) - 集中兵力
- [criticism-self-criticism](file:///workspace/skills/criticism-self-criticism/SKILL.md) - 批评与自我批评

### 4. 工作流系统
新增3个标准工作流：
- Workflow 1：新项目启动 - 从零开始面对新任务
- Workflow 2：复杂问题攻坚 - 处理已知但难以解决的问题
- Workflow 3：方案迭代优化 - 已有方案的迭代改进

### 5. 新增辅助文档
- [analysis-subtask-optimization.md](file:///workspace/analysis-subtask-optimization.md) - 子任务处理优化分析
- 创建 `mingsi-skills/` 目录，包含完整的技能副本

## Key Features

1. **五级复杂度分级** - 根据任务复杂度选择合适的分析深度
2. **工作流组合** - 多种工具按正确顺序组合使用
3. **子任务管理** - 复杂任务的拆分和管理
4. **可观测行为** - 明确质量标准的可观测行为
5. **参考卡片系统** - 快速查找所需信息

## Testing

- 已验证文件结构完整
- 所有新增文档内容正确
- 参考卡片索引有效

## Checklist

- [ ] 代码已测试
- [ ] 文档已更新
- [ ] 遵循项目标准
- [ ] 无破坏性变更

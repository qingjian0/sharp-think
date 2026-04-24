# GitHub 仓库重命名和PR创建指南

## 一、仓库重命名步骤

### 在 GitHub 网站上重命名仓库
1. 访问 https://github.com/qingjian0/sharp-think
2. 点击仓库页面右上角的 "Settings"
3. 在 "Repository name" 字段中输入新名称：`mingsoli-skill`
4. 点击 "Rename" 按钮确认

### 更新本地 git 远程仓库地址
重命名后，在本地运行：
```bash
cd /workspace
git remote set-url origin https://github.com/qingjian0/mingsoli-skill
```

## 二、创建 Pull Request (PR)

### 1. 访问 PR 创建页面
访问：https://github.com/qingjian0/sharp-think/compare/main...trae/solo-agent-rMCkYa

### 2. 填写 PR 信息
- **Title**：「明思」技能重构 - 结构化思考优化框架
- **Description**：复制 [PULL_REQUEST_TEMPLATE.md](file:///workspace/PULL_REQUEST_TEMPLATE.md) 的内容

### 3. 创建 PR
点击 "Create pull request" 按钮

## 三、PR 内容预览

### 标题
「明思」技能重构 - 结构化思考优化框架

### 主要内容
- 技能名称从 `sharp-think` 更名为 `mingsi`
- 新增 12 个参考文档
- 新增 10 个专项工具
- 新增 3 个标准工作流
- 完整的子任务管理系统

## 四、快速参考

| 项目 | 链接 |
|------|------|
| 当前仓库 | https://github.com/qingjian0/sharp-think |
| 分支 | trae/solo-agent-rMCkYa |
| PR 模板 | [PULL_REQUEST_TEMPLATE.md](file:///workspace/PULL_REQUEST_TEMPLATE.md) |

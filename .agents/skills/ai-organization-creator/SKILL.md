---
name: ai-organization-creator
description: 一键初始化 AI 虚拟企业系统 (AI Organization OS v1.0) 的全部目录与配置文件。
---

# AI Organization Creator Skill - 一键系统初始化指南

本 Skill 专用于在任何新项目的根目录下一键初始化 **AI Organization Operating System v1.0 (AI Org OS)** 的全套目录结构和 42 个核心配置规范。

## 1. 触发时机与条件
当用户在输入框里以斜杠命令形式调用 `/ai-organization-creator`，或者提及以下关键字或意图时，AI 必须主动加载并执行本技能：
- “初始化 AI 组织 / AI 虚拟企业”
- “创建 AI Org OS / AI 组织系统”
- “在这个项目生成 AI 公司的目录与配置”
- “运行 ai-organization-creator”

## 2. 自动化执行逻辑
不需要人工逐步生成这 42 个文件。为了最高效率与 100% 的准确性，AI 应该直接使用系统 Python 环境来运行技能包中预设的初始化脚本：

### 执行步骤
1. **运行初始化脚本**：
   在终端（Terminal）中，以当前项目根目录为 Cwd，运行以下命令：
   ```bash
   python3 "/Users/croodslee/.gemini/antigravity/builtin/skills/ai-organization-creator/scripts/initialize_org.py"
   ```
2. **校验生成状态**：
   执行完脚本后，运行 `ls -la .ai-organization` 或者是 `find .ai-organization -type f` 确保以下目录和文件已全部创建成功：
   - `.ai-organization/README.md`
   - `.ai-organization/core/` (5个核心政策文件)
   - `.ai-organization/organization/` (2个架构配置文件)
   - `.ai-organization/registry/` (3个注册表文件)
   - `.ai-organization/agents/` (19个岗位说明书/System Prompts)
   - `.ai-organization/skills/` (7个行为规范技能包)
   - `.ai-organization/templates/` (5个协作流程模板)
   - 工作区根目录下的 `AGENTS.md` (融合了组织规范的开发原则文件)

3. **结果交付汇报**：
   向用户反馈初始化成功，并向用户提供生成的 [README.md](file:///.ai-organization/README.md) 点击链接，引导用户开启模拟演练。

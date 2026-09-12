## 已归档 · 2026-09-12

后续维护入口：[Qiaolab_skills](https://github.com/Yu-Qiao-sjtu/Qiaolab_skills)。

五个完整技能目录及参考材料已迁移到 skills/。

本仓库保留原始源码与提交历史，不再维护。请从新仓库安装所需的完整技能目录。

---

# Wisp_skills

基于 [cangjie-skill](https://github.com/kangarooking/cangjie-skill) 方法论蒸馏的结构化 Agent Skill 集合，格式兼容 [wisp-science](https://github.com/xuzhougeng/wisp-science) 加载规范。每个 Skill 是一个可独立部署的知识单元，包含方法论骨架、触发场景和可执行步骤。

## 致谢

本项目 fork 自 [cangjie-skill](https://github.com/kangarooking/cangjie-skill)，并兼容 [wisp-science](https://github.com/xuzhougeng/wisp-science) 的 Skill 格式。感谢两个上游项目的开源贡献：

### [cangjie-skill](https://github.com/kangarooking/cangjie-skill)

> 把书、长视频、播客里的方法论，蒸馏成可调用的 AI Skills。

**Cangjie Skill** 是一套知识蒸馏方法论与流水线，使用 RIA-TV++ 七阶段流程（整体理解 → 并行提取 → 三重验证 → RIA++ 构造 → Zettelkasten 链接 → 压力测试 → 交付），将书籍、视频转写、播客文字稿等原始内容变成可独立调用、可组合使用、可压力测试的 Agent Skill 工具包。本仓库的所有 Skill 均通过 cangjie-skill 方法论蒸馏产出。

### [wisp-science](https://github.com/xuzhougeng/wisp-science)

> Open-source, local-first desktop AI research workbench.

**Wisp Science** 是一个开源的本地优先桌面 AI 科研助手和科学计算工作台。它连接 OpenAI 兼容和 Anthropic 模型，运行持久 Python/R 环境，加载可复用的 Agent Skills（`SKILL.md`），并通过内置 MCP 服务器连接约 80 个生物信息学数据库。基于 Rust + Tauri v2 + Leptos 构建，支持跨平台桌面应用和命令行两种运行模式。本仓库的 Skill 格式遵循 Wisp Science 的 Skill 加载规范。

**作者**：[徐洲更](https://xuzhougeng.top/)（Xu Zhougeng），中国科学院分子植物科学卓越创新中心博士后，遗传学博士。专注于基因组学分析与生物信息学教程创作（全网阅读量超 200 万），在 *Cell*、*Nature Methods*、*Nature Communications*、*Science*、*PNAS* 等期刊发表多篇论文。独立开发 WispTerm、CiteBox、Baize 等多款 AI for Science 工具。

---

## Skill 列表

### 面向 AI4Science 的跨领域科研思维（推荐优先使用）

| Skill | 来源 | 模块数 | 简介 |
|-------|------|--------|------|
| [research-thinking-insights](./research-thinking-insights/) | 三场访谈跨领域蒸馏 | 9 | **面向AI4Science**：问题定义优先(80/20)、系统化排错、能做实验=能往前走、干净>花哨、第一性原理、喇叭口跨域思维、不抄作业、环境>经验、靠谱>聪明 |

### 原始访谈技能包

| Skill | 来源 | 模块数 | 简介 |
|-------|------|--------|------|
| [ai-insider-research](./ai-insider-research/) | B站访谈（姚顺宇 x 张小珺） | 8 | AI大模型训练前沿实战：预训练/后训练Scaling、Coding爆发、问题定义优先、组织文化 |
| [semiconductor-chip-insight](./semiconductor-chip-insight/) | B站访谈（廖恒 x 张小珺） | 8 | 半导体芯片产业认知：18层宝塔、韬定律、Co-Design协同优化、问题定义优先 |
| [ai-paradigm-shift](./ai-paradigm-shift/) | B站访谈（罗福莉 x 张小珺） | 8 | AI范式巨变下的Agent时代：OpenClaw引发巨变、群体智能、Code泛化力、组织平权 |

## 与上游项目的关系

本项目是 [cangjie-skill](https://github.com/kangarooking/cangjie-skill) 的下游产出，同时也是 [wisp-science](https://github.com/xuzhougeng/wisp-science) 的 Skill 生态贡献：

```
cangjie-skill (RIA-TV++ 蒸馏方法论)
       │
       ▼ fork & 蒸馏产出
Wisp_skills (本仓库，3个访谈Skill + 1个跨访谈科研思维Skill)
       │
       ▼ 格式兼容
wisp-science (.wisp/skills/ 加载规范)
```

**Fork 关系**：本仓库的蒸馏流程完全遵循 cangjie-skill 的 RIA-TV++ 七阶段方法论，SKILL.md 的内容结构（R原文/I方法论/A1案例/A2触发/E执行/B边界）来源于此。唯一的格式适配是将 `description` 压缩为单行字符串，以兼容 wisp-science 的 YAML 解析器。

**兼容性**：所有 Skill 均符合 wisp-science 的加载规范（大写 `SKILL.md` + 单行 `name`/`description` frontmatter + 文件夹名与 `name` 一致），可直接放入 `.wisp/skills/` 目录使用。

## 蒸馏方法

采用 [cangjie-skill](https://github.com/kangarooking/cangjie-skill) 的 RIA-TV++ 方法论：

1. **阶段0**：整源理解（Adler四步法）
2. **阶段1**：并行提取候选模块
3. **阶段1.5**：三重验证（跨域/预测力/独特性）
4. **阶段2**：RIA++ 构造（R原文 / I方法论 / A1案例 / A2触发 / E执行 / B边界）
5. **阶段3**：Zettelkasten 链接 + INDEX
6. **阶段4**：压力测试
7. **阶段5**：交付 SKILL.md

## 安装

### 方式一：wisp-science（推荐）

```bash
# 克隆到 wisp-science 项目的 .wisp/skills/ 目录
cd your-wisp-science-project
git clone https://github.com/Yu-Qiao-sjtu/Wisp_skills.git .wisp/skills/temp
# 将需要的 skill 移入
cp -r .wisp/skills/temp/ai-paradigm-shift .wisp/skills/
rm -rf .wisp/skills/temp
```

### 方式二：Claude Code / Cursor

```bash
# 将任意 Skill 的 SKILL.md 复制到你的 agent skills 目录
cp ai-paradigm-shift/SKILL.md ~/.claude/skills/
```

*感谢 [kangarooking](https://github.com/kangarooking) 和 [Xu Zhougeng](https://xuzhougeng.top/) 的开源贡献。*

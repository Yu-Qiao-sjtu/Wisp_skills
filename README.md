# Wisp_skills

基于视频/书籍/播客等知识源蒸馏的结构化 Agent Skill 集合。每个 Skill 是一个可独立部署的知识单元，包含方法论骨架、触发场景和可执行步骤。

## Skill 列表

| Skill | 来源 | 模块数 | 简介 |
|-------|------|--------|------|
| [ai-insider-research](./ai-insider-research/) | B站访谈（姚顺宇 x 张小珺） | 8 | AI大模型训练前沿实战：预训练/后训练Scaling、Coding爆发、问题定义优先、组织文化 |
| [semiconductor-chip-insight](./semiconductor-chip-insight/) | B站访谈（廖恒 x 张小珺） | 8 | 半导体芯片产业认知：18层宝塔、韬定律、Co-Design协同优化、问题定义优先 |

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

```bash
# 将任意 Skill 的 SKILL.md 复制到你的 agent skills 目录
cp ai-insider-research/SKILL.md ~/.claude/skills/
```

## 致谢

本仓库的所有 Skill 均基于以下两个开源项目构建：

### [cangjie-skill](https://github.com/kangarooking/cangjie-skill)

> 把书、长视频、播客里的方法论，蒸馏成可调用的 AI Skills。

**Cangjie Skill** 是一套知识蒸馏方法论与流水线，使用 RIA-TV++ 七阶段流程（整体理解 → 并行提取 → 三重验证 → RIA++ 构造 → Zettelkasten 链接 → 压力测试 → 交付），将书籍、视频转写、播客文字稿等原始内容变成可独立调用、可组合使用、可压力测试的 Agent Skill 工具包。本仓库的所有 Skill 均通过 cangjie-skill 方法论蒸馏产出。

### [wisp-science](https://github.com/xuzhougeng/wisp-science)

> Open-source, local-first desktop AI research workbench.

**Wisp Science** 是一个开源的本地优先桌面 AI 科研助手和科学计算工作台。它连接 OpenAI 兼容和 Anthropic 模型，运行持久 Python/R 环境，加载可复用的 Agent Skills（`SKILL.md`），并通过内置 MCP 服务器连接约 80 个生物信息学数据库。基于 Rust + Tauri v2 + Leptos 构建，支持跨平台桌面应用和命令行两种运行模式。本仓库的 Skill 格式遵循 Wisp Science 的 Skill 加载规范。

**作者**：[徐洲更](https://xuzhougeng.top/)（Xu Zhougeng），中国科学院分子植物科学卓越创新中心博士后，遗传学博士。专注于基因组学分析与生物信息学教程创作（全网阅读量超 200 万），在 *Cell*、*Nature Methods*、*Nature Communications*、*Science*、*PNAS* 等期刊发表多篇论文。独立开发 WispTerm、CiteBox、Baize 等多款 AI for Science 工具。

---

*感谢 [kangarooking](https://github.com/kangarooking) 和 [Xu Zhougeng](https://xuzhougeng.top/) 的开源贡献。*

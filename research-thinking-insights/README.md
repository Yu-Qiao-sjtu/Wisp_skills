# research-thinking-insights

## 概述

从三场B站深度访谈中提炼的**跨领域科研思维方法论**，面向 AI4Science 研究者。

三个原始访谈 skill 分别聚焦 AI 训练、芯片设计、Agent 范式——本 skill 不压缩不删减原始内容，而是在其之上增加一层"科研方法论蒸馏层"，把产业洞察翻译成科研思维工具。

## 源材料

| 访谈 | 嘉宾 | 原始技能包 |
|------|------|-----------|
| [BV1YR5E6EE9o](https://www.bilibili.com/video/BV1YR5E6EE9o/) | 姚顺宇（Anthropic→Google DeepMind） | [ai-insider-research](../ai-insider-research/) |
| [BV1nB3u6tERu](https://www.bilibili.com/video/BV1nB3u6tERu/) | 廖恒（华为半导体首席科学家） | [semiconductor-chip-insight](../semiconductor-chip-insight/) |
| [BV1iVoVBgERD](https://www.bilibili.com/video/BV1iVoVBgERD/) | 罗福莉（小米大模型团队负责人） | [ai-paradigm-shift](../ai-paradigm-shift/) |

## 蒸馏信息

| 字段 | 值 |
|------|-----|
| **蒸馏日期** | 2026-07-31 |
| **蒸馏方法** | 跨访谈交叉验证 + AI4Science场景适配 |
| **模块数** | 9个核心模块，3大板块 |
| **文件清单** | `SKILL.md` / `BOOK_OVERVIEW.md` / `INDEX.md` |

## 技能概览

本技能包含 9 个模块，分为 3 个板块：

| 板块 | 模块 | 核心内容 | 来源 |
|------|------|---------|------|
| A. 研究方法论 | ★ 问题定义优先（80/20） | 问题定义占80%价值，方法实现占20% | 姚顺宇+廖恒 |
| A. 研究方法论 | ★ 系统化排错 | "结果不对"三种原因，绝大多数是bug | 姚顺宇 |
| A. 研究方法论 | ★ 能做实验=能往前走 | AI像18世纪热力学，理论实验不分家 | 姚顺宇 |
| A. 研究方法论 | ★ 干净>花哨 | 基线做好>花哨新方法，修bug>神奇技巧 | 姚顺宇+廖恒 |
| B. 跨域思维 | ★ 第一性原理 | 理解物理本质，不光学how要学why | 廖恒+姚顺宇 |
| B. 跨域思维 | 跨域迁移——喇叭口 | 三人跨域路径，上下游追踪 | 廖恒+姚顺宇 |
| B. 跨域思维 | 不抄作业原则 | 四个致命问题，学习≠抄作业 | 廖恒 |
| C. 品质与环境 | ★ 环境>经验+靠谱>聪明 | 两个跨领域共识 | 三人共识 |
| C. 品质与环境 | 持续自我否定 | 范式转移中的个人应对策略 | 罗福莉+姚顺宇 |

## 交叉发现：三位实践者的独立共识

| 共识 | 姚顺宇 | 廖恒 | 罗福莉 |
|------|--------|------|--------|
| 问题定义占80% | ✓ | ✓ | ✓ |
| 靠谱>聪明 | ✓ | ✓ | ✓ |
| 范式转移中速度>静态实力 | ✓ | ✓ | ✓ |

## 安装

```bash
# 将 SKILL.md 复制到你的 skills 目录
cp SKILL.md ~/.claude/skills/
# 或 wisp-science
cp SKILL.md .wisp/skills/research-thinking-insights/
```

## 相关技能

- [ai-insider-research](../ai-insider-research/) — 原始访谈（姚顺宇），AI大模型训练前沿实战
- [semiconductor-chip-insight](../semiconductor-chip-insight/) — 原始访谈（廖恒），芯片产业认知与架构设计
- [ai-paradigm-shift](../ai-paradigm-shift/) — 原始访谈（罗福莉），AI范式巨变下的Agent时代

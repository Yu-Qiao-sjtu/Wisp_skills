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

## 相关仓库

- [wisp-science](https://github.com/xuzhougeng/wisp-science) — 科研文献智能体系统
- [cangjie-skill](https://github.com/kangarooking/cangjie-skill) — 知识蒸馏方法论与流水线

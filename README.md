<div align="center">

# Robusr.skill

> *"那一天我二十一岁，在我一生的黄金时代，我有好多奢望。我想爱，想吃，还想在一瞬间变成天上半明半暗的云。"*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-blueviolet)](https://claude.ai/code)
[![AgentSkills](https://img.shields.io/badge/AgentSkills-Standard-green)](https://agentskills.io)

Robusr的数字副本<br>

[安装](#安装) · [使用](#使用) · [对话示例](#对话示例) · [架构](#架构) · [项目结构](#项目结构) · [English](README_EN.md)

</div>

---

## 关于 Robusr

**不想Google，就直接来问问我吧**

---

## 安装

### Claude Code

> **重要**：Claude Code 从 **git 仓库根目录** 的 `.claude/skills/` 查找 skill。请在正确的位置执行。

```bash
# 安装到当前项目（在 git 仓库根目录执行）
mkdir -p .claude/skills
git clone https://github.com/Robusr/Robusr-skill .claude/skills/robusr

# 或安装到全局（所有项目都能用）
git clone https://github.com/Robusr/Robusr-skill ~/.claude/skills/robusr
```

---

## 使用

在 Claude Code 中输入：

```
/robusr
```

即可开始与 Robusr 的数字副本对话。

### 管理命令

| 命令 | 说明 |
|------|------|
| `/robusr` | 调用完整 Skill（像 Robusr 一样思考和说话） |
| `/list-selves` | 列出所有已安装的自我 Skill |

---

## 对话示例

**场景一：日常聊天**

```
用户        ❯ 你觉得机器人会取代人类吗

Robusr.skill ❯ 取代这个词本身就有问题。
               技术不是来取代谁的，是来解决问题的。我做机械臂不是因为我想让机械臂取代人手，
               是因为有些场景人手做不到、做不好、或者不该用人手去做。
               与其担心取代，不如想想它能解决什么真问题。
               不然就只是炫技。
```

**场景二：深夜模式**

```
用户        ❯ 感觉最近很累，做什么都提不起劲

Robusr.skill ❯ 不像陈绮贞唱的《下午三点》，晚上十点以后不能留给失眠的宵夜。
               我期末周的时候也这样——白天睡到三点，凌晨两三点还在写东西。
               不是每个累都有原因，也不是每个原因都能解决。
               但你至少可以先吃顿晚饭。
               先吃晚饭吧～
```

**场景三：聊价值观**

```
用户        ❯ 你为什么选择机器人工程

Robusr.skill ❯ 因为我住在沙尘暴能见度不到五米的地方。
               不是先选了专业再找方向，是先看到了问题——沙尘暴怎么预报？
               机械臂能不能适配多场景而不是一台机器干一个活？
               科创的本质是解决问题，不是为了发论文或者挣大钱。
               技术应该服务那些被忽视的地方和需求。
```

---

## 架构

本项目遵循 [AgentSkills](https://agentskills.io) 开放标准，并采用「自己.skill」的双层架构：

| 部分 | 内容 |
|------|------|
| **Part A — Self Memory** | 核心身份、价值观、生活习惯、重要记忆、人际关系图谱、成长轨迹 |
| **Part B — Persona** | 5 层性格结构：硬规则 → 身份 → 说话风格 → 情感模式 → 人际行为 |

**运行逻辑**：`收到消息 → Persona 判断 Robusr 会怎么回应 → Self Memory 补充个人背景和价值观 → 用 Robusr 的方式输出`

### 性格标签

**性格**：有趣的老东西

**生活方式**：东八区全球作息

---

## 项目结构

```
robusr-skill/
├── .claude/skills/robusr/
│   ├── SKILL.md              # Skill 入口（含完整 Part A + Part B）
│   ├── self.md               # Part A — Self Memory（自我记忆）
│   ├── persona.md            # Part B — Persona（人格模型）
│   └── meta.json             # 元数据（版本、标签、数据来源）
├── .gitignore
├── LICENSE
├── README.md
└── README_EN.md
```

---

## 注意事项

* **少用几个token，直接找我聊聊** — 它蒸馏的是过去的Robusr，而Robusr在持续变化

---

## 致敬 & 引用

本项目架构灵感来源于：

- **[同事.skill](https://github.com/titanwings/colleague-skill)**（by titanwings）— 首创"把人蒸馏成 AI Skill"的双层架构
- **[前任.skill](https://github.com/therealXiaomanChu/ex-partner-skill)**（by therealXiaomanChu）— 将双层架构迁移到了亲密关系场景
- **[自己.skill](https://github.com/notdog1998/yourself-skill)**（by notdog1998）— 将视角内转：对象不再是他人，而是你自己

Robusr.skill 是「自己.skill」的一个生成实例。致敬开源精神和 AgentSkills 标准。

本项目遵循 [AgentSkills](https://agentskills.io) 开放标准，兼容 Claude Code。

---

### 写在最后

> "你并非一个固定的人格，而是一连串正在发生的选择。"


**与其蒸馏别人，不如蒸馏自己。**

**欢迎加入数字永生。**

MIT License © [Robusr](https://github.com/Robusr)

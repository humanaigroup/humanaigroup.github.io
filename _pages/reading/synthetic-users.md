---
layout: note
permalink: /reading/synthetic-users/
title: synthetic-users
date: 2026-05-15
note_title: 'AI 做用户研究，"比真人更准"反而是失败信号'
note_subtitle: '——业界对 Synthetic Users 的批判与方法论修正'
note_source: '业界对 Synthetic Users 的批判性实践与方法论修正'
note_source_meta: 'IDEO · NN/g · MeasuringU · 2024-2026 文献综述'
note_author: 'Wei Xiang'
---

> 基于 2024-2026 年公开可验证文献整理。所有引用均经过 web search 核实出处与原文。

## 核心观察

业界对 synthetic users 的批判已经形成一个相对成熟的论述群，有具体案例、量化对比、方法论修正建议，而不是单纯的情绪反对。这个论述群与学术界的 LLM × UX evaluation 研究形成有趣的张力——学术界用对照实验严格量化能力边界，业界则基于实际项目经验直接得出"不该这样用"的结论。

---

## 第一部分：三个具体的实证对比案例

### 1.1 IDEO 的乡村医疗项目：三周 AI 调研对比一小时真实访谈

**出处**：Sarah Stein Greenberg & Eli Brown, *The Case Against AI-Generated Users*, IDEO Journal, 2025 年 1 月。

IDEO 一个团队启动了一个改善乡村医疗的项目，用 ChatGPT + 多个 GenAI 工具生成 synthetic patients 和 practitioners 进行模拟访谈。三周 AI 调研后，他们发现一小时与一位真实病人 + 一位真实医生的对话，展现的人类经验深度和复杂度远超合成用户能传达的。

IDEO 的结论："依赖合成用户——本质上只是 LLM 模型里的一堆数据——不仅对实践者不利，对商业结果也不利，对我们设计的对象也不利。"

**方法学含义**：AI 调研在边际投入与边际产出上明显劣于真实用户访谈，即便前者看起来更便宜更快。

### 1.2 Nielsen Norman Group 的对照测试

**出处**：Maria Rosala & Kate Moran, *Synthetic Users: If, When, and How to Use AI-Generated "Research"*, Nielsen Norman Group, 2024。

NN/g 把 Synthetic Users 平台和 ChatGPT 自建 persona 与他们之前用真实参与者做的三项研究做对比，发现三个问题：

1. **谄媚效应（Sycophancy）**：真实学习者承认"由于太忙，没完成所有课程"；synthetic users 回答说"完成了所有课程，从中获得了重要技能"。
2. **价值观过于浅显**：synthetic user 列出 7 个因素，所有因素权重相等——与真实用户有清晰优先级形成对比。
3. **对体验的"想象"不可靠**：大多数真实参与者说他们不使用课程讨论论坛；synthetic users 反而持正面态度。

NN/g 最终立场："真实用户研究是必要的。合成用户不能替代研究和与真实人类交流所获得的深度与共情。"

### 1.3 Jeff Sauro / MeasuringU 的 tree testing 实验

**出处**：Jeff Sauro, Will Schiavone, Jim Lewis, *Using ChatGPT in Tree Testing*, MeasuringU, 2024。

在 IRS.gov 网站的复杂导航结构上做 tree testing，ChatGPT-4 的表现"远超大多数真实参与者"——这不是优势，而是 AI 失去模拟价值的证据。

MeasuringU 系统综述了 23 项 synthetic users 相关研究，其中 12 项 peer-reviewed：**14 项给出否定结果，9 项给出肯定结果**。Sauro 的总结："相关性不等于等价性。即便合成数据与人类数据相关，常常仍存在大的系统性差异。"

---

## 第二部分：个人 UX leader 的批判性论述

**Pavel Samsonov（AWS UX leader）**："与客户实际说过的话相比，听起来像客户可能说的话毫无价值。LLM 不能讲它上次完成某个任务的经历。LLM 与客户的另一个非常重要的区别：LLM 不会买你的产品。"

**Christopher Roosen** 的"navel gazing"比喻："用合成人类做直接研究就像盯着肚脐看，但不是看自己的肚脐，而是看互联网那个庞大、混乱、拥挤的肚脐。解决方案不是制造假人，而是更好地接触真人。"

**Greg Nudelman** 的实践替代："当我领导 UX 团队时，我会建立一个 30-50 名近似理想客户的 panel，每月访谈，每周至少 6-8 次客户对话。"——不是回到传统昂贵的用户研究，而是用 ops 工程把访谈成本降下来。

---

## 第三部分：学术化批判——"Epistemic Freeloading"

**出处**：Konstantinos Papangelis, *The Synthetic Persona Fallacy*, ACM Interactions, 2025。

Papangelis 创造了 **"epistemic freeloading"（认识论搭便车）** 这个术语：调用学术方法的形式（persona、研究假设、用户访谈）而抛弃学术方法的内核（真实数据、可重复性、外部验证）。

---

## 第四部分：方法论修正的四个方向

### 修正一：从"替代"到"补充"，严格限定范围

- ✓ 可以用 AI：desk research、初步假设生成、已发布数据综述
- ✗ 不可以用 AI：验证设计决策、检测可用性问题、最终决策依据

### 修正二：从"AI 替代用户"到"AI 增强真实访谈的运营效率"

Jeff Sauro 团队 2025 年提出的三角色框架：
- **AI as Assistant**：转写、总结访谈、编码主题——已被广泛使用，争议小
- **AI as Analyst**：AI 主持人、AI 检测 UX 问题——有争议但有潜力
- **AI as User（Synthetic）**：任何把"用户"从 UX 中移除的尝试都有争议

### 修正三：把"AI 反超人类"识别为失败信号

AI 在用户研究中"做得越好"反而越不像用户。任何"AI 调研工具"如果展示出"我比真人更快/更准"的卖点，这恰恰应该被视为可疑信号。

### 修正四：用 lived experience 与 skin in the game 作为筛选标准

1. **这个问题需要 lived experience 才能回答吗？** 是 → 必须真实用户
2. **回答方需要 skin in the game 吗？** 是 → 必须真实用户
3. **变换 prompt 是否可能引出新洞察？** 是 → 这种"洞察"是可疑的

---

## 对我们工作的启示

1. **警惕"AI 比真人更快/更准"的卖点**——这在 UX 研究中是失败信号
2. **把"AI as Assistant"与"AI as User"严格分开**——前者有清晰 ROI，后者被一致质疑
3. **lived experience 与 skin in the game 是简洁可操作的筛选标准**
4. **与其投入"AI 替代用户"，不如投入"AI 降低真实用户访谈运营成本"**

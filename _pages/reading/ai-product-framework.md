---
layout: note
permalink: /reading/ai-product-framework/
title: ai-product-framework
date: 2026-05-15
note_title: 'AI 产品设计的四步框架——从 NotebookLM 说起'
note_subtitle: ''
note_source: 'AI 产品 User Needs 与功能：四步框架'
note_source_meta: 'PAIR Guidebook · NotebookLM 实践 · 教学材料'
note_author: 'Wei Xiang'
---

> 整合 Google PAIR Guidebook、王珊 NotebookLM 团队实践、认知过程理论。面向 AI Behavior Designer 的四步工作流。

## 核心立场

**AI 产品的 user needs 不是"用户要什么功能"，而是"AI 应该接管/辅助用户的哪一段认知过程"。** 这是 AI-native 与 SaaS-native 的根本分野。

## AI Behavior Designer：一个新职能

AI 时代正在催生 AI Behavior Designer（AI 行为设计师）。它不是把"产品经理"或"交互设计师"换个新名字，而是 PM、Designer、Linguist、Risk Officer 四种职能能力的交集：

- **Product Manager** — 定义场景 · 评估价值
- **Designer** — 编排行为 · 人格与时机
- **Linguist** — 语气 · 勘误 · 提问架构
- **Risk Officer** — 画边界 · 写降级剧本

---

## Step 1 · 发现：找到用户需求与 AI 优势的交集

**核心问题：** 这是一个真实的用户需求吗？AI 是否能为它提供独特价值？

两个判断动作：

**① AI 能不能加分？** 用 PAIR 的模板写一句话假设："我们认为 AI（能/不能）帮助解决（用户需求），因为（理由）。"如果写不出"理由"，就是伪需求，直接停。

**② AI 应该自动化还是增强？** 如果用户享受过程、"正确做法"无共识——选增强。如果任务重复、标准清晰——选自动化。

**NotebookLM 案例：** "我们认为 AI 能帮助解决'用户有大量阅读材料但没时间读完'这一需求，因为 AI 可以把书面材料转换成符合听觉认知节奏的对话式音频。" → 增强（用户享受学习过程）→ Go。

---

## Step 2 · 定义：认知过程三角（枢纽）

**核心命题（王珊原话）：** "问题不是做什么功能，而是替用户完成什么认知过程。"

三个支柱必须同时定义、互相校准：

### 支柱 A · UNDERSTAND — 用户需要理解什么

- **输入维度** — 用户提供给系统的是什么？
- **输出维度** — 用户期望得到什么"认知结果"？
- **时机维度** — 什么场景、什么节点需要 AI 介入？
- **Bloom 层级** — Remember / Understand / Apply / Analyze / Evaluate / Create

### 支柱 B · CAPABILITY — AI 能给什么

- **推理模式** — 检索 · 总结 · 归纳 · 演绎 · 辩论 · 多智能体协作
- **输出模态** — 文本 · 语音 · 视觉 · 交互式 widget
- **语言层** — 语气与人格、勘误策略、提问架构
- **反馈回路** — 用户能用什么方式纠正/调教 AI？

### 支柱 C · BOUNDARY — 设计师定义边界

- **做的清单** — 显式列出范围内的任务
- **不做的清单** — 显式列出范围外的任务
- **审批链** — AI 自主决定 / 用户确认 / 人工审批（按风险分级）
- **降级剧本入口** — 边界外的情况会发生什么？

### 三角自洽性检查

- U 要求的 Bloom 层级 ≤ C 能达到的层级（避免能力缺口）
- C 能做的范围 ≤ B 允许的范围（避免越权）
- B 允许的范围 ≥ U 真正需要的范围（避免过度保守）
- 三个支柱中任一支柱有空缺 = PRD 空心化

**NotebookLM 案例：** UNDERSTAND（用户要听不要读，Understand + Analyze 层级）× CAPABILITY（多智能体辩论 + disfluency 自然语音）× BOUNDARY（不做版权敏感，不做单一作者批评）。三角自洽。

---

## Step 3 · 标准：设计 Reward Function

**核心问题：** AI 怎么知道自己做对了/做错了？

三类指标：
- **准确性** — 事实正确率、hallucination 率
- **效率** — 用户节省多少时间/步骤
- **满意度** — 用户对产出的主观评价

**Goodhart's Law 自查：** "任何指标一旦成为目标就不再是好指标。"对每一个 reward 指标必须问：如果团队只追这一个指标，会发生什么坏结果？

**NotebookLM 案例：** 满意度当前值 4.2，已接近 Goodhart 警戒带——"高分是不是来自人格魅力而非真正有用？"

---

## Step 4 · 回环：Failure 的定义与应对

**核心命题：** AI 失败不是异常，是常态。产品如何定义失败？如何让用户在失败发生时能继续前进？

### Failure 沿三角分类

- **U-failure**：用户认知任务定义错了
- **C-failure**：AI 能力不到位
- **B-failure**：边界越界/责任不清

### Graceful Failure 三原则

1. **Communicate** — 显式告诉用户失败了，不要假装成功
2. **Empower** — 失败发生时提供降级方案、人工兜底
3. **Reduce future** — 把这次失败转化为下次的训练信号

### 框架闭环

Failure 发现的问题常常不是模型问题，而是 Step 2 三角某一边定义错了。Step 4 的产出物之一是修订后的 Behavior Spec——失败不是流程末端的"擦屁股"，而是回到 Step 2 修订三角的最重要入口。

---

## 整套框架的真正价值

不是给 PM 一份做不完的 checklist，而是让 AI Behavior Designer 这个新职能在四个具体动作上有了共同语言——四张图就是四种共同语言的视觉表达。

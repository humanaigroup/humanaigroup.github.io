---
layout: subpage
permalink: /research/
title: research
nav: true
nav_order: 2
nav_active: research
page_title_short: Research
page_eyebrow: "RESEARCH · 研究"
page_title_display: "Research · 研究方向"
page_tagline: "Interaction and experience in complex, dynamic, high-stakes scenarios."
---

<div class="research-overview">
  <div class="research-overview-main">
    <p class="research-overview-en">We study how humans and intelligent systems interact in complex scenarios — autonomous driving, aviation, emergency medicine, elder care. Equipment is intricate, scenes shift fast, and task overload is the norm.</p>
    <p class="research-overview-zh zh">在工程机械集群、航空航天、腹腔镜手术等场景中，设备操控繁复、场景变化多样，导致任务响应过载。我们研究这些复杂场景中的人机交互策略与设计。</p>
  </div>
  <div class="research-overview-approach">
    <div class="research-overview-label">APPROACH · 思路</div>
    <p>理解与增强交互情境中的用户</p>
    <p class="research-overview-approach-en">Understand and augment users in interaction contexts — by simulating their experience to locate problems, and by building systems that enhance their performance in real time.</p>
  </div>
</div>

<hr class="divider" style="margin: 48px 0;">

<!-- ===== Pillar 1 ===== -->
<div class="research-pillar">
  <div class="research-pillar-header">
    <div class="research-pillar-number">01</div>
    <div>
      <h2 class="research-pillar-title">User Simulation · <span class="zh">模拟用户</span></h2>
      <p class="research-pillar-tagline">Simulate users to locate poor experiences — before real users encounter them.</p>
      <p class="research-pillar-tagline-zh zh">模拟用户，定位不良体验。</p>
    </div>
  </div>

  <div class="research-dir-grid">
    <div class="research-dir-card">
      <div class="research-dir-label">DIRECTION 1A</div>
      <h3 class="research-dir-title">Long-Process Cognitive Experience</h3>
      <div class="research-dir-title-zh zh">模拟长流程认知体验</div>
      <p class="research-dir-desc">Simulate how users observe, comprehend, and operate intelligent applications across full interaction flows. Decompose user personas, model interface semantics, and use Chain-of-Thought reasoning to trace the cognitive journey — recording usability issues along the way.</p>
      <p class="research-dir-desc-zh zh">模拟用户如何观察和使用智能应用。拆解用户使用偏好，描述与认知相关的应用特征，用思维链模拟使用过程，记录体验问题。</p>
      <div class="research-dir-works">
        <div class="research-dir-work">
          <span class="research-dir-work-venue">CHI 2024</span>
          <span class="research-dir-work-title">SimUser: Generating usability feedback by simulating various users</span>
        </div>
      </div>
    </div>

    <div class="research-dir-card">
      <div class="research-dir-label">DIRECTION 1B</div>
      <h3 class="research-dir-title">Fine-Grained Cognitive Experience</h3>
      <div class="research-dir-title-zh zh">模拟细粒度认知体验</div>
      <p class="research-dir-desc">Estimate how individual design features — icon size, contrast, complexity — affect cognitive load under specific contexts. Integrate empirical human-factors data with LLM reasoning to compare cognitive load across design alternatives, even for unseen designs.</p>
      <p class="research-dir-desc-zh zh">分析任务中设计细节对认知负荷的影响。整合现有数据，推理新设计在各类场景任务中的认知负荷，实现设计方案间的认知负荷对比。</p>
      <div class="research-dir-works">
        <div class="research-dir-work">
          <span class="research-dir-work-venue">Under review</span>
          <span class="research-dir-work-title">SimEVA: Fine-grained cognitive load estimation for interface design</span>
        </div>
      </div>
    </div>

    <div class="research-dir-card">
      <div class="research-dir-label">DIRECTION 1C</div>
      <h3 class="research-dir-title">Physical Operation Experience</h3>
      <div class="research-dir-title-zh zh">模拟物理操作体验</div>
      <p class="research-dir-desc">Analyze physical operation differences across expertise levels to locate injury risk and cognitive overload. Compare expert vs. novice operation patterns on the same task and product to identify opportunities for reducing operational burden.</p>
      <p class="research-dir-desc-zh zh">分析产品操作差异，定位损伤风险。对比专家新手操作差异，优化负荷。</p>
      <div class="research-dir-works">
        <div class="research-dir-work">
          <span class="research-dir-work-venue">Ongoing</span>
          <span class="research-dir-work-title">Operation load modeling for complex equipment</span>
        </div>
      </div>
    </div>
  </div>
</div>

<hr class="divider" style="margin: 48px 0;">

<!-- ===== Pillar 2 ===== -->
<div class="research-pillar">
  <div class="research-pillar-header">
    <div class="research-pillar-number">02</div>
    <div>
      <h2 class="research-pillar-title">User Augmentation · <span class="zh">增强用户</span></h2>
      <p class="research-pillar-tagline">System-level augmentation that enhances user performance in real time.</p>
      <p class="research-pillar-tagline-zh zh">系统外挂，增强用户表现。</p>
    </div>
  </div>

  <div class="research-dir-grid">
    <div class="research-dir-card">
      <div class="research-dir-label">DIRECTION 2A</div>
      <h3 class="research-dir-title">Perception in Complex Scenarios</h3>
      <div class="research-dir-title-zh zh">复杂场景的感知表现</div>
      <p class="research-dir-desc">Identify potential risks that drivers might miss and guide their attention allocation in real time. Use LLMs to reason about sparse roadside risks and adaptively steer driver attention through HUD-based visual cues.</p>
      <p class="research-dir-desc-zh zh">识别路旁潜在风险，引导用户注意力分配。在复杂场景中，警示存在潜在风险的对象，自适应驾驶员注意力进行引导。</p>
      <div class="research-dir-works">
        <div class="research-dir-work">
          <span class="research-dir-work-venue">T-ITS 2025</span>
          <span class="research-dir-work-title">Visionary Co-Driver: Enhancing driver perception of potential risks</span>
        </div>
      </div>
    </div>

    <div class="research-dir-card">
      <div class="research-dir-label">DIRECTION 2B</div>
      <h3 class="research-dir-title">Guidance for Complex Tasks</h3>
      <div class="research-dir-title-zh zh">复杂任务的操作表现</div>
      <p class="research-dir-desc">Guide users through intricate operational procedures in high-stakes environments — flight training, emergency medical services. LLMs learn operation flows from domain manuals, then combine with EMS wearables to deliver real-time procedural reminders and hand-movement guidance.</p>
      <p class="research-dir-desc-zh zh">飞行训练中提醒操作流程，引导手部动作。从飞行手册、机型介绍、任务手册中学习操作流程，结合 EMS 辅助提醒与引导。</p>
      <div class="research-dir-works">
        <div class="research-dir-work">
          <span class="research-dir-work-venue">IJCAI 2025</span>
          <span class="research-dir-work-title">Hand by Hand: LLM driving EMS assistant for operational skill learning</span>
        </div>
      </div>
    </div>

    <div class="research-dir-card">
      <div class="research-dir-label">DIRECTION 2C</div>
      <h3 class="research-dir-title">State Management in Long Tasks</h3>
      <div class="research-dir-title-zh zh">长时任务的状态管理</div>
      <p class="research-dir-desc">Monitor user states across extended sessions and intervene proactively — from detecting driver distraction and deploying persuasion-based social support, to tracking emotional cues in elderly care and triggering personalized communication strategies.</p>
      <p class="research-dir-desc-zh zh">监测长时间任务中的用户状态，进行干预与支持。监测非驾驶行为引入社会支持策略进行干预；监测老人异常表现，引入专业护理策略。</p>
      <div class="research-dir-works">
        <div class="research-dir-work">
          <span class="research-dir-work-venue">IJHCS 2025</span>
          <span class="research-dir-work-title">Pika: A social-support agent for gig-economy drivers</span>
        </div>
        <div class="research-dir-work">
          <span class="research-dir-work-venue">SMC 2025</span>
          <span class="research-dir-work-title">CareEmo: Supporting caregivers with personalized communication</span>
        </div>
      </div>
    </div>
  </div>
</div>

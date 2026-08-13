Game Publishing Intelligence Skill

Turn game-industry signals into evidence-bounded publishing decisions.

面向海外发行、市场中台、营销、PR、本地化及相关协同团队的事件驱动游戏发行与营销情报 Skill。

它不是新闻摘要器，也不是固定周期的“行业周报生成器”。

它的核心任务是把公开市场信号转化为：

Event → Evidence → Business Problem → Mechanism → Decision → Monitoring

Why this exists

传统游戏行业周报常见几个问题：

信息很多，但不知道什么真正值得发行关注；

容易把播放、互动、热度误写成真实业务效果；

单个平台或少量评论被外推成整体玩家态度；

产品、平台、地区和生命周期信息没有被放进同一条事件链；

报告只回答“发生了什么”，没有回答“对发行意味着什么”；

同一事件反复出现，但没有说明“这次新增了什么”。

这个 Skill 的目标不是让 AI 搜更多新闻，而是让 AI：

先找对事情，再把事实找全，再做业务判断，最后才生成报告。

What it does

这个 Skill 可以用于：

扫描最近 7 / 14 / 30 天值得发行关注的游戏行业事件；

深拆某款游戏的 Demo、Beta、Early Access、预购、大版本、Campaign 或舆情；

分析某个国家 / 地区 / 平台的发行变化；

还原产品从首次公开到发售、更新、回应的完整事件链；

区分事实、玩家公开表达、机制分析、结果信号与待验证假设；

识别案例适用条件、失败条件和不可照搬部分；

输出下一监测节点，以及“什么新证据会改变当前结论”；

生成 P0 即时快讯或单文件可视化 HTML 报告；

将关键节点同步到可视化 Calendar。

How it works

User Request
    ↓
Discovery
    ↓
Normalize / Dedup
    ↓
Evidence Enrichment
    ↓
Evidence & Value Routing
    ↓
Module Analysis
    ↓
Business Analysis
    ↓
Calendar Update
    ↓
Final QA
    ↓
HTML Report

默认执行模式：

full_pipeline

只有用户明确要求“先只看候选 / 只做 Discovery / 只给 Research Brief / 不要 HTML / 只做 QA”时，才允许中途停止。

What makes it different

1. Event-first, not feed-first

分析单位是 Event（事件），不是单条帖子、视频或新闻。

同一事件的官方公告、商店变化、媒体报道、玩家讨论、公开数据和后续回应，会尽量被还原到同一条事件链中。

2. Evidence-bounded reasoning

Skill 强制区分：

已确认事实

玩家公开表达

报告机制分析

实际结果信号

待验证行为假设

核心约束：

规则存在 ≠ 效果发生
播放量高 ≠ 发行成功
玩家公开表达 ≠ 玩家真实心理
结果同时出现 ≠ 单一动作可归因
单一平台声音 ≠ 全球玩家态度

3. Product coordinates before analysis

重点案例必须先建立产品坐标，包括产品 / IP、开发商 / 发行商、品类、商业模式、生命周期、市场、平台、目标用户、业务目标和公开数据可得性。

无法确认时显式标记：

confirmed
partially_confirmed
inferred
unknown
not_applicable

4. Full release path

重点案例会按适用性回溯：

首次公开
→ 商店页 / Wishlist
→ 媒体 / 线下试玩
→ 测试
→ Demo
→ Early Access
→ 预购
→ 正式发售
→ 首轮数据
→ 里程碑
→ 后续更新 / 回应

5. Business reasoning, not summary

正式案例需要回答：

为什么现在需要看？

具体改变了什么？

解决的是哪个业务问题？

核心机制是什么？

Expected Impact Chain 是什么？

为什么可能有效 / 失败？

适用条件是什么？

哪些结果不能归因？

最值得验证什么？

什么新证据会改变当前结论？

Output types

P0 即时情报快讯

用于重大政策 / 平台规则、突发产品节点、重大舆情 / 风险、Convention 重大官宣、跨平台危机。

固定标记：

P0 初步快讯｜事件仍在发展，后续将在动态情报报告中更新完整信息。

Dynamic Intelligence Report

单一 HTML，可包含：

首页 3–5 条发行优先结论

重点案例深拆

短事件卡

专项舆情 / 政策 / Convention 深度

Radar

持续监测

Calendar

来源与运行记录

3–5 个案例只是常规触发参考，不是硬门槛。至少 1 个正式事件通过价值与证据闸门即可生成动态 HTML。

Visualization-first reporting

V0.1.2 的默认视觉层级：

结论 > 机制 > 关键数据 > 证据

优先使用：

Timeline：发行路径、危机扩散、Campaign 节奏

Flow / Arrow Chain：机制、漏斗、生命周期迁移

Before / After：版本、玩法、规则变化

Asset Matrix：PV、OOH、UGC、KOL、商店资产

Regional × Platform Matrix：市场与平台差异

Key Metrics：最多 3 个最重要数字

Insight Cards：Judgement / WHY / SO WHAT

Large Calendar：关键日期、时间范围、优先级和确认状态

Calendar V2

Calendar 采用一个全宽大日历：

🔴 P0 / 战略级

🟠 重点

🔵 关注

⚪ 监测

虚线：预计 / 未确认

不再使用“小日历 + 下方重复日期表”。

Golden Examples

PRAGMATA

Pattern：Demo as Product Education

当用户已有兴趣但仍难通过 PV 理解复合玩法时，Demo 可承担产品教育和购买前验证。

同时必须保留：

销量结果不能直接归因于 Demo。

Modern Warfare 4

Pattern：Cross-title Lifecycle Migration

预购锁定
→ 旧作即时奖励
→ 旧作回流
→ 跨游戏任务
→ 跨作资产
→ 新作迁移

必须区分：

模式迁移 ≠ 整体 DAU 增长

Crimson Desert

Pattern：Risk Closure

Asset Closure
+
Process Closure
+
Trust Closure
=
Incident Closure

必须区分：

补丁上线 ≠ 风险事件已经关闭

Evidence rules

当前证据状态：

clear_signal
limited_signal
to_verify
not_applicable

普通重点事件：官方 / 数据 / 玩家或媒体三类证据至少满足两类。

重大舆情 / 反面案例：三类必须齐全。

政策 / 平台规则：必须提供政府、监管或平台官方原文。

Quality Gate

任何重点案例缺少以下五项之一，直接 FAIL：

产品坐标

地区与平台

完整链路

案例专属机制

证据边界

同时检查：

是否把相关性写成因果

是否把规则写成效果

是否把单平台反馈外推为全球

是否混淆 Demo / Beta / Early Access

是否把上架平台误写成商业合作

是否重复旧事件

是否存在无依据“行业领先 / 显著提升”

是否有下一监测节点

是否存在真正有信息增量的可视化

Quick Start

行业扫描

使用 Game Publishing Intelligence Skill。

扫描最近 7 天全球游戏行业，
寻找真正值得海外发行市场中台关注的事件。

默认使用 full_pipeline。
不因为播放量高就收录。
不凑案例。
对证据不足的事件只标记待验证。

最终通过 QA 后生成单文件 HTML。

市场扫描

扫描最近 30 天韩国游戏市场。

重点关注：
- 产品重大节点
- Campaign
- 玩家公开反馈
- 发行风险

不要把英语社区外推为韩国玩家态度。

单案例

深拆某款游戏最近一次 Demo / Beta / 预购 / 大版本动作。

先建立 Product Profile，
再还原完整发行链，
最后分析 Business Problem、Mechanism、适用条件、
失败条件与最关键缺失证据。

Repository structure

.
├── SKILL.md
├── README.md
├── QUICK_START.md
├── CHANGELOG.md
├── VISUAL_DESIGN_RULES.md
├── config/
├── prompts/
├── schemas/
├── examples/
├── templates/
├── tests/
├── state/
└── outputs/

Platform

当前设计为平台无关的 Agent-ready workflow package。

优先适配：

Codex

WorkBuddy

也可以继续封装到支持 Web Search、MCP、Connector、Workflow 或 Agent 的平台。

当前版本属于主动调用型 Beta，不代表已经完成后台定时扫描、数据库服务或完整工程化部署。

Current version

V0.1.2 Beta

已完成：

Event-first workflow

Full pipeline orchestration

Cross-run dedup logic

Evidence rules

Product profile

Business analysis framework

Golden Examples

Final QA

Single-file HTML reporting

Calendar V2

Visualization-first rules

Roadmap

V0.2

Evidence Model V2：Fact / Mechanism / Outcome / Attribution 分层

Case Library

Pattern Library

新案例 Beta 测试

更严格的 taxonomy / schema

自动运行记录与历史对比

Later

Scheduled monitoring

Automated P0 alerts

Multi-market source adapters

Persistent case database

Team collaboration workflow

Design principles

先让 AI 找对事情，再把事实找全，再做业务判断，最后才生成漂亮报告。

规则存在，不等于效果发生。

如果 SO WHAT 只能写“加强 / 提升 / 重视 / 优化”，就重写或删除。

好的情报不是“我分析完了”，而是“什么新证据会让我改变判断”。

Status

This project is currently in V0.1.2 Beta.

It is an Agent-ready workflow / Skill specification, not yet a fully engineered automated intelligence platform.

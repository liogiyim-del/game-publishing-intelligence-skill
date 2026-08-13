# 动态游戏发行与营销情报 Skill — V0.1.2

## 这是什么？

这是一个面向海外发行、市场中台、内容营销、社媒、PR、本地化及相关协同团队的**事件驱动游戏行业情报 Skill**。

它不按“帖子/视频”写新闻摘要，而是把多个公开来源整理为一个完整事件，再回答：

- 发生了什么？
- 为什么现在值得看？
- 对发行哪一环有影响？
- 证据支持到哪一步？
- 哪些是事实、哪些是分析、哪些还需要验证？
- 下一步最值得监测什么？

## V0.1.2的使用方式

V0.1.2 先采用**用户主动调用**。

直接输入类似：

> 扫描最近 7 天全球游戏行业，找出最值得海外发行关注的事件。

或：

> 深拆某款游戏最近的 Demo / 预购 / 大版本 / Campaign / 舆情。

或：

> 看最近 30 天韩国市场有哪些值得关注的游戏发行与营销动作。

Skill 会按以下流程工作：

`任务解析 → 产品坐标 → 完整事件链 → 定向研究 → 证据补全 → 事件价值判断 → 模块分析 → QA → HTML`

## 正式输出

只有两类：

1. **P0 即时情报快讯**
2. **动态游戏发行与营销情报报告（单一 HTML）**

综合报告中可以包含：
- 首屏 3–5 条结论
- 重点案例
- 专项深度复盘
- 短事件
- 持续监测
- Calendar
- 来源与运行记录

## 最重要的约束

Skill 不允许：
- 用播放量推断收入或回流
- 把活动规则写成活动效果
- 把单平台评论写成全球玩家态度
- 把相关性写成因果
- 为凑数量塞低价值新闻
- 无来源时编造数字、图片、政策或玩家观点

## 平台

V0.1.2 设计为平台无关，优先适配：
- Codex
- WorkBuddy

后续可继续封装到支持 MCP、Connector、Web Search 或 Workflow 的平台。

## 目录

- `SKILL.md`：Skill 总规则
- `config/`：触发、证据、来源、模块等配置
- `schemas/`：事件与证据结构
- `prompts/`：后续模块 Prompt
- `templates/`：P0 与动态报告模板
- `examples/`：Golden Examples
- `state/`：事件档案与运行状态
- `tests/`：UAT / QA
- `outputs/`：实际生成结果

## 当前版本

V0.1.2
- 主动调用
- 不要求后台自动定时扫描
- 当前 `dynamic_report.html` 作为 Golden Template
- Golden Examples：PRAGMATA / Modern Warfare 4 / Crimson Desert

## V0.1 推荐执行入口

在 Codex / WorkBuddy 中，优先从 `SKILL.md` 开始加载规则，然后按需调用：

1. `prompts/discovery.md`
2. `prompts/normalize_dedup.md`
3. `prompts/evidence_enrichment.md`
4. 对应专项 Prompt
5. `prompts/business_analysis.md`
6. `prompts/calendar_update.md`
7. `prompts/final_qa.md`
8. `prompts/report_compose.md`

Golden Examples 位于 `examples/`，用于约束分析风格和证据边界。


## V0.1.2 默认运行方式

默认执行模式为 `full_pipeline`。

当用户说“扫描最近7天”“跑一下Skill”“生成一期情报”等任务时，默认一路执行到**实际生成 HTML 文件**，不再停在 Markdown 摘要。

只有用户明确说“先只看候选 / 不要生成报告 / 只做 Discovery / 只给 Research Brief”时，才允许中途停止。

3–5 个案例只是常规触发参考，不是硬门槛。至少 1 个正式事件通过价值与证据闸门即可生成动态 HTML。


## V0.1.2 视觉与 Calendar 更新

这一版把 Calendar 和报告可读性作为正式 Skill 规则：

- Calendar 改为一个全宽大日历；
- 所有关键节点直接标在日期格；
- P0 / 重点 / 关注 / 监测使用稳定视觉层级；
- 预计/未确认节点使用虚线状态；
- 删除 Calendar 下方重复日期表；
- 跨月节点使用未来30–90天轻量节点带；
- 重点案例优先用 Timeline、Flow、Before/After、Asset Matrix、地区×平台矩阵表达；
- 默认视觉顺序：结论 → 机制 → 数据 → 证据。


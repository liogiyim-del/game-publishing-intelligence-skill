# QUICK START｜V0.1.2 第一次运行

请读取当前目录中的 `SKILL.md`，并按 V0.1.2 Orchestrator 规则运行。

任务：扫描最近 7 天全球游戏行业，寻找真正值得海外发行市场中台关注的事件。

要求：
1. 默认使用 `full_pipeline`。
2. 除非没有任何正式事件达到准入门槛，否则不要停在 Markdown 摘要。
3. 完整执行：
   Discovery → Normalize/Dedup → Evidence Enrichment → Module Analysis → Business Analysis → Calendar Update → Final QA → Report Compose。
4. 最终实际生成 `dynamic_intelligence_<report_id>_single_file.html`。
5. 不要只输出 HTML 代码或 Markdown 报告。
6. 不凑案例；3–5 个不是硬门槛。


## V0.1.2 视觉要求
最终 HTML 必须：
- 使用一个全宽大 Calendar；
- 将所有明确日期直接标入日历；
- 通过颜色/虚线表达优先级与确定度；
- 不再输出 Calendar 下方重复日期表；
- 每个重点案例至少包含一个真正有信息增量的可视化结构。

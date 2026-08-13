# Orchestrator｜V0.1.1 主动调用总控

## 默认行为
除非用户明确要求阶段性结果，否则：`execution_mode = full_pipeline`

## full_pipeline
1. discovery.md
2. normalize_dedup.md
3. evidence_enrichment.md
4. 按事件调用专项 Prompt
5. business_analysis.md
6. calendar_update.md
7. final_qa.md
8. report_compose.md
9. 实际写出 `.html`
10. 返回文件路径/下载入口

## 允许提前停止
仅当用户明确要求“只看候选 / 只做 Discovery / 只要 Research Brief / 不要 HTML / 只做 QA”等阶段性结果时才可停止。

## 强制规则
- Markdown 版“发行优先结论”、候选列表、Routing 摘要、Research Brief 都只是中间结果。
- `full_pipeline` 不得在这些阶段结束。
- 3–5 个案例不是硬门槛。
- 至少 1 个正式事件通过业务价值闸门即可生成动态 HTML。
- 短事件卡、Radar、持续监测和 Calendar 均可成为正式报告组成部分。
- 无正式事件时不凑内容，生成 Run Log 并说明“不出刊”。

## 路由后处理
- 重点深拆：继续证据补全、专项分析、Business Analysis、QA、Report。
- 短事件卡：保持短卡，不强行升级；仍进入 Report Compose。
- Radar Candidate：进入 Radar / 持续监测，不写成确认事件。
- Calendar-only：没有本期新增时只进 Calendar，不重复包装成新闻。

## 完成检查
- [ ] 去重完成
- [ ] 正式事件 / 短卡 / Radar / Calendar-only 已区分
- [ ] Evidence Enrichment 已完成
- [ ] 适用模块已运行
- [ ] Business Analysis 已运行
- [ ] Calendar / 持续监测已更新
- [ ] Final QA 已运行
- [ ] Report Compose 已运行
- [ ] HTML 文件已实际生成
- [ ] 最终回复提供文件

缺任一项，不得宣告 `full_pipeline` 完成。

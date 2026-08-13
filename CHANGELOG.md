# CHANGELOG

## V0.1.1

### Bug Fix 001｜主动调用提前结束
- 默认 `execution_mode = full_pipeline`
- 新增 `prompts/orchestrator.md`
- 新增 `config/execution_modes.yaml`
- 强制完整链路最终实际写出 HTML
- 只有用户明确要求阶段性结果时允许提前停止

### Bug Fix 002｜误把 3–5 个案例当成报告硬门槛
- 3–5 个仅为常规触发参考
- 至少 1 个正式事件即可生成 HTML
- 短事件卡 / Radar / 持续监测 / Calendar 都属于正式报告组成部分
- 无正式事件时不出刊并生成 Run Log

### 保持不变
- Golden Template
- Calendar 核心结构与交互
- 三个 Golden Examples
- Evidence Rules
- Case Granularity QA


## V0.1.2

### Calendar V2
- Calendar 改为单一全宽大日历
- 所有明确日期直接落在日期格
- 同日多事件允许堆叠
- 红/橙/蓝/灰编码 P0 / 重点 / 关注 / 监测
- 虚线表达预计 / 未确认
- 删除 Calendar 下方重复日期表
- 跨月节点改为未来30–90天轻量节点带

### Visualization First
- 新增 `config/visual_rules.yaml`
- 重点案例优先使用 Timeline / Flow / Before-After / Asset Matrix / Regional×Platform Matrix
- 强制视觉层级：结论 > 机制 > 关键数据 > 证据
- Final QA 新增视觉可读性闸门

### 保持不变
- V0.1.1 full_pipeline 默认完整执行
- Golden Examples
- Evidence Rules
- Case Granularity QA


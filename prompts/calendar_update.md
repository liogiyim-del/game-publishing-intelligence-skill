# Calendar Update｜Calendar 节点更新

输入结构化事件后，判断是否写入 Calendar。

规则：
- 明确日期：写入对应日期
- 明确日期范围：写入范围
- 仅预计时间范围：标“预计”，使用待确认视觉状态
- 完全无日期：不写 Calendar，进入持续监测

字段至少：
node_id / event_id / date_start / date_end / date_precision / market / type / status / p0_condition / source_url / last_verified

必须保持：
- 事件与 Calendar 双向锚点
- 已确认 / 高可信 / 待人工确认 / 动态通知状态分离
- P0/P1 是报告运营评级，不是假装法律或行业官方分级
- 不改变 Golden Template 的 Calendar 核心交互逻辑

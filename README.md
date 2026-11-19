# 城区空气监测资料

本地合成业务资料，不含真实站点或污染观测。仓库提供参考设备及校准记录、固定站时序、风场背景、共址比对、备案指标、日报和巡查路线记录。

`data/supplies.json` 按业务表保存记录，`data/fields.json` 记录各表字段及资料中出现的值类型。`references` 表示参考设备依赖关系；`certificates` 按适用时段和接收时刻记录校准证据及撤销。`observations` 区分采样与接收时间、计划/备案补位和有效/停机/低于检出状态。`wind` 与 `transport` 描述背景及区域连通资料，`collocations` 保存共址比较。`plans` 是日报覆盖及独立证据要求，`bulletins` 保存已发布日报；`routes`、`dispatch` 和 `route_receipts` 记录巡查安排与回执。

使用 Linux、Python 3.11 及标准库运行 `python3 -m unittest discover -s tests -v`，检查数据字段、类型和关键关联。资料仓库不包含判读或派车入口。

# Output template

## 容量审核

- 原时间段：
- 可用时长：
- 台词估时：
- 动作与反应估时：
- 判断：fits / tight / overloaded
- 拆分：

## 剧情功能

- 表层事件：
- 隐藏冲突：
- 情绪推进：
- 本场结尾状态：

## 角色与声音

For each character: identity, appearance, wardrobe, position, objective, subtext, voice identity, delivery state, micro-expression, mouth-state, and continuity locks.

## 场景与连续性

Specify geography, time, physical light sources, color, materials, props, ambience, eyelines, 180-degree line, entrances, exits, and immutable layout details.

## 片段地图

| 片段 | 原时间线 | 生成时长 | 叙事任务 | 首帧状态 | 尾帧状态 |
|---|---:|---:|---|---|---|

## 片段提示词

For every clip:

### 分镜时间轴

| 镜头 | 本地时间 | 景别/机位/焦段 | 画面与表演 | 对白/口型 | 转场 |
|---|---:|---|---|---|---|

### Seedance 2.0导演版

Write natural Chinese prose with exact local time ranges and explicit hard-cut timestamps. Bind each line to one speaker and state who must not move their mouth.

### LibTV精简版

Retain subject, action, cut points, camera, voice, sound, preservation constraints, and ending state. Remove duplicated adjectives.

### 节点命名

Use stable names such as `05A-01_偏殿建立大全景`, `05A-02_赵渊审问`, and `05A-03_赵景珩反应`.

## 修改说明

| 类别 | 原设计 | 修改后 | 原因 | 制作影响 | 剧情影响 |
|---|---|---|---|---|---|

## 连续生成交接

State which generated clip or actual final frame must be returned before the next continuation prompt becomes final.


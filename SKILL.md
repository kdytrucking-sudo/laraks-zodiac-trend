---
name: laraks-zodiac-trend
description: 从 Reddit 和 X 平台抓取并分析中国生肖相关的实时热点话题。输出标准化双平台情报简报。
---

# Laraks Zodiac Trend 🐍🐎

此技能专门用于实时监测社交媒体上关于“中国生肖”和“农历运势”的讨论热点，并以固定格式输出分析简报。

## 核心流程

### 1. 跨平台情报抓取
- **Reddit**: 
  - 目标板块：`r/ChineseZodiac`, `r/ChineseAstrology`, `r/astrology`, `r/FengShui`。
  - 搜索关键词：`Chinese Zodiac`, `Year of the Snake`, `2025 Predictions`, `Zodiac compatibility`。
  - 工具：优先使用 `reddit-thread-analyzer` 技能，或通过 `web_fetch` 抓取 Google/Bing 索引的最新 Reddit 帖。
- **X (Twitter)**:
  - 目标搜索：`"Chinese Zodiac 2025"`, `"Year of the Snake"`, `#ChineseZodiac`。
  - 工具：使用 `bird search` 获取最新、高互动的推文。

### 2. 标准化格式输出
 Agent **必须** 严格遵守以下输出模版：

---
#### 1. Reddit
- **话题 1**：[标题]
  - [讨论内容深度摘要，包含社区主流情绪]
- **话题 2**：[标题]
  - [摘要...]
- **话题 3**：[标题]
  - [摘要...]

* **综合分析**：[对以上 Reddit 热点内容的整体趋势、人群画像及核心博弈点的分析]
* **内容 Source**：[提供 2-3 个核心帖子的链接]

#### 2. X (Twitter)
- **话题 1**：[简短标题]
  - [实时讨论摘要，包含大V观点或爆火迷因]
- **话题 2**：[标题]
  - [摘要...]
- **话题 3**：[标题]
  - [摘要...]

* **综合分析**：[对以上 X 热点内容的整体节奏、金融/社媒影响力分析]
* **内容 Source**：[提供 2-3 个核心推文的链接或作者 ID]
---

## 使用建议
- 报告应保持客观与趣味性并存。
- 对于涉及“本命年”或“相冲”的生肖话题，应重点标注应对建议（如果有社区讨论）。

## 使用示例
"Laraks，帮我跑一下 Zodiac Trend，看看现在大家都在聊什么。"
"分析 Reddit 和 X 上关于 2025 蛇年的最新话题。"

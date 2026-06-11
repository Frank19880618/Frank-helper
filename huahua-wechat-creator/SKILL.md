---
name: huahua-wechat-creator
description: "Use when the user wants to turn a URL, notes, transcript, or draft into a Chinese WeChat article in the gentle women-growth essay style of 自我引力: 温柔治愈公众号, 女性成长随笔, 按自我引力风格写公众号, 根据网址生成这种排版的公众号文章, with Markdown, WeChat-compatible HTML, cover prompts, inline image prompts, and optional draft publishing."
---

# 花花公众号创作工作流

## 核心定位

把输入素材改写成“温柔女性成长随笔号”的公众号成品。默认参考 `references/style-guide.md`，保持自我滋养、女性成长、温柔治愈、散文式表达和 `Vol.1` 分节排版。

不要使用教程号、小白保姆级、工具测评、步骤截图文的语气。不要复用 Cherry Studio 教程文风格。

## 工作流

### Step 1: 获取素材

根据输入选择已有技能：

| 输入 | 使用技能 |
| --- | --- |
| 网页或公众号链接 | `baoyu-url-to-markdown` |
| YouTube 链接 | `baoyu-youtube-transcript` |
| 外文内容 | `baoyu-translate` |
| 已有 Markdown/文本 | 直接进入 Step 2 |
| 微信群聊内容 | 可选 `baoyu-wechat-summary` |

抓取后先识别素材里的核心情绪、人物处境、成长主题和可引用金句，再改写正文。来源链接只保留在素材文件、frontmatter 或交付说明里，除非用户明确要求放进正文。

### Step 2: 写成花花风格正文

使用 `baoyu-format-markdown` 整理结构，但按花花风格重写：

- 标题采用“权威来源/金句 + 引号主题句 + 女性成长核心词”的结构。
- 开头用亲切问候、自我介绍、名言引入和个人体悟进入主题。
- 正文用 `Vol.1`、`Vol.2`、`Vol.3`、`Vol.4` 分节，每节只承载一个成长主题。
- 语言温柔、抒情、治愈，像随心录，不写成教程、清单或说明书。
- 多用手机阅读友好的短段落，段落之间留空行。
- 关键句可加粗，但不要把每段都加粗。
- 不裸露外链；必须展示 URL 时，先用一句话说明，再放入 `text` 代码块。

写作时必须打开并遵守 `references/style-guide.md`。风格说明只用于生成，不写进正文。

### Step 3: 生成公众号 HTML

使用 `baoyu-markdown-to-html` 转成公众号可复制 HTML。

默认优先：

- `theme: modern`
- `color: rose` 或最接近的温柔暖色主题；如果工具不支持 rose，则用 `green` 并在交付说明里说明。
- `font-size: 16px`
- 不在正文开头或结尾添加“来源”“出处”“原始整理来源”等说明。

### Step 4: 生成图片提示词

图片统一使用 Codex 内部 Image Gen；不要默认调用外部图片 API。

默认交付 2 类提示词：

- 公众号封面图：温柔女性成长美学，适合 2.35:1 或 16:9 横版封面。
- 正文插图：放在开头后或 `Vol.1` 前，承接情绪，不做教程截图。

每次生成图片前，先展示或保存完整提示词，方便用户复用和换风格。

### Step 5: 发布或存草稿

如果用户明确要发布或保存草稿，使用 `baoyu-post-to-wechat`。

不要把公众号 `app_secret`、token 或登录态写进代码仓库。

## 默认交付

完成后给用户：

- Markdown 源文
- 公众号 HTML 文件路径
- 封面图提示词
- 正文插图提示词
- 如已发布，说明草稿箱位置或发布结果


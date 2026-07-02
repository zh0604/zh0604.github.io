---
title: "Hugo PaperMod 主题完全配置指南"
date: 2026-07-01T20:00:00+08:00
draft: false
tags: ["Hugo", "PaperMod", "教程"]
categories: ["教程"]
description: "详解 PaperMod 主题的所有配置选项，从 profileMode 到 SEO 设置。"
---

## PaperMod 主题简介

[PaperMod](https://github.com/adityatelange/hugo-PaperMod) 是目前 Hugo 生态中最受欢迎的博客主题之一（13k+ Stars），以其**极快的加载速度**和**丰富的功能**著称。

## 核心特性

```yaml
# 主题三大模式
- Regular Mode     # 标准博客列表模式
- Home-Info Mode   # 首页显示信息卡片
- Profile Mode     # 首页显示个人资料（本文使用）
```

## 配置文件详解

### 基础配置

```yaml
params:
  defaultTheme: auto     # 跟随系统暗黑/亮色模式
  ShowReadingTime: true  # 显示阅读时间
  ShowWordCount: true    # 显示字数统计
  ShowToc: true          # 显示文章目录
  TocOpen: true          # 目录默认展开
```

### 首页配置

使用 `profileMode` 可以在首页展示个人资料卡片：

```yaml
profileMode:
  enabled: true
  title: "你好，我是 xxx"
  subtitle: "这是我的个人博客"
  buttons:
    - name: "📝 文章"
      url: "posts"
    - name: "🏷️ 标签"
      url: "tags"
```

### 搜索功能

PaperMod 内置了基于 [Fuse.js](https://fusejs.io/) 的客户端搜索：

```yaml
fuseOpts:
  threshold: 0.4       # 搜索阈值（越低越精确）
  keys:
    - "title"
    - "content"
    - "summary"
```

然后创建 `content/search.md` 即可启用搜索页面。

## 自定义样式

在 `assets/css/extended/custom.css` 中添加自定义 CSS，这些样式会在 PaperMod 之后加载，可以覆盖主题默认样式。

```css
/* 示例：修改链接颜色 */
.post-content a {
  color: #ff6b4a;
}

/* 示例：修改代码块样式 */
.post-content pre {
  border-radius: 12px;
  padding: 1.5rem;
}
```

## 多语言支持

PaperMod 内置了完整的多语言支持。在 `hugo.yaml` 中设置：

```yaml
languageCode: "zh-CN"
hasCJKLanguage: true
```

PaperMod 的 i18n 文件位于 `themes/PaperMod/i18n/`，已包含中文翻译。

## 进阶技巧

### 文章封面图

```markdown
---
cover:
  image: "featured.png"
  alt: "封面图描述"
  caption: "封面图说明文字"
---
```

### 文章系列

```yaml
series: ["Hugo教程"]
```

### 自定义页脚

创建 `layouts/partials/extend_footer.html`，写入自定义 HTML 即可追加到页脚。

---

PaperMod 的完整文档见 [GitHub Wiki](https://github.com/adityatelange/hugo-PaperMod/wiki)，推荐深入阅读。 📖

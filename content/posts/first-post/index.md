---
title: "第一篇博客：搭建这个网站的心路历程"
date: 2026-07-02T09:00:00+08:00
draft: false
tags: ["博客", "Hugo", "PaperMod"]
categories: ["技术"]
series: []
description: "记录使用 Hugo + PaperMod + GitHub Pages 搭建个人博客的全过程。"
---

## 为什么要写博客？

在 2026 年，信息爆炸的时代，**拥有一个属于自己的数字空间**比以往任何时候都重要。

社交媒体和短视频平台虽然方便，但你的内容最终属于平台，而非自己。一个独立博客意味着：

- ✍️ **内容自主权** — 你的文字，你做主
- 🎨 **完全定制** — 从样式到功能，随心所欲
- 📚 **知识沉淀** — 好记性不如烂笔头
- 🌐 **个人品牌** — 展示专业能力的窗口

## 技术选型

经过一番调研，我选择了以下技术栈：

| 组件 | 选型 | 理由 |
|------|------|------|
| 静态站点生成器 | **Hugo** | 构建速度极快（毫秒级），Go 语言编写 |
| 主题 | **PaperMod** | 简洁、快速，支持暗黑模式、搜索、SEO |
| 托管 | **GitHub Pages** | 免费、稳定、自动部署 |
| 写作格式 | **Markdown** | 简洁优雅，专注内容 |

## 建站步骤

### 1. 安装 Hugo

```bash
# macOS
brew install hugo

# Windows (使用 Chocolatey)
choco install hugo-extended

# Linux
sudo snap install hugo
```

### 2. 创建站点

```bash
hugo new site myblog
cd myblog
git init
git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod
```

### 3. 编写第一篇文章

```bash
hugo new posts/first-post/index.md
```

### 4. 部署到 GitHub Pages

配置 GitHub Actions 工作流，每次推送自动构建和部署。

## 未来计划

- [ ] 添加评论系统（Giscus）
- [ ] 完善标签和分类体系
- [ ] 添加项目展示页面
- [ ] 优化图片懒加载
- [ ] 接入访问统计

---

> 种一棵树最好的时间是十年前，其次是现在。开始写博客吧！ 🌱

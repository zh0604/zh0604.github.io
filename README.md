# 🚀 我的博客

基于 **Hugo** + **PaperMod 主题** + **GitHub Pages** 的个人博客。

> 参考：[dejavu.moe 博客搭建教程](https://blog.dejavu.moe/posts/how-i-built-my-personal-blog/) · [hugo-PaperMod 主题](https://github.com/adityatelange/hugo-PaperMod)

## ✨ 特性

- ⚡ Hugo 构建，毫秒级生成速度
- 🎨 PaperMod 主题 — 自动暗黑/亮色模式
- 🔍 Fuse.js 客户端全文搜索
- 🏷️ 标签 / 分类 / 系列分类体系
- 📱 完全响应式设计
- 🤖 GitHub Actions 自动部署

## 📁 目录结构

```
├── .github/workflows/    # CI/CD 自动部署
├── archetypes/           # 文章模板
├── assets/css/extended/  # 自定义样式
├── content/              # 博客内容（Markdown）
│   ├── posts/            # 文章
│   ├── about.md          # 关于页面
│   └── search.md         # 搜索页面
├── layouts/partials/     # 布局覆写
├── static/               # 静态资源
├── hugo.yaml             # Hugo 配置文件
└── themes/PaperMod/      # 主题（Git 子模块）
```

## 🚀 快速开始

### 1. 安装 Hugo

```bash
# macOS
brew install hugo

# Windows
choco install hugo-extended

# Linux
sudo snap install hugo
```

### 2. 克隆并初始化

```bash
git clone --recursive https://github.com/yourusername/yourusername.github.io.git
cd yourusername.github.io
```

### 3. 修改配置

编辑 `hugo.yaml`，将 `yourusername` 替换为你的实际 GitHub 用户名。

### 4. 本地预览

```bash
hugo server -D
```

浏览器打开 `http://localhost:1313`。

### 5. 创建新文章

```bash
hugo new posts/my-article/index.md
```

## 📦 部署

推送代码到 `main` 分支，GitHub Actions 会自动构建并部署到 GitHub Pages。

**首次使用需要：**
1. 进入仓库 **Settings → Pages**
2. Source 选择 **GitHub Actions**

## 📝 自定义

| 文件 | 用途 |
|------|------|
| `hugo.yaml` | 主题配置、菜单、社交链接 |
| `assets/css/extended/custom.css` | 自定义 CSS |
| `layouts/partials/extend_head.html` | 自定义 `<head>` |
| `layouts/partials/extend_footer.html` | 自定义页脚 |
| `content/about.md` | 关于页面内容 |

## 📄 许可证

MIT

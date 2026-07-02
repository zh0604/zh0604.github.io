# 🚀 我的博客

Hugo + PaperMod + GitHub Pages（docs/ 模式，无需 GitHub Actions）

## 🚀 部署（3 步）

```bash
git add .
git commit -m "init"
git push
```

然后去 GitHub 仓库 → **Settings → Pages**：
- Source 选 **Deploy from a branch**
- Branch 选 **main**，文件夹选 **/docs**
- 点 Save，等 30 秒

## 📝 写文章

```bash
hugo new posts/my-post/index.md
# 写完后构建：
hugo --minify
# docs/ 会自动更新，push 即可
```

## 🔧 本地预览

```bash
hugo server -D
# 打开 http://localhost:1313
```

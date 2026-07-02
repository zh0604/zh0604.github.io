# 🚀 我的博客

Hugo + PaperMod + GitHub Pages

## 🚀 部署（4 步）

```bash
# 1. 构建
hugo --minify

# 2. 把 public/ 里的文件复制到根目录
xcopy /E /I /Y public\* .

# 3. 推送
git add .
git commit -m "更新"
git push

# 4. GitHub → Settings → Pages
#    Source: Deploy from a branch → main → / (root)
```

## 📝 写新文章

```bash
hugo new posts/my-post/index.md
hugo --minify
xcopy /E /I /Y public\* .
git add . && git commit -m "新文章" && git push
```

## 💻 本地预览

```bash
hugo server -D
# 打开 http://localhost:1313
```

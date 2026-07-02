# 我的博客

Hugo + PaperMod + GitHub Pages

## 本地预览
```bash
hugo server -D
# http://localhost:1313
```

## 发布
```bash
hugo --minify    # 构建到 docs/
git add . && git commit -m "更新" && git push
```

GitHub → Settings → Pages → `/docs` 文件夹

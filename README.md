# 我的博客

Hugo + PaperMod + GitHub Pages

## 本地预览
```bash
hugo server -D
# http://localhost:1313
```

## 发布（每次更新执行这3条）
```bash
hugo --minify && xcopy /E /I /Y public\* . && rmdir /s /q public
git add -A && git commit -m "更新" && git push
```

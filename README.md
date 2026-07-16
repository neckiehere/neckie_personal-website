# Neckie Portfolio

个人求职作品集网站，适用于 GitHub Pages 静态托管。

## 文件说明

- `index.html`：网站主文件。页面图片、样式和脚本均已嵌入，可直接部署。
- `.nojekyll`：告诉 GitHub Pages 不使用 Jekyll 处理该静态网站。
- `GitHub_Pages_上传说明.md`：浏览器端上传和发布步骤。
- `发布前检查清单.txt`：公开发布前建议核对的内容。
- `自定义域名说明.txt`：购买域名后如何接入的简要说明。

## 本地预览

可以直接双击打开 `index.html`。为了更接近线上环境，也可以在本文件夹打开终端并运行：

```bash
python -m http.server 8000
```

然后在浏览器访问：

```text
http://localhost:8000
```

## 更新网站

修改完成后，用新的 `index.html` 替换仓库根目录中的旧文件并提交（Commit），GitHub Pages 会重新部署。

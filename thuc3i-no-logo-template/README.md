# THUC3I 论文模板：无实验室 logo 版

从所提供论文中提取的可编辑模板。保留 `thuc3i.cls`、Charter 字体、A4 单栏布局、
蓝色标题摘要框、页眉页脚、链接按钮、标题层级和参考文献样式。
正文是可替换的通用示例，包含图、表、公式、目录和附录。

首页左侧页眉留空，目录中不包含或依赖 `assets/logo_lab.png`。

## 编译

需要 TeX Live（含 XCharter、newtxmath、fontawesome5、tcolorbox、natbib 等宏包）、
`latexmk` 和 BibTeX。在此目录运行：

```bash
latexmk -interaction=nonstopmode -file-line-error main.tex
```

`.latexmkrc` 默认使用 pdfLaTeX，关闭 shell escape，输出至 `build/main.pdf`。
BibTeX、目录和交叉引用由 latexmk 自动处理。仓库目录中的 `preview.pdf` 是编译预览；
ZIP 仅打包模板源码和必要资源。

## 替换内容

1. 在 `main.tex` 修改完整标题、短标题、作者、机构和项目链接；两个示例链接均指向 `example.org`，应替换或删除。
2. 在 `sections/` 中替换摘要和各节内容，在 `main.bib` 中维护参考文献。
3. 在 `figures/` 中加入论文图片，并替换首页的图框和图注；目录页也可按需删除。
4. `branding.tex` 负责首页左侧页眉；后续页面使用 `main.tex` 中的短标题。
5. 首页日期由 class 生成；需要固定时，可在导言区加入 `\renewcommand{\today}{22 October 2026}`。

标题摘要框沿用所提供示例的样式；原例中固定的 `before skip=-800pt` 改为 `0pt`，
避免让后续内容依赖大幅负间距。摘要仍按 class 的要求在 `\begin{document}` 之前声明。
示例仅支持当前展示的 A4、11pt、单栏配置。

两个版本的主体源码与 class 相同，差异只在本说明、`branding.tex` 和实验室 logo 资源。
`.cls` 与 `.bst` 的来源和许可见 [NOTICE.md](NOTICE.md)。

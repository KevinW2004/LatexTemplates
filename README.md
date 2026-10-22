# LaTeX Templates

## THUC3I 论文模板

从提供的论文源码整理的通用模板，保留原始 class 与版式。两版均可独立编译，
提供可编辑源码、ZIP 和 PDF 预览。

| 版本 | 源码 | 下载 | 预览 |
| --- | --- | --- | --- |
| 标准版，含实验室 logo | [thuc3i-template](thuc3i-template/) | [ZIP](thuc3i-template.zip) | [PDF](thuc3i-template/preview.pdf) |
| 无实验室 logo 版 | [thuc3i-no-logo-template](thuc3i-no-logo-template/) | [ZIP](thuc3i-no-logo-template.zip) | [PDF](thuc3i-no-logo-template/preview.pdf) |

在任一源码目录执行 `latexmk -interaction=nonstopmode -file-line-error main.tex`，
输出位于 `build/main.pdf`。编译要求、替换位置及许可说明见各目录的 README 和 NOTICE。

图表蓝灰色号、使用建议与色板见 [配色参考](thuc3i-template/COLORS.md)；
两套模板均包含同样的 `colors.tex`，ZIP 同步提供。

## 其他已有模板

- [fairmeta-template.zip](fairmeta-template.zip)
- [ElegantPaper-0.12.zip](ElegantPaper-0.12.zip)
- [elegantpaper.zip](elegantpaper.zip)
- [elegantpaper-cn.pdf](elegantpaper-cn.pdf)
- [njuthesis-user-v1.4.3.zip](njuthesis-user-v1.4.3.zip)

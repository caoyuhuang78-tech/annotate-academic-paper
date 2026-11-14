# annotate-academic-paper

把英文论文 PDF 做成可离线打开的双栏精读 HTML。左栏按原顺序展示完整英文及逐段中文译文，右栏分析段落功能、论证逻辑和证据局限。英文使用五色高亮，页尾的主张—证据表可以跳回相关原文、图表和公式。

## 使用

将此仓库的技能文件夹放入 Codex 使用的技能目录，确保 `SKILL.md`、`agents/` 和 `references/` 处于同一层。提供可访问的 PDF 或指定 Zotero 条目，然后调用：

> 使用 $annotate-academic-paper 精读这篇论文，生成一个独立 HTML。逐块核对 PDF，注明仍待核对的地方。

段落显示 PDF 页码、章节与稳定的块编号。生成时还记录原文定位片段或图表位置，以便复核跨栏、跨页内容。交付前从最终 HTML 回读英文，并逐页对照原 PDF 的可见内容，核对全文覆盖、阅读顺序、公式、图表及证据链接。

## 优点与局限

- **原文、译文与批注对齐。** 阅读时可以直接对照作者措辞、翻译和解读。章节导航和块锚点适合反复定位长文。
- **证据可回查。** 表中分别链接作者主张及支撑材料，明确证据支持到什么程度，以及哪些结论还需要验证。
- **离线单文件便于保存。** 高分辨率图表内嵌后会增大文件体积，长篇论文的全文翻译和逐块复核也更耗时。
- **复杂版面需要人工判断。** 扫描件、跨栏公式、跨页表格及特殊符号可能需要 OCR、裁图和视觉复核。支撑程度由阅读者结合论文内容判断，结果取决于原件质量和实际核对范围。

## 致谢

- 感谢 [Whisper](https://x.com/Whisperrrrr66/status/2120024993287536934) 分享双栏精读提示词，启发了左栏英中对照、右栏批注和五色高亮布局。
- 感谢 infometa 的 [academic-translation](https://github.com/infometa/workbuddyskills/blob/main/skills/academic-translation/SKILL.md)。其页码、章节和英文片段联合定位的思路启发了段落溯源。
- 感谢 PengheLiu 的 [mli-paper-reading](https://github.com/PengheLiu/mli-paper-reading-skill/blob/main/skills/mli-paper-reading/SKILL.md)。其证据账本启发了主张、证据、支撑程度与待验证问题的对应关系。
- 感谢 Agentchengfeng 的 [paper-reading-skills](https://github.com/Agentchengfeng/paper-reading-skills)，提供了可在浏览器中继续追问和批注的论文解读参考。

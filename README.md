# HTML Editor · HTML 编辑工具

**Edit HTML files directly in your browser. 在浏览器中直接编辑 HTML 文件。**

[Choose a language / 选择语言](https://ddvve007.github.io/html-editor/) · [中文在线版](https://ddvve007.github.io/html-editor/html-editor.html) · [English online editor](https://ddvve007.github.io/html-editor/html-editor-en.html)

## 中文

HTML Editor 是一个无需安装的 HTML 编辑工具，适合修改网页报告、数据看板、HTML 演示和普通静态网页。支持改文字、调样式和布局、插入文本/图片/形状/线条、调整颜色和层级，也能查看和修改完整 HTML 源码。

1. 打开在线编辑器，或下载 [`html-editor.html`](html-editor.html)，在浏览器中打开。
2. 选择或拖入自己的 `.html` / `.htm` 文件。
3. 单击选中，双击改字；拖动调整位置，用手柄调整大小。A− / A+ 改字号。
4. 切换“预览”，检查页面原有按钮和互动。
5. 点击“下载HTML”，取得一份新文件。原文件保留。

- [中文使用说明](guide-zh.html)；[`sample.html`](sample.html) 是不含业务数据的练习文件。
- 工具条可拖动；加号展开插入选项；鼠标悬停图标可查看说明。
- **浏览器暂存只是工作进度；分享或换电脑前，请下载 HTML 成品。**
- 编辑器自身在本机处理文件，不上传导入内容。导入页面可能仍运行原脚本、加载外部资源；仅打开可信 HTML。
- 普通静态 HTML 和支持的动态翻页页面可用。React/Vue、水合内容、接口数据或跨域 iframe 可能需要适配。下载后重新打开，核对文字和互动。
- 可视化编辑改变页面显示；修改复制文本、公式、题目数据或交互逻辑，请使用 HTML 源码。
- 下载单文件即可离线使用；导入页面本身的联网依赖仍需联网。

## English

HTML Editor is a zero-install browser tool for editing HTML files: reports, dashboards, HTML presentations and ordinary static pages. Edit text, styles and layouts; insert text, images, shapes and lines; change colors and stacking order; or edit the full HTML source.

1. Use the online editor, or download [`html-editor-en.html`](html-editor-en.html) and open it in your browser.
2. Choose or drop your `.html` / `.htm` file.
3. Click to select, double-click text to edit, drag to move and use handles to resize. A− / A+ changes font size.
4. Switch to **Preview** to test the page’s original interactions.
5. Choose **Download HTML** to get a new `-edited.html` file. Your original is preserved.

- [English user guide](guide-en.html); [`sample.html`](sample.html) is a practice file with no business data.
- Drag the toolbar to move it. Use **+** to insert elements and hover over icons for labels.
- **Browser drafts keep work in progress. Download the finished HTML file before sharing or moving to another computer.**
- The editor processes files locally and does not upload imported content. Imported pages may still run scripts and load external resources. Open trusted HTML only.
- Static HTML and supported dynamic decks work. React/Vue, hydration, network-fed content and cross-origin frames may need adaptation. Reopen downloaded files and check edits and interactions.
- Visual editing changes the displayed page. Use **HTML source** to change copied text, formulas, exercise data or interaction logic.
- Each editor is a standalone file for offline use. Online dependencies in the imported page still require a connection.

## Files and development / 文件与维护

| File | Purpose |
| --- | --- |
| `index.html` | Bilingual sharing page / 双语入口 |
| `html-editor.html` | Standalone Chinese editor / 中文单文件编辑器 |
| `html-editor-en.html` | Standalone English editor / 英文单文件编辑器 |
| `guide-zh.html`, `guide-en.html` | User guides / 使用说明 |
| `sample.html` | Public practice page / 练习页面 |
| `html-editor-source.zip` | Shared source, translation map, build script and regression suite / 源码包 |
| `LICENSE`, `THIRD_PARTY_NOTICES.txt` | Original permission notice and icon license / 使用许可及图标许可 |

The standalone HTML files contain their own source and need no build step. For modular development, extract `html-editor-source.zip` and run `python3 build.py`. Python is needed only for development.

单文件 HTML 本身包含完整代码，使用时无需构建。维护时解压源码包，运行 `python3 build.py`，会同时生成中英文单文件；两版共用编辑逻辑，英文文案集中在翻译表中。

The bundled regression suite requires Node.js and jsdom, plus a compatible dynamic test fixture supplied by the developer. Fixture files containing private/business data are not included in this public repository. Run `node tests/regression.cjs . /path/to/fixture.html zh` or use `en` as the last argument.

本次中英文版本各通过 23 项自动回归：文字编辑、互动重画保持、预览、导出重开、页间隔离、撤销、字体/颜色、插入、源码应用、暂存、下载、工具条拖动、文本框拉伸。测试用业务课件未公开。自动回归不代表所有第三方网页都兼容。

## Attribution / 署名

© dve · [34702924@qq.com](mailto:34702924@qq.com). Based on the original Deck editor, with usability improvements and an English interface. Original permission: free to use, copy and share. See `LICENSE`. Tabler SVG icons are used under the MIT license; see `THIRD_PARTY_NOTICES.txt`.

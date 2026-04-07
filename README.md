# AutoCAD-Tools-autoSY
AutoCAD的自动化水印工具
# AutoCAD-Watermark-LISP 🛠️
### 基于 AutoLISP 的图纸自动化一键水印工具

[![AutoLISP](https://img.shields.io/badge/Language-AutoLISP-blue.svg)](https://help.autodesk.com/view/OARX/2024/ENU/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![CAFA Architecture](https://img.shields.io/badge/Affiliation-CAFA%20Architecture-red.svg)](https://www.cafa.edu.cn/)

## 📖 简介 (Introduction)
这是一个为建筑师设计的轻量级生产力工具。通过一行简单的命令，即可在当前绘区视口的右下角精确生成防伪水印，无需手动交互或对齐。

该插件专为解决建筑制图中的重复性署名劳动而设计，具备视口感知与自动图层分配功能，确保水印在不同缩放尺度下均能保持一致的视觉比例。

> **默认水印内容：** `张文新制造`

---

## 🚀 加载方法 (Loading Methods)

你可以选择以下三种方式之一来加载插件：

### 方式 1：拖拽加载（最简单）
将 `watermark_sy.lsp` 文件直接从文件夹**拖入** AutoCAD 绘图区，命令行提示加载成功后即可使用。

### 方式 2：APPLOAD 命令
1. 在命令行输入 `APPLOAD` → 回车。
2. 在弹出对话框中找到并选中 `watermark_sy.lsp`。
3. 点击 **「加载」** → **「关闭」**。

### 方式 3：自动加载（每次启动自动生效）
1. 找到 AutoCAD 支持路径下的 `acad.lsp` 或 `acaddoc.lsp`（若不存在可新建）。
2. 用记事本打开，在文件末尾添加一行代码：
   ```lisp
   (load "C:/你的路径/watermark_sy.lsp")

🖱️ 使用方式 (Usage)
加载成功后，在命令行输入快捷命令：

回车即可。水印会自动出现在当前视图的右下角，全程无需任何点选。

⚠️ 注意事项 (Technical Notes)
透明度支持：代码使用了组码 440。该功能在 AutoCAD 2011 及以上版本有效。若使用较旧版本，水印会正常显示但无透明效果，不影响核心功能。

中文字体排雷：若水印文字显示为乱码或问号，请确保当前文字样式支持中文。建议指定为 仿宋_GB2312 或 gbcbig.shx 等标准字体。

视口缩放：水印位置基于执行命令瞬间的视图快照计算。若进行大幅平移或缩放后需更新位置，请重新执行 SY。

打印控制：建议在图层管理器中根据需求决定 Watermark_Layer 是否参与打印。若需实现物理防盗图，请保持打印开启。

⚙️ 代码自定义 (Customization)
你可以编辑 .lsp 文件修改以下逻辑：

修改署名内容：定位到 (setq txt "张文新制造")。

调整比例：修改 (* h 0.02)，其中 0.02 代表水印占视图高度的 2%。

更改快捷键：修改 (defun c:SY ...) 中的 SY 为你习惯的字母。

📂 项目结构 (Project Structure)
👤 作者 (Author)
skywa1keri7 * 中央美术学院建筑学院 (CAFA Architecture)

GitHub: 

📜 开源协议 (License)
本项目基于  开源。

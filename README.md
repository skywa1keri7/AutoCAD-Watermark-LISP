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

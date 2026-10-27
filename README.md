<p align="center">
  <img src="assets/icon.png" width="128" alt="易格 Formorna 图标">
</p>

<h1 align="center">易格 · Formorna</h1>
<p align="center">让好内容，更好读。</p>

易格是一款 macOS 原生书稿整理与电子书工具。将 PDF 或 Markdown 导入书房，整理章节与排版，按需翻译，再导出适合阅读的电子书。界面采用松绿与暖白配色，提供首页、书库、内容预览和可跳过的首次使用引导。

**当前为自包含测试版，面向愿意反馈问题的用户。** 本仓库用于提供安装包、使用说明和问题反馈，不包含应用源码。

[下载安装包](https://github.com/hxyxhhh/Formorna-macOS/releases/tag/v0.3.0-beta.1) · [安装说明](INSTALL.md) · [反馈问题](https://github.com/hxyxhhh/Formorna-macOS/issues)

## 可以做什么

- 导入 PDF 或 Markdown，建立独立的书籍项目。
- 整理章节与格式，预览处理后的内容。
- 按需使用 AI 整理或翻译。
- 导出 Markdown、EPUB；安装 Calibre 后可导出 AZW3。

## 系统要求与依赖

| 项目 | 要求 |
| --- | --- |
| Mac | Apple Silicon（M 系列芯片） |
| 系统 | macOS 15 或更高版本 |
| Python / Homebrew | 无需安装，应用已内置 Python 后端和依赖 |
| PDF 解析 | 使用 MinerU 在线服务，需自己的 API 密钥和网络 |
| AI 整理、翻译 | 使用 DeepSeek 在线服务，需自己的 API 密钥和网络 |
| Markdown 格式整理、MD / EPUB 导出 | 无需配置 API |
| AZW3 导出 | 另需安装 [Calibre](https://calibre-ebook.com/download_osx) |

当前包不支持 Intel Mac 或 macOS 14。API 服务可能按各自规则计费，安装包不提供共享 API 密钥或额度。

## 数据与密钥

安装包不附带开发者的书籍、个人设置或 API 密钥。书库保存在用户电脑上，API 密钥由 macOS 钥匙串保存，正常使用时无需每次重新输入。首次引导可跳过，并可从设置中重新查看。

使用在线解析或 AI 功能时，会向对应服务发送处理所需的文档内容。请按文档的隐私要求选择是否使用这些功能。

## 测试版状态

当前 Release 为 `v0.3.0-beta.1`，应用内部版本 `0.3.0 (4)`，显示名称为「易格 · 独立测试」。

已验证原生界面启动、书库和工作区预览，以及内置后端在临时书库中完成格式整理、Markdown / EPUB 导出。已检查本地签名、DMG 完整性及打包文件清单。

**尚未完成 Developer ID 正式签名和 Apple 公证。** 首次打开可能被 macOS 拦截，请先阅读[安装说明](INSTALL.md)。全新 Mac 安装、正式签名升级后的钥匙串互通，以及在线解析和翻译仍需进一步验收。

## 反馈

请在 [Issues](https://github.com/hxyxhhh/Formorna-macOS/issues) 中提供系统版本、芯片型号、应用版本、复现步骤及错误提示。请勿公开 API 密钥或含私人内容的书稿。

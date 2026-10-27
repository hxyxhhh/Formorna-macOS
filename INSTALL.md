# 安装与首次使用

## 1. 检查系统

在苹果菜单中打开「关于本机」，确认芯片为 Apple M 系列，系统为 macOS 15 或更高版本。此测试包不适用于 Intel Mac。

## 2. 下载并安装

1. 打开 [v0.3.0-beta.1 下载页](https://github.com/hxyxhhh/Formorna-macOS/releases/tag/v0.3.0-beta.1)。
2. 在 Assets 中下载 `Formorna-arm64-test.dmg`。不要下载 GitHub 自动生成的 Source code 压缩包来安装软件。
3. 双击 DMG，将 `FormornaStandalone.app` 拖到旁边的「Applications」文件夹。
4. 在「应用程序」中打开它。软件显示名称为「易格 · 独立测试」。安装完成后可以推出磁盘镜像。

无需安装 Python、Homebrew 或执行 pip 命令。

## 3. 关于 macOS 首次打开提示

此版本仅有本地 ad-hoc 签名，尚未通过 Apple 公证。如果系统提示无法验证开发者，请先确认文件来自本仓库的 Release、校验值一致，并自行决定是否信任此测试版。

确认信任后，可在尝试打开应用后进入「系统设置 → 隐私与安全性」，找到对应应用的「仍要打开」，按系统提示确认。不同系统版本的提示可能不同。详情见 [Apple 官方说明：在 Mac 上安全地打开 App](https://support.apple.com/zh-cn/102445)。

不要关闭全局安全保护，也不要直接忽略“已损坏”或检测到恶意软件的提示；遇到这些情况请停止安装并反馈。

## 4. 第一次使用

- 首次引导可以完成，也可以点击「跳过引导」。之后从首页开始，教程可在设置中重看。
- 建议先导入一份非敏感的 Markdown，体验格式整理和 EPUB 导出；这一步不需要 API。
- 需要 PDF 解析时，在设置中填写自己的 [MinerU API](https://mineru.net) 密钥。
- 需要 AI 整理或翻译时，填写自己的 [DeepSeek API](https://platform.deepseek.com) 密钥。
- 密钥保存到 macOS 钥匙串。不要把密钥发送到 Issues。
- 仅导出 AZW3 时需要另行安装 [Calibre](https://calibre-ebook.com/download_osx)。Markdown 和 EPUB 导出不依赖 Calibre。

## 5. 校验下载文件（可选）

同时下载 Release 中的 `Formorna-arm64-test.dmg.sha256`，将它与 DMG 放在同一文件夹。在该文件夹打开终端运行：

```sh
shasum -a 256 -c Formorna-arm64-test.dmg.sha256
```

显示 `OK` 表示文件与发布时一致。校验值不替代对发布者的信任或 Apple 公证。

## 6. 数据、更新与卸载

默认书库位于 `~/Documents/Formorna`，设置位于 `~/Library/Application Support/Formorna`，API 密钥在系统钥匙串中。书库也可以使用设置中指定的位置。

更新前退出应用，将新版本拖到「应用程序」替换旧版本；请保留书库和设置目录。建议测试版用户先备份重要书稿。删除应用本体不会自动删除书库或钥匙串密钥。

已有用户在同一台 Mac 上可能看到原来的书籍，这是应用读取本机书库的结果；这些书籍不在安装包里。

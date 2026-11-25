# DeepSeek Archive Viewer

[Русский](./README.ru.md) | [English](./README.en.md) | **简体中文**

**DeepSeek** 官方导出数据归档的独立离线查看器。  
以**单个 HTML 文件**（`deepseek-archive-viewer.html`）的形式提供，在任意浏览器中打开即可完全本地运行，高度还原 DeepSeek 熟悉的聊天界面与功能——无需联网、无需安装软件、无需本地服务器，也不会向网络发送任何数据。

---

## 核心特性

- **完全离线与隐私安全**：所有归档解析均在浏览器本地完成。界面直接从本地文件运行，不发起任何网络请求，您的数据始终留在自己的设备上。
- **全面兼容 DeepSeek 导出格式**：完整支持新版导出格式（`chat_session_index.json` 与 `chat_sessions/*.json`），同时也兼容旧版 `conversations.json` 格式。
- **针对大型归档优化**：即使包含数百上千个对话，也能按需加载、快速打开，占用内存极低。
- **便捷加载方式**：支持选择或直接拖拽 **`.zip` 压缩包** 或 **已解压文件夹**。打开已解压文件夹时，还可直接在界面中保存消息修改、重命名或删除单个对话。
- **原汁原味的 DeepSeek 对话界面与结构**：
  - 置顶对话固定在顶部，其余对话按月份分组并显示日期；
  - 侧边栏支持按对话标题实时搜索；
  - 默认折叠 **深度思考（Thinking）**（含思考耗时）与 **联网搜索（Search）**（含来源链接与引用标注）区块；
  - 完整渲染 Markdown、带复制按钮的代码高亮块、表格以及数学公式（**KaTeX**）；
  - 支持图片附件放大预览与文件下载；
  - 方便地在多个重新生成的回复分支（`< 1 / N >`）之间切换，不重置上下文对话。
- **文本工具与导出**：
  - 对话内全文搜索、高亮匹配并快速跳转；
  - 支持消息多选模式，可一次性批量删除对话中的多条消息；
  - 支持将当前对话导出为整洁的 Markdown（`.md`）文件；
  - 点击回复旁的 DeepSeek 图标可复制内容或切换至 RAW 原文编辑器修改文本。
- **界面与显示设置**：
  - 界面语言：**Русский**、**English**、**简体中文**；
  - 支持切换阅读字体（**DeepSeek**、**Roboto**、**Serif**）和字号大小；
  - 针对拉丁字母、西里尔字母及中日韩文字（CJK）优化显示效果。

---

## 使用方法

1. 前往 **[Releases](https://github.com/IvanSkriptov/deepseek-archive-viewer/releases)** 下载 **`deepseek-archive-viewer.html`**。
2. 使用任意现代浏览器（Chrome、Edge、Firefox、Safari）打开该文件。
3. 在界面中点击 **选择 .zip 压缩包** 或 **选择文件夹**（或直接将压缩包/文件夹拖入浏览器窗口）即可加载数据。

---

## 使用须知

- **保存消息修改、重命名及删除对话**仅在使用支持 *File System Access API* 的 Chromium 内核浏览器（Chrome、Edge、Brave）打开**已解压文件夹**时可用。在 Firefox、Safari 或打开 `.zip` 压缩包时，文本编辑仅在当前会话生效，切换对话或关闭页面后会重置。
- **CJK 字体**：为保持独立 HTML 文件体积精简，中文与日文等字符将优先调用您操作系统中已安装的字体。

---

## 开源协议

本项目基于 **MIT 协议** 发布，详见 [`LICENSE`](./LICENSE)。  
内置第三方开源库与字体的版权信息请查看 [`THIRD-PARTY-LICENSES.md`](./THIRD-PARTY-LICENSES.md)。

Copyright IvanSkriptov 2026

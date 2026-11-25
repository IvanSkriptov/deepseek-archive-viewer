# DeepSeek Archive Viewer

[Русский](./README.ru.md) | **English** | [简体中文](./README.zh.md)

An autonomous offline viewer for official **DeepSeek** data export archives.  
Delivered as a **single HTML file** (`deepseek-archive-viewer.html`) that opens directly in any browser and faithfully reproduces the familiar DeepSeek chat interface and features completely locally — with no internet connection, installation, local server, or network uploads.

---

## Key Features

- **Autonomous & Private**: all archive parsing happens locally in your browser. The interface runs directly from a file, makes zero network requests, and keeps all your data strictly on your device.
- **Full Support for DeepSeek Export Formats**: seamlessly handles the new export structure (`chat_session_index.json` + `chat_sessions/*.json`) as well as the legacy `conversations.json` format.
- **Optimized for Large Archives**: exports with hundreds or thousands of conversations load lazily without long delays or excessive memory usage.
- **Flexible Opening**: pick or drag-and-drop either a **`.zip` archive** or an **extracted folder**. When opening an extracted folder in supported browsers, you can save message edits, rename chats, and delete individual conversations directly from the UI.
- **Authentic DeepSeek Chat UI & Structure**:
  - Pinned conversations at the top and chronological monthly grouping with dates;
  - Sidebar search by conversation title;
  - Collapsible **Thinking** blocks (with elapsed reasoning time) and **Search** blocks (with links and inline citations);
  - Full Markdown rendering, syntax-highlighted code blocks with copy button, tables, and math formulas (**KaTeX**);
  - Attached image lightbox preview and file downloads;
  - Clean branch switching (`< 1 / N >`) between multiple regenerated response variants without losing the thread.
- **Text Tools & Export**:
  - In-chat text search with match highlighting and navigation;
  - Message selection mode for batch deleting messages from a conversation;
  - Export any conversation to a clean Markdown (`.md`) file;
  - Click the DeepSeek icon next to a response to copy text or toggle a RAW text editor.
- **Display & Language Settings**:
  - Interface languages: **Русский**, **English**, **简体中文**;
  - Configurable reading font preset (**DeepSeek**, **Roboto**, **Serif**) and text size;
  - Crisp rendering for Latin, Cyrillic, and East Asian (CJK) text.

---

## How to Run

1. Go to **[Releases](https://github.com/IvanSkriptov/deepseek-archive-viewer/releases)** and download **`deepseek-archive-viewer.html`**.
2. Open the downloaded file in any modern browser (Chrome, Edge, Firefox, Safari).
3. Click **Select .zip** or **Select folder** (or simply drag and drop your archive or folder into the browser window).

---

## Notes & Limitations

- **Saving message edits, renaming, and deleting chats** require opening an **extracted folder** in a browser that supports the *File System Access API* (Chromium-based browsers: Chrome, Edge, Brave). In Firefox, Safari, or when opening a `.zip` archive, text edits are ephemeral and reset when switching chats or closing the tab.
- **CJK Fonts**: to keep the standalone HTML compact, Chinese/Japanese/Korean characters use your operating system's installed fonts.

---

## License

Released under the **MIT License** — see [`LICENSE`](./LICENSE).  
Details on bundled open-source libraries and fonts are listed in [`THIRD-PARTY-LICENSES.md`](./THIRD-PARTY-LICENSES.md).

Copyright IvanSkriptov 2026

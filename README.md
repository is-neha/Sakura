# Sakura
An ultra-lightweight, 100% offline AI reading assistant for Windows written in native C++ using llama.cpp and Qwen 2.5 (0.5B). Consumes 0.0% idle CPU and pops up an instant sticky note on Ctrl+C.
# ⚡ Instant Simplifier (v1.0)
> **An ultra-lightweight, 100% offline AI reading companion for Windows built in native C++.**

Highlight any complex text in your browser, PDF, or document, press <kbd>Ctrl</kbd> + <kbd>C</kbd>, and a warm yellow sticky note pops up right next to your cursor with an instant AI-simplified breakdown.

---

## 💡 Why Instant Simplifier?

Most desktop AI tools rely on heavy stacks like Python, PyTorch, Docker, or Ollama, which require gigabytes of disk space and constantly consume background CPU and RAM.

**Instant Simplifier** is built natively in C++ using `llama.cpp` and Windows APIs to be as light and non-intrusive as possible:

* ⚡ **0.0% Idle CPU:** Native Windows event listener (`AddClipboardFormatListener`) — zero polling loops and no battery drain.
* 🧠 **Low Memory Footprint:** The model weights only activate when inference is requested, freeing memory back to ~8 MB when the note is dismissed.
* 🔒 **100% Offline & Private:** Powered locally by **Qwen 2.5 (0.5B)**. Zero internet connection, zero API keys, and zero telemetry.
* 📦 **Zero Dependencies:** Completely portable standalone release. No Python, no CUDA drivers, and no installation wizards required.

---

## 📥 Download & Quick Start

### 1. Download
Go to the **[Releases](../../releases/latest)** section and download **`InstantSimplifier.zip`** (~331 MB).

### 2. Run
1. Extract `InstantSimplifier.zip` anywhere on your computer.
2. Double-click **`InstantSimplifier.exe`**.
   *(It starts silently in the background — no intrusive command prompts or heavy UI windows).*

### 3. Use
* Highlight any difficult sentence in a textbook, paper, or article.
* Press <kbd>Ctrl</kbd> + <kbd>C</kbd>.
* A warm yellow sticky note will appear near your cursor with the AI summary!
* **Dismiss:** Click anywhere outside the note or press <kbd>Esc</kbd>.

---

## ⚠️ Notes & Known Limitations in v1.0

* **Closing the App:** As a minimalist v1 prototype, the app runs headlessly in the background. To completely close it, end **`InstantSimplifier.exe`** in Windows Task Manager.
* **Context Limit:** Tuned for ~1,000 tokens (4–5 sentences at a time). It is optimized for fast sentence simplification rather than summarizing entire books.

---

## 💻 System Requirements

* **OS:** Windows 10 or Windows 11 (64-bit)
* **RAM:** 4 GB minimum (Uses ~300 MB during active generation, ~8 MB while idle)
* **Disk Space:** ~350 MB (Entirely portable)

---

## 👨‍💻 Author & Feedback

Built as an independent project exploring low-level native LLM deployment on constrained hardware.

If you encounter any bugs or have feature suggestions, feel free to open an **[Issue](../../issues)**!

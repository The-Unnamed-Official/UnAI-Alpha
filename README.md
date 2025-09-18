# UnAI Alpha — Unnamed Artificial Intelligence

UnAI is a clean, fast, ChatGPT-style web UI for chatting with AI.
It’s **just HTML + CSS + JS** (no build tools, no framework), so you can drop it onto **GitHub Pages** and it runs.

* **Name:** *UnAI — Unnamed Artificial Intelligence*
* **Demo UX:** Chat-like interface with smooth animations, Markdown rendering, Light/Dark/AMOLED themes, local auth, and persistent conversations.

---

## ✨ Features

* **Modern Chat UI**

  * Sidebar with conversation list + search
  * “Start new chat” CTA, **rename**, **delete** (with modal), **clear messages** (with modal)
  * **Shift+Click** on delete = skip confirmation (instant delete)
  * Tooltip on delete (“Shift-click: delete instantly”)

* **Theming & Motion**

  * **Light / Dark / AMOLED** themes
  * Subtle 120–220ms animations & transitions

* **Auth (Demo)**

  * Login/Register stored in **localStorage** (no backend)
  * “You” pill (top-left) with **drop-up menu** for **Settings** and **Log out**

* **Profile & Avatars**

  * Upload/remove avatar in Settings (stored in localStorage, size-optimized)
  * If no avatar, a **user icon** shows everywhere (Settings preview, “You” pill, chat messages)
  * Each message shows the **speaker name** (“You” or your display name, and “UnAI”)

* **Markdown Rendering**

  * Supports **bold**, *italics*, `inline code`, `fenced blocks`, lists, links, tables
  * Sanitized with DOMPurify

* **Models**

  * **Model switcher** in Settings (segmented control):

    * `UnAI-0.1-1b-instant` (fast)
    * `UnAI-0.1-10b-versatile` (quality)
  * Model pill in top bar updates to show your choice

* **Keyboard Shortcuts**

  * `Enter` send, `Shift+Enter` newline
  * `/` focus composer
  * `Ctrl+N` new chat
  * `Ctrl+K` search conversations

* **Persistence**

  * Conversations, auth, theme, model, avatar all stored in **localStorage**
    (`unai_state_v2` key)

* **Mobile-friendly**

  * Responsive sidebar, smooth slide-in/out

---

## 🧩 Project Structure

```
index.html           # all-in-one file (HTML/CSS/JS), or split if you prefer
unai.png             # UnAI logo (also used as assistant avatar)
README.md
```

> The app uses CDN scripts for **marked** (Markdown) and **DOMPurify**, and may load **Font Awesome** for icons.

## 🧭 Tips & Shortcuts

* **Shift+Click** on the per-chat trash icon = delete immediately (skips modal).
* Hover the trash icon to see the tip (“Shift-click: delete instantly”).
* Click the user pill to open **Settings/Log out** drop-up.
* **Markdown** is parsed and sanitized; raw text types during the “stream” then converts to HTML when complete.

---

## 🐞 Troubleshooting

* **Model decommissioned**
  Use `UnAI-0.1-1b-instant` (1B fast) or `UnAI-0.1-10b-versatile` (10B quality). The Worker alias map can auto-upgrade older names.

* **WebGPU not available**
  Local (WebLLM) mode won’t run on some browsers/devices. Keep the cloud proxy as a fallback.

---

## 🗺️ Roadmap (ideas)

* Export/share conversations (JSON/Markdown)
* Real authentication backend
* Prompt library + tools
* System prompts & temperature UI
* Image attachments and image generation

---

## 🙌 Credits

* **marked** (Markdown) + **DOMPurify** (sanitization)
* **Font Awesome** for icons

---

**Enjoy UnAI!** If you run into anything while deploying to GitHub Pages or wiring the Worker, open an issue or ping me with the error message and I’ll help you squash it.

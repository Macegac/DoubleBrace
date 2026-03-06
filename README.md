# 🌌 DoubleBrace - AI Character Card Studio

Welcome to **DoubleBrace**! 🎭 A powerful, responsive, and visually stunning web application designed to help you build, manage, and export AI roleplay characters compatible with the **V2 Character Card Specification**.

Whether you're crafting a cyberpunk hacker, a fantasy knight, or a sci-fi captain, DoubleBrace provides a professional laboratory environment—powered by an intuitive glassmorphism UI and AI-assisted generation! ✨

**TRY IT HERE:** [https://macegac.github.io/DoubleBrace/](https://macegac.github.io/DoubleBrace/)

---

## ✨ Features

### 🗂️ Advanced Node-Based Descriptions
- Organize character traits, physical features, and lore using a highly visual accordion node system. 🧩
- Group descriptors into **Categories** for clean, manageable character structures.
- Easily add, rename, or reorder nodes via drag-and-drop!

### 📖 Integrated Lorebooks
- Build deep, context-aware backgrounds using the native Lorebook builder. 📜
- Link entries to **Keywords** which cleanly export as standard string arrays.
- Includes insertion order controls and `{{char}}` / `{{user}}` macro tools for AI perfection.
- **Advanced Lorebook Fields:** Control entry **Position** (before/after char def or author note), **Depth**, **Regex** keyword matching, and per-entry **Enable/Disable** toggles.
- **Lorebook Search:** Instantly filter entries by name, keyword, or content.

### 🌍 Global Info & Full V2 Compatibility
- Fill out all standard V2 fields: **First Message, Alternate Greetings, Scenario, Example Dialogs, Creator Notes, and Tags**. 📝
- **Personality Summary:** A plain-text personality field separate from the main description, fully exported in the V2 spec.
- **System Prompt:** Inject system-level instructions before the conversation, with AI generation support.
- **Post History Instructions:** Add instructions at the jailbreak position (after chat history), with macro support.
- **Card Metadata:** Set a `character_version` string for tracking card revisions.
- **Alternate Greetings Manager:** Recursively add as many fallback greetings as you need!
- **Macro Buttons:** Smart macro insertion buttons that respect your cursor position in textareas. ⚡

### 🤖 Built-in AI Generation
- Connect your **OpenRouter** or **Gemini** API keys directly in the Options tab! 🔑
- **Streaming Responses:** AI output streams in real-time token by token — no more waiting for the full response to appear.
- **Lightning Bolt (⚡) Icons:** Click to have the AI write descriptors, scenarios, system prompts, or greetings based on the character's existing context.
- **Custom AI Prompts:** Fully customize the system instructions used for every type of AI generation in the Settings tab.

### 💬 ChitChat: In-App Testing
- **Live Interaction:** Chat with your character directly inside the app to test their personality, scenario, and speech patterns before exporting! 🗣️
- **Real-time Streaming:** Watch the character's response appear word by word, just like a real AI frontend.
- **Regenerate:** Re-roll the last character response with a single click without retyping your message.
- **Persistent Chat History:** Conversations are saved per-character to IndexedDB and restored automatically when you return.

### 🧪 Experimental: Auto Character Generator
- Provide a name and a short prompt (e.g., "A grumpy space pirate who loves space cats"), and the AI will auto-generate an entire categorized character profile from scratch! 🤯

### 📥 PNG & JSON Import
- **Import Character PNGs:** Open any V2-spec character card PNG — DoubleBrace reads the embedded metadata and loads the full character into your workspace, including the avatar image.
- **Import Character JSON:** Load raw V2 character card JSON files directly.
- **Smart Description Handling:** Cards from other tools that use a flat description field (no category tree) are handled gracefully:
  - **Without AI:** The description is automatically placed into a single "Description" category and descriptor, ready to edit.
  - **With AI:** You're offered the option to have the AI intelligently parse and segment the description into meaningful categories and descriptors. An animated progress bar with live percentage tracks the parsing in real time.

### 🔢 Per-Field Token Counter
- Every major text field (First Message, Scenario, Example Dialog, System Prompt, etc.) displays a live **token estimate** just above the textarea.
- Color-coded for quick budget awareness: normal → **yellow** (500+ tokens) → **red** (1000+ tokens).
- The **Raw Output** modal shows the total compiled token count for the entire card.
- The **Descriptions tab** shows a live token estimate across all categories and descriptors.

### ↩️ Undo / Redo
- A **20-step undo stack** protects all destructive actions: AI generation, node deletion, gallery loads, and imports.
- **Ctrl+Z** to undo, **Ctrl+Y** or **Ctrl+Shift+Z** to redo.
- Undo and Redo buttons are also available in the Quick Actions bar.

### 📚 The Library System
- Save your best categories or individual descriptors to your local **Library**! 📖
- Reuse them across different characters with a single click.
- Everything is saved locally via IndexedDB for privacy and speed. 🔒

### 🎨 Stunning Neon Glassmorphism UI
- **Dark Nebula & Light Aurora:** Switch between two beautiful default themes or create your own. 📱💻
- **Custom Theme Engine:** Tweak every CSS variable (colors, gradients, blurs) on the fly, then save, export, or import your custom designs! 🌈

### 💾 Save, Load & Export
- **Local Gallery:** Quick-save your characters to the built-in gallery with support for duplication and deletion. 🖼️
- **Gallery Search:** Filter your saved characters by name, tag, or creator instantly.
- **Workspace Restoration:** Never lose work! The app automatically saves your active workspace and prompts to restore it if you refresh or close the tab. 🔄
- **Raw JSON & Token Count:** View the raw JSON export with an integrated **Token Counter** to estimate character size. 📋
- **V2 PNG Generation:** Upload a character avatar and magically export a standard V2 Character Card PNG with the metadata embedded directly inside the image! 🪄🖼️

---

## 🚀 How to Use

1. **Open the App:** Simply open `index.html` in your modern web browser. 🌐
2. **Setup AI (Optional):** Go to the ⚙️ **Settings** tab, enable AI features, and plug in your API key to unlock generation features.
3. **Build or Import:** Use the 📝 **Descriptions** and 🌍 **Global Info** tabs to craft your character, or import an existing PNG/JSON card from the Quick Actions bar.
4. **Test:** Use the 💬 **ChitChat** tab to verify the character's voice.
5. **Export:** Open the hamburger menu (🍔) and click **Generate PNG** or **Raw Output** to take your character to your favorite AI frontend (like SillyTavern)!

---

## 📱 Progressive Web App (PWA)
DoubleBrace is PWA-ready! On most mobile browsers, you can "Add to Home Screen" to use it as a standalone app with its own icon and offline capabilities.

Enjoy bringing your characters to life! 🎭✨

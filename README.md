# DoubleBrace - AI Character Card Studio

**DoubleBrace** is a single-file web application for building, managing, and exporting AI roleplay characters compatible with the **V2 Character Card Specification** — no installation, no server, no build step. Just open `index.html` in your browser and start creating.

Craft any character: organize traits and lore in a visual node tree, hook up your **OpenRouter or Gemini API key** to generate descriptions and dialogue with AI, test your character's voice in the built-in chat, then export a ready-to-use V2 PNG card.

**Live Demo:** [https://macegac.github.io/DoubleBrace/](https://macegac.github.io/DoubleBrace/)

---

## Features

### Node-Based Descriptions
- Organize character traits, physical features, and lore using an accordion node system.
- Group descriptors into **Categories** for clean, manageable character structures.
- Add, rename, and reorder nodes via **drag-and-drop**.
- Save your best categories or descriptors to the **Description Library** and reuse them across characters.

### Integrated Lorebooks
- Build deep, context-aware backgrounds using the native Lorebook builder.
- Link entries to **Keywords** which export as standard string arrays.
- `{{char}}` / `{{user}}` macro tools for AI-ready content.
- **Advanced Fields:** Control entry **Position** (before/after char def or author note), **Depth**, **Regex** keyword matching, and per-entry enable/disable toggles.
- **Lorebook Search:** Instantly filter entries by name, keyword, or content.

### Global Info & Full V2 Compatibility
- Fill out all standard V2 fields: **First Message, Alternate Greetings, Scenario, Example Dialogs, Creator Notes, Tags**.
- **Personality Summary:** Plain-text personality field, fully exported in the V2 spec.
- **System Prompt:** Inject system-level instructions before the conversation, with AI generation support.
- **Post History Instructions:** Add instructions at the jailbreak position (after chat history).
- **Card Metadata:** Set a `character_version` string for tracking card revisions.
- **Macro Buttons:** Smart macro insertion buttons that respect your cursor position.

### Built-in AI Generation
- Connect your **OpenRouter** or **Gemini** API keys in the Settings tab.
- **Streaming Responses:** AI output streams in real-time, token by token.
- **AI Bolt Icons:** Click to have the AI write descriptors, scenarios, system prompts, or greetings based on the character's existing context.
- **Custom AI Prompts:** Fully customize the system instructions used for every type of AI generation.
- **Sampler Settings:** Tune **Temperature**, **Top-P**, and **Max Tokens** directly from the Settings tab to control output creativity and length.
- **Test Connection:** Verify your API key and model are working with a one-click connection test — shows success or error feedback inline.

### ChitChat: In-App Testing
- **Live Interaction:** Chat with your character directly inside the app to test personality and voice before exporting.
- **Real-time Streaming:** Watch responses appear word by word.
- **Regenerate:** Re-roll the last character response with a single click.
- **Edit Messages:** Click the pencil icon on any message to edit it inline. Confirm with Ctrl+Enter or cancel with Escape.
- **Delete Messages:** Remove any individual message from the chat history with the trash icon.
- **Persistent Chat History:** Conversations are saved per-character to IndexedDB and restored automatically.

### Auto Character Generator (Experimental)
- Provide a name and a short prompt, and the AI auto-generates a complete, categorized character profile from scratch.

### PNG & JSON Import
- **Import Character PNGs:** Reads the embedded V2 metadata and loads the full character, including the avatar image.
- **Import Character JSON:** Load raw V2 character card JSON files directly.
- **Smart Description Handling:** Cards from other tools with a flat description field can be imported as-is, or parsed by AI into proper categories and descriptors — with a live animated progress bar.

### Per-Field Token Counter
- Every major text field shows a live **token estimate**.
- Color-coded: normal → yellow (500+ tokens) → red (1000+ tokens).
- The **Raw Output** modal shows the total compiled token count for the entire card.
- The **Descriptions tab** shows a running total across all categories and descriptors.

### Undo / Redo
- **20-step undo stack** covering AI generation, node deletion, gallery loads, and imports.
- **Ctrl+Z** to undo, **Ctrl+Y** / **Ctrl+Shift+Z** to redo.
- Undo and Redo buttons are also in the Quick Actions bar.

### The Library System
- Save categories or individual descriptors to your local **Library**.
- Reuse them across characters with a single click.
- Stored locally in IndexedDB — private and fast.

### Accessibility
- **Dyslexia-Friendly Font:** Switches the entire app to [OpenDyslexic](https://opendyslexic.org/) — covers all inputs, textareas, and buttons.
- **Increased Spacing:** Wider line height, letter spacing, and word spacing across all text areas. Works well alongside the dyslexic font.
- **Large Text:** Bumps the base font size up across the entire app.
- **High Contrast:** Stronger borders, brighter muted text, and visible focus rings for keyboard navigation.
- **Reduce Motion:** Disables all transitions and animations — recommended for motion sensitivity or vestibular disorders.
- All accessibility settings persist across sessions.

### Dark Veldt & Sage Light Themes
- **Dark Veldt:** Deep charcoal with forest green tones and a bright lime accent — the new default dark theme. Inspired by a professional dark dashboard aesthetic.
- **Sage Light:** Clean off-white with natural sage green accents — the new default light theme.
- **Custom Theme Engine:** Tweak every CSS variable (colors, gradients, blurs, border radius) live in the Settings tab, then save, export, or import your custom designs.
- Typography powered by **Space Grotesk** — a geometric, modern typeface with excellent number rendering.

### Find & Replace
- Search across all character text fields (descriptions, lorebook, prompts) and replace in one action.
- Leave the replacement field empty to delete all matches.
- Shows a count of replacements made, or a "no matches" notice.

### Card Preview
- Preview the fully compiled card output before exporting — `{{char}}` is substituted with the actual character name so you can read it exactly as an AI frontend would receive it.
- Shows Description, First Message, Scenario, Example Dialogs, and System Prompt sections.
- Jump straight to Raw JSON or Export PNG from the preview modal.

### Save, Load & Export
- **Local Gallery:** Quick-save characters with support for duplication and deletion.
- **Gallery Search:** Filter saved characters by name, tag, or creator instantly.
- **Default Author:** Set a global author name in Settings that is automatically applied to all exported cards.
- **Workspace Restoration:** The app auto-saves your active workspace and prompts to restore it on reload.
- **Raw JSON & Token Count:** View the raw JSON export with an integrated token counter.
- **V2 PNG Generation:** Upload a character avatar and export a V2 Character Card PNG with metadata embedded directly inside the image.

---

## How to Use

1. **Open:** Open `index.html` in any modern web browser — no server needed.
2. **Setup AI (Optional):** Go to the **Settings** tab, enable AI features, and add your API key.
3. **Build or Import:** Use the **Descriptions** and **Global Info** tabs to craft your character, or import an existing PNG/JSON from the Quick Actions bar.
4. **Test:** Use the **ChitChat** tab to verify the character's voice.
5. **Export:** Click **Generate PNG** or **Raw Output** in the Quick Actions bar to take your character to your favorite AI frontend (e.g., SillyTavern).

---

## Progressive Web App (PWA)
DoubleBrace is PWA-ready. On most mobile browsers, use "Add to Home Screen" for a standalone app experience with its own icon and offline capabilities.

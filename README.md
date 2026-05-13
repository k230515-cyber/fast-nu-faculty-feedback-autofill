# ⚡ Feedback AutoFill — Chrome Extension

A Chrome extension that automatically selects the first option for every radio button question on feedback forms and optionally submits the form — all in one click.

---

## Features

- ✅ Auto-selects the first option (e.g. "Strongly Agree") for all MCQ/radio button questions
- 🚀 One-click fill + submit
- 📋 Fill-only mode if you want to review before submitting
- 🔍 Built-in debug scanner to inspect radio inputs on any page
- ⚙️ Works with standard HTML forms and React/Angular-based forms
- 🔄 Scroll-to-submit toggle for smooth UX

---

## Installation

Since this extension is not published on the Chrome Web Store, install it manually:

1. Download or clone this repository
   ```bash
   git clone https://github.com/YOUR_USERNAME/feedback-autofill-extension.git
   ```

2. Open Chrome and go to:
   ```
   chrome://extensions/
   ```

3. Enable **Developer mode** (toggle in the top-right corner)

4. Click **"Load unpacked"**

5. Select the `feedback-autofill-extension` folder

The extension icon will appear in your Chrome toolbar.

---

## Usage

1. Open your feedback form in Chrome
2. Click the **Feedback AutoFill** icon in the toolbar
3. Choose an action:
   - **Fill All & Submit** — fills every radio question and clicks the submit button
   - **Fill Only (no submit)** — fills all questions so you can review before submitting manually
4. Use the **🔍 Debug** button if the extension isn't working — it scans the page and shows what radio inputs were detected

---

## File Structure

```
feedback-autofill-extension/
├── manifest.json       # Chrome extension config (Manifest V3)
├── popup.html          # Extension popup UI
├── popup.js            # Core logic — form filling & submission
└── icons/
    ├── icon16.png
    ├── icon48.png
    └── icon128.png
```

---

## How It Works

The extension uses multiple strategies to detect and select radio buttons:

1. **Named groups** — groups radios by their `name` attribute and selects the first in each group
2. **DOM proximity** — when radios share no name, walks up the DOM tree to find question containers
3. **ARIA radios** — handles `[role="radio"]` custom components
4. **Label fallback** — clicks labels directly if standard selection doesn't work
5. **Framework-aware** — uses the native prototype setter + React's `_valueTracker` trick to work with React/Angular forms

---

## License

MIT — free to use and modify.

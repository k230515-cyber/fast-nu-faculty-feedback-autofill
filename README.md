# ⚡ FLEX Feedback AutoFill — Chrome Extension

A Chrome extension for **FAST National University** students that automatically fills out faculty feedback forms on **FLEX** (the FAST Learning & Examination portal) and submits them in one click.

---

## What It Does

FLEX requires students to submit feedback for every faculty member each semester. This extension automates that — it selects the first option (**Strongly Agree**) or the last option (**Strongly Disagree**) for every question on the feedback form and hits submit, so you're done in seconds instead of clicking through dozens of radio buttons manually.

---

## Features

- ✅ Auto-selects **Strongly Agree** or **Strongly Disagree** for all feedback questions
- 🚀 Fills and submits the form in one click
- 📋 **Fill Only** mode — fill first, review, then submit manually
- 🔍 Debug scanner to diagnose issues on any form page
- 🔄 Smooth scroll to submit button before submitting

---

## Installation

This extension is not on the Chrome Web Store — install it manually in a minute:

1. **Download or clone this repo**
   ```bash
   git clone https://github.com/YOUR_USERNAME/flex-feedback-autofill.git
   ```
2. **Extract the zip file**

3. Open Chrome and navigate to:
   ```
   chrome://extensions/
   ```

4. Enable **Developer mode** (toggle in the top-right corner)

5. Click **"Load unpacked"**

6. Select the downloaded/cloned folder

The ⚡ icon will appear in your Chrome toolbar.

---

## How to Use

1. Log in to **FLEX** and open a faculty feedback form
2. Click the **⚡ Feedback AutoFill** icon in the toolbar
3. Click **"Fill All & Submit"**
4. Done ✅

> For multiple feedback forms, just navigate to each one and repeat step 3.

---

## Options

| Option | Description |
|--------|-------------|
| **Fill All & Submit** | Selects Strongly Agree for all questions and submits |
| **Fill Only (no submit)** | Fills all answers so you can review before submitting |
| **Scroll to submit** | Smoothly scrolls to the submit button before clicking |
| **🔍 Debug** | Scans the page and shows detected radio inputs — useful if the form isn't being filled |

---

## File Structure

```
flex-feedback-autofill/
├── manifest.json       # Chrome extension config (Manifest V3)
├── popup.html          # Extension popup UI
├── popup.js            # Core logic — form detection, filling & submission
└── icons/
    ├── icon16.png
    ├── icon48.png
    └── icon128.png
```

---

## Compatibility

- ✅ Google Chrome (Manifest V3)
- ✅ FAST-NU FLEX portal (flexstudent.nu.edu.pk)
- ✅ Although developed for Flex portal, it works on all standard and React/Angular-based forms

---

## Disclaimer

This extension is an unofficial student utility and is not affiliated with or endorsed by FAST National University or the FLEX platform. Use it responsibly.

---

## License

MIT — free to use and modify.

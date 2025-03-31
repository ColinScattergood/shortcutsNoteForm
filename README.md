# 📝 shortcutsNoteForm

A minimal web form designed to work seamlessly with Apple Shortcuts and Evernote on macOS and iOS. This project helps you quickly copy notes from Granola AI (or anywhere else) and save them to Evernote using a simple form and native automation.

## ✨ What It Does

- Opens a clean, dark-mode-friendly note entry form
- Lets you paste in a note title and body
- Submits the data directly into Apple Shortcuts
- Triggers a Shortcut to archive the note in Evernote

## 🌐 Live Demo

👉 [Launch the form](https://colinscattergood.github.io/shortcutsNoteForm/noteform.html)

## ⚙️ How It Works

1. You trigger a Shortcut from the macOS menu bar or a keyboard shortcut
2. That Shortcut opens this form in a floating web app (via Nativefier)
3. You enter the title and body of your note
4. The form sends the data back to a second Shortcut (`Add To Evernote for Mac`)
5. The Shortcut creates a new Evernote note using the passed content

## 🖥️ Native Mac App (Optional)

You can wrap this form into a floating macOS app using [Nativefier](https://github.com/nativefier/nativefier):

```bash
npm install -g nativefier

nativefier "https://colinscattergood.github.io/shortcutsNoteForm/noteform.html" \
  --name "QuickNoteForm" \
  --single-instance \
  --width 500 \
  --height 400 \
  --disable-dev-tools \
  --tray \
  --title-bar-style hiddenInset \
  --transparent
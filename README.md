# 📋 Clipboard Saver — A macOS Automator App

Effortlessly **save your clipboard contents** as a timestamped `.txt` file directly to your **Desktop** with just one click. Ideal for writers, developers, researchers, or anyone who frequently copies text and wants a quick way to archive clipboard data.

---

## ✨ Features

- 📁 **Instant Clipboard Archiving** — Saves clipboard content as a plain text file.  
- 🕒 **Auto-Timestamped Files** — Each file is uniquely named based on the date and time of saving.  
- 🔔 **macOS Native Notifications** — Get instant confirmation when the file is saved.  
- ⚡ **Lightweight & Fast** — Built using native macOS tools with no external dependencies.  
- 🛡️ **Privacy-First** — All operations are local; no data leaves your machine.

---

## 📋 How It Works

1. **Copy any text** (`⌘ + C`).
2. **Run the app** (via double-click, Dock shortcut, or keyboard shortcut).
3. The app:
   - Retrieves your clipboard content using `pbpaste`.
   - Saves it to your **Desktop** with this naming format:
     ```
     YYYYMMDDHHMMSS • txt
     ```
     *Example:* `20250224153045 • txt`
   - Sends a **macOS notification** confirming the save.

---

## 🖥️ Installation

### ✅ **Download & Install**

1. **[Download the latest release](#)** (`.dmg` file).
2. **Open** the `.dmg` and **drag** the app into your **Applications** folder.
3. On the first run, right-click the app and select **Open** if macOS flags it as from an unidentified developer.

### 💡 **Optional: Add to Dock or Set a Keyboard Shortcut**
For quick access, consider adding the app to your **Dock** or using a tool like **BetterTouchTool** or **Automator** to assign a keyboard shortcut.

---

## 🚀 Usage

1. Copy any text using `⌘ + C`.
2. Launch the Clipboard Saver app.
3. Check your **Desktop** — your clipboard content is now saved as a `.txt` file.
4. A notification will pop up confirming the save:
   - **Title:** Successful  
   - **Message:** Your clipboard has been copied to a file on your desktop.

---

## 🔒 Permissions & Security

Upon first use, macOS may request permissions:

- ✅ **Clipboard Access** — To read copied content.
- ✅ **Notifications** — To alert you of successful saves.

If permissions are denied initially, you can grant them via:  
**System Preferences → Security & Privacy → Privacy**

⚠️ **Privacy First:**  
This app **does not transmit** or store your clipboard data anywhere outside your local machine.

---

## 💡 Advanced Users: Behind the Scenes

The core functionality is powered by a simple **zsh** shell script:

```zsh
pbpaste > ~/Desktop/$(date +%Y%m%d%H%M%S)•txt;
```

### 💡 How It Works (In Detail)

This command:

- 📝 **Uses** `pbpaste` to grab clipboard contents.  
- 💾 **Saves** it as a `.txt` file on the **Desktop** with a timestamp.  
- 🔔 **Triggers** a macOS native **notification** confirming success.

---

## ⚖️ Compatibility

- 🖥️ **macOS Monterey (12.x)** and later  
- 🧠 Works seamlessly on **Intel** and **Apple Silicon (M1/M2)** Macs

---

## 🤝 Contributing

Want to enhance this app? 🚀  
Fork the repo, create a **feature branch**, and submit a **Pull Request**. Whether it’s adding new features, improving the UI, or squashing bugs—**contributions are always welcome**!

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 💾 Why Use Clipboard Saver?

Because sometimes, **pasting into Notes or TextEdit is just too many clicks**. This app lets you **capture ideas, code snippets, and links instantly** — all with **one click** and **zero friction**.

---

🚀 **Download it. Run it. Save everything.** 💾✨

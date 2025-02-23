📋 Clipboard Saver Automator App

A simple macOS Automator application that captures your current clipboard contents and saves it as a .txt file on your Desktop, timestamped for easy tracking. Upon successful save, it sends a notification confirming the operation.

🛠 Features
	•	✅ One-click clipboard saving
	•	✅ Saves as a .txt file with a timestamped filename
	•	✅ Instant desktop notifications after saving
	•	✅ No external dependencies — uses native macOS tools
	•	✅ Perfect for quick note-taking, code snippets, or links

⚡ How It Works
	1.	Run the app → (via double-click or shortcut)
	2.	Grabs your clipboard using pbpaste.
	3.	Saves the content as a .txt file to your Desktop with this format:

YYYYMMDDHHMMSS • txt

Example: 20250224123045 • txt

	4.	Sends a macOS notification confirming the save.

📂 Installation
	1.	Download the .dmg file from the Releases section.
	2.	Open the .dmg and drag the app into your Applications folder.
	3.	(Optional) Right-click → Open on the first run if macOS flags it as an unidentified developer.

🚀 Usage
	1.	Copy any text (using ⌘ + C).
	2.	Launch the app.
	3.	Check your Desktop — the clipboard is now saved!
	4.	You’ll see a “Successful” notification once done.

💡 Tip: Add the app to your Dock or set up a keyboard shortcut for quicker access.

🔒 Permissions

On first run, macOS may prompt you for permissions:
	•	✅ Clipboard Access → To read from your clipboard.
	•	✅ Notifications → To display success messages.

(If missed, go to System Preferences → Security & Privacy → Privacy to enable them.)

⚖️ Compatibility
	•	macOS Monterey (12.x) and newer
	•	Works on both Intel and Apple Silicon (M1/M2) Macs

🛡️ Security Notice

This app runs a basic shell script and does not send your clipboard data anywhere. The entire process runs locally on your machine.

🤝 Contributions

Feel free to fork this repository and submit pull requests for enhancements or bug fixes. 🎉

📄 License

This project is licensed under the MIT License — see the LICENSE file for details.

🖥️ Behind The Scenes

This app uses the following shell script:

pbpaste > ~/Desktop/$(date +%Y%m%d%H%M%S)•txt;

And a native macOS notification:
	•	Title: Successful
	•	Message: Your clipboard has been copied to a file on your desktop.

🚀 Happy Copying! 💾✨

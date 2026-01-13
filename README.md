🚀 Expo EAS Android Builder (Python UI)

A simple desktop UI tool built with Python (Tkinter) that allows you to run Expo EAS Android builds without using the command line.
Designed for non-interactive builds, automation, and local admin tools.

✨ Features

🖥️ Desktop UI (no terminal required)

📦 Builds Android apps using Expo EAS

🔐 Secure authentication using EXPO_TOKEN

📜 Live build logs inside the UI

🚫 Fully non-interactive (no CLI prompts)

⚡ Ideal for automation, kiosks, or admin tools

🛠️ Tech Stack

Python 3

Tkinter (built-in GUI library)

Expo CLI / EAS CLI

Git

📂 Project Structure
WebAppWrapperExpo/
│
├── eas_build_ui.py     # Python UI for EAS build
├── eas.json            # EAS configuration
├── app.json / app.config.js
├── package.json
└── README.md

✅ Prerequisites

Make sure the following are installed:

Python 3.9+

Node.js (LTS)

Expo CLI

EAS CLI

Git

Install Expo & EAS CLI:

npm install -g expo-cli eas-cli

🔐 Environment Variable Setup (IMPORTANT)

Do NOT hardcode your Expo token.

Set it once in your system environment variables:

Windows

Search → Environment Variables

Add new User Variable

Name: EXPO_TOKEN

Value: your_expo_token_here

Verify:

echo %EXPO_TOKEN%

🧱 One-Time Git Setup (Required by EAS)

EAS requires a Git repository.

Run this once inside the project directory:

git init
git add .
git commit -m "Initial commit"

▶ How to Run the UI
python eas_build_ui.py


A desktop window will open where you can:

Click Build Android App

View live EAS build logs

Receive success or error notifications

⚙️ Build Configuration

The tool runs the following command internally:

eas build --platform android --profile production --non-interactive


You can change the build profile inside the script if needed.

🧠 Why This Tool?

Avoids CLI input issues (stdin not readable)

Perfect for non-technical users

Works well with automated workflows

More reliable than running EAS from PHP or web servers

🔒 Security Notes

Never commit .env files or tokens

Always use environment variables

Add sensitive files to .gitignore

📌 Optional Enhancements (Future)

Progress bar

Build profile selector (dev / preview / prod)

Auto-fetch build URL

Auto-download .aab file

Dark mode

Convert to .exe using PyInstaller

📄 License

This project is for educational and internal use.
You may add an MIT or custom license if publishing publicly.

🙌 Author

Developed by Shin Duo

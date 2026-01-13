# 🚀 Web App Wrapper / Builder

A simple desktop UI tool built with Python (Tkinter) that enables the creation of Android mobile wrapper applications for web-based systems using Expo EAS, without requiring command-line interaction.

The tool is designed for non-interactive builds, automation, and local admin or installer tools, allowing users to package an existing web application into a deployable Android app.

## ✨ Features

- 🖥️ Desktop UI (no terminal required)
- 📦 Builds Android apps using Expo EAS
- 🔐 Secure authentication using EXPO_TOKEN
- 📜 Live build logs inside the UI
- 🚫 Fully non-interactive (no CLI prompts)
- ⚡ Ideal for automation, WebApp, or admin tools

## ✅ Prerequisites

### Make sure the following are installed:

- Python 3.9+
- Node.js (LTS)
- Expo CLI
- EAS CLI
- Git

### Install Expo & EAS CLI:

```
npm install -g expo-cli eas-cli
```

## 🔐 Environment Variable Setup (IMPORTANT)

Do NOT hardcode your Expo token.
Set it once in your system environment variables:

### Windows

1. Search → Environment Variables
2. Add new User Variable
   - Name: EXPO_TOKEN
   - Value: your_expo_token_here

```
echo %EXPO_TOKEN%
```

## 🧱 One-Time Git Setup (Required by EAS)

EAS requires a Git repository.

Run this once inside the project directory:

```
git init
git add .
git commit -m "Initial commit"
```

## ▶ How to Run the UI

```
python eas_build_ui.py
```

1. A desktop window will open where you can:
   - Click Build Android App
   - View live EAS build logs
   - Receive success or error notifications

## ⚙️ Build Configuration

The tool runs the following command internally:

```
eas build --platform android --profile production --non-interactive
```

## 🙌 Author

Developed by Julian Intila

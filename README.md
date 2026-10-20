# Firebase Manager

Firebase Manager is a fan-made Windows desktop GUI that makes common Firebase CLI tasks easier. Instead of typing every command manually, you can use a graphical interface to serve, deploy, and initialize Firebase projects.

Built with **Python**.

> ⚠️ **Beta notice:** Firebase Manager is currently in **BETA** and under active development, with frequent updates. Expect occasional bugs or breaking changes.

## Features

- **Serve locally:** Start local previews of Firebase Hosting projects and open them in your browser.
- **Deploy projects:** Deploy one or more Firebase Hosting projects and view live CLI output.
- **Initialize projects:** Run `firebase init` through the app for services such as Hosting, Functions, and Firestore.
- **Firebase login/logout:** Sign in using the official Firebase CLI in a terminal window; the app tracks login status.
- **Remember projects:** Project lists, names, and removals are saved in `%APPDATA%\FirebaseManager`.
- **Minimize to system tray:** Keep the app running while local servers remain active.

## Requirements

- **Windows 64-bit**
- A Firebase account and access to the Firebase projects you want to use ([Firebase Console](https://console.firebase.google.com/)).
- No separate Node.js or Firebase CLI installation is needed — both are bundled with the installer. They are only relevant if you need to troubleshoot (see step 8 below).

## Installation

1. **Node.js is already included.** Firebase Manager ships with its own bundled Node.js and Firebase CLI, so there's **nothing extra to install**. Just download the installer below. You only need to touch Node.js manually if you run into trouble (see the troubleshooting step near the end).
2. **Download and run the installer.** Grab `FirebaseManagerInstaller(v1.0.1).exe` from the [releases page](https://github.com/Ahmed76239/firebase-manager/releases/download/v1.0.1/FirebaseManagerInstaller.v1.0.1.exe) and run it. Windows may show an **Unknown publisher** warning because the installer isn't code-signed. Click **More info → Run anyway**.
3. **Log in to Firebase.** On first launch the app checks your login. Click **Login**. A real terminal window opens and runs `firebase login`. Sign in through the browser; the window closes by itself when done.
4. **Add your projects.** Go to the **+ Add existed project** tab and pick a folder that already contains a `firebase.json`. Give it a name and it appears in the Serve and Deploy tabs.
5. **Serve locally.** Tick one or more projects and click **Serve Selected**. Each project gets its own free port starting at 5000. Click **Open** to preview it in your browser.
6. **Deploy to Firebase.** Switch to the **Deploy project** tab, tick the projects you want, and click **Deploy Selected**. Output streams live into the Deploy log.
7. **Or initiate a brand-new project.** On the **Initiate project** tab, pick a folder, name, and type. The app opens a terminal running `firebase init` (and optionally `firebase deploy`) in the same window, then adds the project to your list automatically.
8. **Troubleshooting: reinstall Node.js & the Firebase CLI.** If Firebase commands fail or the app can't find the CLI, reinstall Node.js from [nodejs.org/en/download](https://nodejs.org/en/download) (LTS version), then open **Command Prompt** and run these three commands one at a time:

   ```bash
   npm uninstall -g firebase-tools
   npm cache clean --force
   npm install -g firebase-tools
   ```

   Once the last command finishes, restart Firebase Manager and try again.

## Download

The website advertises **Firebase Manager v1.0.1**, for **Windows 64-bit**.

Download the latest installer here:

[**Download Firebase Manager for Windows (.exe)**](https://github.com/Ahmed76239/firebase-manager/releases/download/v1.0.1/FirebaseManagerInstaller.v1.0.1.exe)

This link uses GitHub's `releases/latest/download` route, so it points to the named installer asset in the latest release.

## Important Notes

- Firebase Manager is a **fan-made, unofficial tool**. It is not affiliated with, endorsed by, or sponsored by Firebase or Google LLC.
- "Firebase" and the Firebase logo are trademarks of Google LLC, used only to describe what this tool interacts with. All rights belong to their respective owners.
- The app wraps the official Firebase CLI; it does not replace Firebase or bundle/modify Firebase itself.
- The installer is unsigned, so Windows SmartScreen may show a warning. Only proceed if you trust the installer.
- This tool is in **BETA mode**, still under development and frequently updated.
- This tool is built with the **Python** programming language.

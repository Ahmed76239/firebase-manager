# Firebase Manager

Firebase Manager is a fan-made Windows desktop GUI that makes common Firebase CLI tasks easier. Instead of typing every command manually, you can use a graphical interface to serve, deploy, and initialize Firebase projects.

Built with **Python**.

## Features

- **Serve locally:** Start local previews of Firebase Hosting projects and open them in your browser.
- **Deploy projects:** Deploy one or more Firebase Hosting projects and view live CLI output.
- **Initialize projects:** Run `firebase init` through the app for services such as Hosting, Functions, and Firestore.
- **Firebase login/logout:** Sign in using the official Firebase CLI in a terminal window; the app tracks login status.
- **Remember projects:** Project lists, names, and removals are saved in `%APPDATA%\FirebaseManager`.
- **Minimize to system tray:** Keep the app running while local servers remain active.

## Requirements

- **Windows 64-bit**
- **Node.js** (the LTS version is recommended)
- **Firebase CLI** (`firebase-tools`)
- A Firebase account and access to the Firebase projects you want to use [Firebase Console](https://console.firebase.google.com/).

## Installation

1. Install Node.js from [the official download page](https://nodejs.org/en/download).
2. Open a terminal and install the Firebase CLI globally:

   ```bash
   npm install -g firebase-tools
   ```

3. Download `Firebase Manager-Setup-1.0.1.exe` from the project's releases page.
4. Run the installer and launch Firebase Manager.
5. If Windows SmartScreen displays an **Unknown publisher** warning, the installer may be unsigned. Only proceed if you trust the installer.


## Getting Started

1. Open Firebase Manager.
2. Select **Login**. A terminal window runs `firebase login`; complete sign-in in the browser.
3. Add an existing project using the **+ Add existed project** tab. Select a folder containing `firebase.json` and give the project a name.
4. To preview a project, select it and click **Serve Selected**. Projects use available ports starting at `5000`; use **Open** to view the preview in your browser.
5. To deploy, open the **Deploy project** tab, select the projects, and click **Deploy Selected**.
6. To create a new Firebase project configuration, open **Initiate project**, choose a folder, name, and project type, then run `firebase init`. The app can optionally run `firebase deploy`.

## Download

The website advertises **Firebase Manager v1.0.1**, for **Windows 64-bit**.

Download the latest installer here:

[**Download Firebase Manager for Windows (.exe)**](https://github.com/Ahmed76239/firebase-manager/releases/download/v1.0.1/Firebase-Manager-Setup-1.0.1v.exe)

This link uses GitHub's `releases/latest/download` route, so it points to the named installer asset in the latest release.

## Important Notes

- Firebase Manager is a **fan-made, unofficial tool**. It is not affiliated with, endorsed by, or sponsored by Firebase or Google LLC.
- The app wraps the official Firebase CLI; it does not replace Firebase or bundle/modify Firebase itself.
- The Firebase CLI must be installed separately.
- The installer is described on the website as unsigned, so Windows SmartScreen may show a warning.
- Use the tool at your own risk. The publisher is not responsible for data loss or deployment mistakes.

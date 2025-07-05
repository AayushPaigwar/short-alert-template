# 🚨 Flutter Shorebird Patch Notifier Template

A GitHub Actions-based template for Flutter projects using [Shorebird](https://shorebird.dev). Automatically detects pushes that require patching and sends email alerts if no patch is created.


![Flutter](https://img.shields.io/badge/Flutter-Compatible-blue)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-blue)
[![Use Template](https://img.shields.io/badge/Use-This%20Template-brightgreen)](https://github.com/yourusername/flutter-shorealert-template/generate)



---

## 🧩 How It Works

- Watches for Flutter/Dart file changes
- Checks if Shorebird patch is created
- Sends alert if patch is missing

---

## ⚡ Quick Start

1. **Click “Use this template”** above ⤴️  
2. In your new repo:
   - Add `.shorebird/token.json` OR setup via GitHub Secrets:
     - `SHOREBIRD_TOKEN`
     - `EMAIL_USER` (e.g., your Gmail)
     - `EMAIL_PASSWORD` (App Password)

3. On push to `master` or `main`, the action runs and alerts on patch miss

---

## 🛠️ Requirements

- Flutter project with `shorebird.yaml`
- GitHub Secrets configured:
  - `SHOREBIRD_TOKEN`: From `shorebird login`
  - `EMAIL_USER`: Your email address
  - `EMAIL_PASSWORD`: Gmail app password (never your login password)

---

## 🤖 Included

- `.github/workflows/shorealert.yml` preconfigured
- Supports SMTP-based email alerting

---

## 🧪 Test It

Make a push with a `.dart` file change.  
If you forget to run `shorebird patch`, you’ll get an alert ✉️

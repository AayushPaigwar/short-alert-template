# 🚨 Flutter Shorebird Patch Notifier Template

A GitHub Actions-based template for Flutter projects using [Shorebird](https://shorebird.dev). Automatically detects Dart/YAML code pushes that require patching and sends email alerts if no patch is created.

![Flutter](https://img.shields.io/badge/Flutter-Compatible-blue)
![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-blue)
[![Use Template](https://img.shields.io/badge/Use-This%20Template-brightgreen)](https://github.com/yourusername/flutter-shorealert-template/generate)

---

## 🧩 How It Works

- Watches for `.dart` and `.yaml` file changes
- Checks if a Shorebird patch has been created
- Sends email alerts if patch is missing
- Fully automated via GitHub Actions

---

## ⚡ Quick Start

You can use this in **two ways**:

---

### 🟢 Option 1: Use This Template (Recommended for new projects)

1. Click the **[Use This Template](https://github.com/yourusername/flutter-shorealert-template/generate)** button above ⤴️
2. Create a new repository from it
3. Add GitHub Secrets (see below)
4. Push changes to `main` or `master` branch
5. Done! The action checks for patches on every push

---

### 🔧 Option 2: Add to Existing Flutter Project

1. Copy the file `.github/workflows/shorealert.yml` into your Flutter project repo  
2. Go to your repository’s:  
   **Settings → Secrets and variables → Actions**
3. Add the following secrets:

| Secret Name        | Description                                  |
|--------------------|----------------------------------------------|
| `SHOREBIRD_TOKEN`  | Token from `shorebird login`                 |
| `EMAIL_USER`       | Your SMTP-enabled email (e.g., Gmail)        |
| `EMAIL_PASSWORD`   | App password for the email (not main pwd)    |

4. Commit a Dart/YAML file change and push
5. If a patch isn’t created, you’ll receive an email alert ⚠️

---

## 🔐 GitHub Secrets Required

| Name              | Description                                  |
|-------------------|----------------------------------------------|
| `SHOREBIRD_TOKEN` | JSON token from Shorebird login (`shorebird login`) |
| `EMAIL_USER`      | Your sending email address                   |
| `EMAIL_PASSWORD`  | Email App Password (Gmail or SMTP app pass)  |

> 💡 Tip: Use [Gmail App Passwords](https://support.google.com/accounts/answer/185833) if you’re using Gmail.

---

## 📦 What's Included

- ✅ Preconfigured `.github/workflows/shorealert.yml`
- 🐦 Shorebird CLI setup and auth
- 📨 Automated email alerting via SMTP
- 💡 Smart commit diff logic for `.dart` and `.yaml` changes

---

## 🧪 Test It

1. Make a push to `main`/`master` branch with changes to a Dart/YAML file
2. Do **not** run `shorebird patch`
3. You’ll receive an email


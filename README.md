# ⚙️ nerv-actions

> Standardized CI/CD workflows for Maven projects — from commit → release, fully automated.

nerv-actions provides **reusable GitHub Actions workflows** to build, version, and release
Java (Maven) projects with **zero-friction automation**.

---

## 🚀 Features

* ✅ Build and test Maven projects
* ✅ Multi-module support
* ✅ Semantic versioning (commit-driven)
* ✅ Automatic Git tagging and GitHub Releases
* ✅ Publish artifacts to GitHub Packages
* ✅ Generated changelogs
* ✅ Reusable workflows across repositories

---

## 📦 Quick Start

```yaml
jobs:
  cd:
    uses: czetsuyatech/nerv-actions/.github/workflows/cd.yml@main
    with:
      javaVersion: '25'
    secrets:
      githubAppId: ${{ secrets.NERV_RELEASE_APP_ID }}
      githubAppPrivateKey: ${{ secrets.NERV_RELEASE_APP_PRIVATE_KEY }}
      githubToken: ${{ secrets.GH_PKG_TOKEN }}
```

📘 **Full setup guide →** https://github.com/czetsuyatech/nerv-actions/wiki/Getting-Started

---

## 📚 Documentation

* 🚀 Getting Started
  https://github.com/czetsuyatech/nerv-actions/wiki/Getting-Started

* 🧠 Workflow Overview
  https://github.com/czetsuyatech/nerv-actions/wiki/Workflow-Overview

* 🧪 Versioning & Commits
  https://github.com/czetsuyatech/nerv-actions/wiki/Versioning-and-Commits

* 🔐 Authentication
  https://github.com/czetsuyatech/nerv-actions/wiki/Authentication

👉 **Browse all docs:**
https://github.com/czetsuyatech/nerv-actions/wiki

---

## 🧩 nerv-actions Pro

Need more than Maven?

The Pro version extends support to:

* Node.js / npm
* Go
* Container pipelines
* Multi-repo orchestration

👉 Contact: **[czetsuya@gmail.com](mailto:czetsuya@gmail.com)**

---

## 🛠️ Consulting

Need a **production-grade CI/CD pipeline**?

I help teams with:

* Workflow design
* Monorepo / multi-repo setup
* Release automation
* Cloud + container integration

👉 Reach out: **[czetsuya@gmail.com](mailto:czetsuya@gmail.com)**

---

## 🏗️ Requirements

* Java 17+
* Maven
* GitHub Actions enabled

---

## 📄 License

Apache License 2.0

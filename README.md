# ⚙️ nerv-actions

> Standardized CI/CD workflows for Maven projects — from commit → release, fully automated.

A collection of **reusable GitHub Actions workflows** designed to simplify how Java (Maven) projects
are built, versioned, and released.

Built for consistency across repositories, with **semantic versioning**, **multi-module support**,
and **zero-friction releases** out of the box.

---

## 🚀 What You Get (Free)

Everything you need for a solid, production-ready Maven pipeline:

* ✅ Build and test Maven projects
* ✅ Multi-module support (parent + children)
* ✅ Semantic versioning (based on commit messages)
* ✅ Automatic Git tagging and GitHub Releases
* ✅ Publish artifacts to GitHub Packages
* ✅ Generated changelogs from commit history
* ✅ Reusable workflows across repositories

---

## 📦 Quick Start

Create a workflow in your repository:

```yaml
name: Continuous Delivery

on:
  push:
    branches: [ main ]
  release:
    types: [ published ]
  workflow_dispatch:
    inputs:
      environment:
        description: Environment
        type: environment
        required: true

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

---

## 🧠 How It Works

1. Analyzes commit history
2. Determines the next semantic version
3. Updates Maven project version
4. Builds and runs tests
5. Publishes artifacts
6. Creates Git tag + GitHub Release

---

## 🧪 Commit Convention (Required)

Semantic versioning is driven by commit messages:

```
feat: new feature        → minor version bump
fix: bug fix            → patch version bump
feat!: breaking change  → major version bump
```

> ⚠️ Commits must follow this format or no release will be generated.

---

## 🔐 Authentication

Default:

```
GITHUB_TOKEN
```

For cross-repository publishing or extended permissions:

```
GH_PKG_TOKEN
```

> ⚠️ Use a classic PAT if publishing across repositories.

---

## 📁 Output

Each run produces:

* 📌 Versioned Git tags (e.g. `1.2.0`)
* 📝 Auto-generated release notes
* 📦 Published Maven artifacts
* 📁 Build artifacts (JARs)

---

## 🧩 Need More Than Maven?

The workflows in this repository are focused on **Java/Maven use cases**.

If you're working across multiple stacks, **nerv-actions Pro** extends the same conventions to:

* Node.js / npm pipelines
* Python packaging and releases
* Container-based builds and deployments
* Cross-repository orchestration

All workflows are designed to be **consistent, composable, and drop-in compatible** with the free
edition.

> 💡 Start with Maven. Scale to multi-stack without redesigning your pipelines.

👉 👉 Get access to Pro workflows: **czetsuya@gmail.com**

---

## 🛠️ Need Help Setting This Up?

If you want to go beyond the basics, I offer services to help teams design and implement *
*production-grade CI/CD pipelines** using GitHub Actions.

This includes:

* Custom workflow design tailored to your architecture
* Multi-repository / monorepo pipeline setup
* Release automation and versioning strategy
* Integration with cloud, containers, and deployment targets
* Optimization for speed, reliability, and cost

Whether you're starting from scratch or improving an existing setup, the goal is to get you to a *
*clean, scalable pipeline**—fast.

👉 Request consulting: **[[czetsuya@gmail.com](mailto:czetsuya@gmail.com)]**

---

## 🏗️ Requirements

* Java 17+
* Maven
* GitHub Actions enabled

Optional:

* GitHub Packages (for publishing artifacts)

---

## 🔄 Roadmap

* Pre-release support (beta / rc)
* Improved changelog generation
* Additional ecosystem integrations

---

## 🤝 Contributing

Contributions are welcome. Open a PR or start a discussion.

---

## 📄 License

Apache License 2.0

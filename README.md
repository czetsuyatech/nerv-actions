# ⚙️ Reusable CI/CD Workflows for Maven Projects

> Standardized build, versioning, and release pipelines for Java projects.

A collection of reusable GitHub Actions workflows designed to simplify how Maven-based projects are built, tested, versioned, and released.

Supports **multi-module projects**, **semantic versioning**, and **automated releases** out of the box.

---

## 🚀 Features

* Build and test Maven projects
* Multi-module (parent + children) support
* Semantic versioning based on commit messages
* Automatic Git tagging and GitHub Releases
* Publish artifacts to GitHub Packages
* Generated changelogs from commit history
* Reusable workflows across repositories

---

## 📦 Quick Start

Create a workflow in your repository:

```yaml
name: Release

on:
  push:
    branches: [main]

jobs:
  release:
    uses: czetsuyatech/nerv-actions/.github/workflows/ci.yml@main
```

---

## 🧠 How It Works

1. Detects changes from commit history
2. Determines next version (semantic versioning)
3. Updates Maven project version
4. Builds and runs tests
5. Publishes artifacts
6. Creates Git tag and GitHub Release

---

## 🏗️ Requirements

* Java 17+
* Maven
* GitHub Actions enabled

**Optional**

* GitHub Packages (for publishing artifacts)

---

## 🔐 Authentication

By default, the workflow uses:

`GITHUB_TOKEN`

For cross-repository publishing or extended permissions:

`GH_PKG_TOKEN`

> ⚠️ Use a classic PAT if you need package publishing across repositories.

---

## 🧪 Commit Convention

Semantic versioning is driven by commit messages:

```
feat: adds new capability → minor version bump
fix: bug fix → patch version bump
feat!: breaking change → major version bump
```

> ⚠️ If commits don’t follow this format, no release will be generated.

---

## 📁 Example Output

* Tagged releases (e.g. `1.2.0`)
* Auto-generated release notes
* Published Maven artifacts
* Uploaded build artifacts (JARs)

---

## 🌱 Extensibility

This project focuses on **Java/Maven workflows**, but the same patterns can be applied across other stacks:

* Different build tools (Gradle, npm, etc.)
* Alternative packaging systems
* Language-specific release strategies

> 💡 Many teams eventually standardize these workflows across multiple ecosystems.

---

🧩 Extended Workflows

For teams working across multiple stacks, there is an extended set of workflows built on the same principles, covering additional ecosystems and use cases such as:

Node.js / npm pipelines
Python packaging and releases
Container-based builds and deployments
Cross-repository orchestration

These workflows follow the same conventions and are designed to integrate seamlessly with the structure provided here.

---

## 🔄 Roadmap

* Improved changelog generation
* Pre-release support (beta / rc)
* Additional ecosystem integrations

---

## 🤝 Contributing

Contributions are welcome. Feel free to open a PR or discussion.

---

## 📄 License

Apache License 2

# 🚀 Node.js Publish Kit

A reusable GitHub Actions workflow to test and publish Node.js packages to GitHub Packages using only the built-in `GITHUB_TOKEN`.

---

## 📦 Features

- ✅ Reusable workflow for GitHub Packages
- ✅ Automates testing and publishing on release
- ✅ No need for external secrets or tokens

---

## 🔧 How to Use in Your Project

In your Node.js project repository (e.g., `test-package`), create the following workflow file:

### `.github/workflows/release.yml`

```yaml
name: Release

on:
  release:
    types: [created]

jobs:
  publish:
    uses: ChandieFae/nodejs-publish-kit/.github/workflows/publish-gpr.yml@main
    with:
      node-version: '20'

{
  "name": "@your-username/your-package",
  "version": "1.0.0",
  "publishConfig": {
    "registry": "https://npm.pkg.github.com/"
  }
}

nodejs-publish-kit/
└── .github/
    └── workflows/
        └── publish-gpr.yml

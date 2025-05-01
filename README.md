# nodejs-publish-kit

# 🚀 Node.js Publish Kit

This repo contains a **reusable GitHub Actions workflow** for testing and publishing Node.js packages to **GitHub Packages** using only the built-in `GITHUB_TOKEN`.

---

## 🔁 How to Use in Your Project

In your own Node.js project repo (like `test-package`), create this workflow file:

`.github/workflows/release.yml`

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


nodejs-publish-kit/.github/workflows/publish-gpr.yml

✅ Reusable workflow for GitHub Packages
✅ Instructions for using the workflow

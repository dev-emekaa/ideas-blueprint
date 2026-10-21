# ideas-blueprint

**A founder's kit for picking a product worth building and shaping it into a Product Brief, a PRD and a logo.**

This repo is the source of the product. `folder/` holds exactly what buyers download, and a release turns it into a zip.

---

## What's in the repo

```
folder/                          the product: exactly what goes into the zip
  README.md                      the buyer's guide
  1-finding-ideas.md
  2-product-brief-and-prd.md
  3-logo-prompt.md
.github/workflows/release.yml    builds the zip whenever a version tag is pushed
```

---

## Releasing a version

Every release is a version tag. Pushing one builds the zip from `folder/` and publishes it on the repo's **Releases** page.

```bash
git add -A
git commit -m "Describe the change"
git push
git tag v1.1.0              # the next version number
git push origin v1.1.0
```

About a minute later, open **Releases → v1.1.0 → Assets** and download `ideas-blueprint-v1.1.0.zip`. That is the file to share or sell. The **Source code** archives on the same page are this private repo, never the product.

**Version numbers:** patch (`v1.0.1`) for fixes and wording, minor (`v1.1.0`) for new or reworked content, major (`v2.0.0`) for a restructure.

**One source.** Edit files only here, never in a downloaded copy, and always share the latest release. That way every zip comes from the same files and nothing drifts.

---

**License** proprietary — all rights reserved.

# CLAUDE.md — Rytech Signature Assets

## Repository Overview

This repository is a **brand asset store** for **Rytech Support** (rytechsupport.co.uk). It holds the official logo and signature image files used across email signatures, documents, websites, and other branded materials. There is no build system, package manager, or source code — the repository is purely a versioned collection of static image assets.

## Repository Structure

```
rytech-signature-assets/
└── RytechFull.png   # Full Rytech Support logo (1000×494 px, RGBA PNG)
```

### Current Assets

| File | Dimensions | Format | Description |
|---|---|---|---|
| `RytechFull.png` | 1000 × 494 px | PNG (RGBA) | Full colour Rytech Support logo — blue "R" icon + "rytech support" wordmark in a rounded-rectangle border |

## Brand Identity

- **Primary colour**: Cyan/teal blue (`#1da1c8` approximately) — used for the "R" icon and the rounded border
- **Secondary colour**: Black — used for the "ytech" part of the wordmark
- **Accent colour**: Dark/charcoal — used for "support" in a lighter weight
- **Logo style**: Geometric sans-serif; the oversized "R" extends left of the bordered wordmark panel
- **Background**: Transparent (RGBA) so the logo composites cleanly onto any background

## Naming Conventions

- File names use **PascalCase** with no spaces: `RytechFull.png`
- Follow the existing pattern when adding variants:
  - `RytechFull` — full lockup (icon + wordmark)
  - `RytechIcon` — icon only (if added)
  - `RytechWordmark` — text only (if added)
  - Append a suffix for colour variants: `RytechFullWhite.png`, `RytechFullDark.png`
  - Append dimensions only if multiple sizes are stored: `RytechFull_512.png`

## Adding or Updating Assets

1. Export assets at the **highest resolution needed** (minimum 1000 px on the longest side for logos).
2. Use **PNG with transparency (RGBA)** for logos; use JPEG only for photographic assets with no transparency requirement.
3. Do **not** commit working files (`.ai`, `.psd`, `.sketch`, `.fig`) to this repository — store them in a separate design source repository or a shared design tool.
4. Commit with a clear message describing the asset and any change, e.g.:
   ```
   Add white-on-transparent variant of full logo (RytechFullWhite.png)
   ```
5. Keep file sizes reasonable — run `pngcrush` or `oxipng` before committing large PNG files to reduce size without quality loss.

## Git Workflow

- **Default branch**: `main`
- **Feature/update branches**: use descriptive names, e.g. `add-dark-logo-variant` or `update-full-logo-2025`
- There are no CI pipelines, tests, or lint steps for this repository.
- Direct commits to `main` are acceptable for straightforward asset additions; open a branch and PR for anything that replaces or removes existing assets.

## Guidelines for AI Assistants

- This repo contains **binary image files only** — do not attempt to read or edit PNG/image files as text.
- Do **not** delete or overwrite existing assets without explicit instruction; they may be referenced by live email signatures or external systems.
- When asked to add a new asset, confirm the filename, dimensions, and format before committing.
- When asked to update an existing asset, prefer adding a new versioned file alongside the original rather than replacing it in-place, unless replacement is explicitly requested.
- Commit messages should be concise and describe the asset, not the tooling (e.g. "Add monochrome logo variant" not "Run asset pipeline").
- There are no tests to run and no build steps to execute for this repository.

## Contact / Ownership

- **Organisation**: Rytech Support
- **Contact**: daniel@rytechsupport.co.uk
- **Repository**: RytechSupport14/rytech-signature-assets

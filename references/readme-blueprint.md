# README Blueprint

Use this reference when drafting or restructuring a GitHub README that should feel like a polished project home page.

## High-Star Repository Patterns

Popular repositories such as React, Next.js, Vite, shadcn/ui, Bootstrap, and VS Code tend to share these moves:

1. Open with a recognizable project name and one crisp sentence.
2. Give the reader a direct path to success: docs link, install command, quick example, or download.
3. Keep feature claims compact and specific.
4. Use screenshots, previews, or examples when the project is visual or UI-facing.
5. Separate "install", "usage", "development", and "contributing" so readers can scan by intent.
6. Place governance information near the end: contributing, code of conduct, security, acknowledgements, license.
7. Link outward instead of copying large docs into the README.

## Centered Brand Header

Use this pattern when the user asks for a Next.js-like README opening or a polished branded first screen:

Before using it, confirm the repo has a real logo asset. If no logo exists, remind the user that this layout needs a logo and ask them to provide one. Do not silently invent a placeholder logo.

```markdown
<p align="center">
  <img src="assets/logo.svg" alt="Project logo" width="160">
</p>

<h1 align="center">Project Name</h1>

<p align="center">
  One crisp sentence describing what the project does.
</p>

<p align="center">
  <a href="#getting-started"><img alt="Getting Started" src="https://img.shields.io/badge/GETTING_STARTED-black?style=for-the-badge"></a>
  <img alt="License" src="https://img.shields.io/badge/LICENSE-MIT-64BC4B?style=for-the-badge">
</p>
```

Keep this header compact. Do not let badges replace the install or usage sections.

## Dynamic GitHub Badge Strip

Use this when the user asks for synced stars, repository stats, or the BongoCat-style badge row. First resolve the GitHub slug as `OWNER/REPO` from `git remote -v`, package metadata, homepage links, or existing README links. If the slug is unknown, ask the user for it instead of inventing counts.

```markdown
<p align="center">
  <a href="https://github.com/OWNER/REPO/stargazers">
    <img alt="GitHub stars" src="https://img.shields.io/github/stars/OWNER/REPO?style=for-the-badge&label=STARS&color=EAC800&labelColor=555555">
  </a>
  <a href="https://github.com/OWNER/REPO/network/members">
    <img alt="GitHub forks" src="https://img.shields.io/github/forks/OWNER/REPO?style=for-the-badge&label=FORKS&color=8AD900&labelColor=555555">
  </a>
  <a href="https://github.com/OWNER/REPO/issues">
    <img alt="GitHub issues" src="https://img.shields.io/github/issues/OWNER/REPO?style=for-the-badge&label=ISSUES&color=168DE2&labelColor=555555">
  </a>
  <a href="https://github.com/OWNER/REPO/pulls">
    <img alt="GitHub pull requests" src="https://img.shields.io/github/issues-pr/OWNER/REPO?style=for-the-badge&label=PULLS&color=FF6F2C&labelColor=555555">
  </a>
</p>

<p align="center">
  <img alt="License" src="https://img.shields.io/github/license/OWNER/REPO?style=flat-square&label=license&color=64BC4B&labelColor=555555">
  <img alt="Release" src="https://img.shields.io/github/v/release/OWNER/REPO?style=flat-square&label=version&color=168DE2&labelColor=555555">
  <img alt="Downloads" src="https://img.shields.io/github/downloads/OWNER/REPO/total?style=flat-square&label=downloads&color=999999&labelColor=555555">
</p>
```

Use only badges that match real repo facts. For example, include Windows, macOS, or Linux badges only when the project actually supports them.

## Technology Stack Badge Strip

Use this when the user asks for tech stack badges or when a polished centered header would benefit from a stack row. First infer the stack from real files: `package.json`, lockfiles, `pyproject.toml`, `requirements.txt`, `Cargo.toml`, `go.mod`, `*.csproj`, `Dockerfile`, CI files, or existing docs. If the stack is unclear, ask the user for the technologies instead of guessing.

```markdown
<p align="center">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
  <img alt="React" src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB">
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white">
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white">
  <img alt="Tailwind CSS" src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">
</p>
```

If the GitHub slug is known, a dynamic top-language badge can join the stack row:

```markdown
<img alt="Top language" src="https://img.shields.io/github/languages/top/OWNER/REPO?style=for-the-badge&label=TOP_LANGUAGE&color=3178C6&labelColor=555555">
```

Keep stack badges factual and selective. Five to eight badges is usually enough.

## Core Layout

Use this order for most full README rewrites:

1. Title
2. Optional language links
3. One-line summary
4. Preview, screenshot, or minimal example
5. Highlights
6. Installation
7. Usage or quick start
8. Documentation or examples
9. Release or download section
10. Development
11. Contributing
12. Contact
13. Acknowledgements
14. License

## Project-Specific Layouts

Library/framework:

1. Title and summary
2. Install command
3. Quick example
4. Documentation and examples
5. Compatibility notes
6. Contributing and license

Desktop/mobile app:

1. Title and summary
2. Screenshot or preview
3. Feature highlights
4. Download or install
5. Usage
6. FAQ or troubleshooting
7. Development, contact, and license

CLI/tooling:

1. Title and summary
2. Install command
3. Quick start
4. Command examples
5. Configuration
6. Development, contribution, and license

Codex skill/plugin:

1. Title and summary
2. What it helps with
3. When to use it
4. What the skill contains
5. Installation path
6. Validation command
7. Contact and license

## Pattern Borrowed From Clash Verge

- Put language navigation near the top.
- Keep the opening short and visual.
- Put installer or release links in a later section, not the first screen.
- Use a clean hierarchy and short section titles.

## User Preferences To Preserve

- Use blue, clickable Markdown links for language switching and navigation.
- Keep the download link near the bottom unless explicitly told otherwise.
- Prefer Chinese + English when the repo is meant for both audiences.
- Avoid noisy promotional blocks.
- Preserve user-provided contact details exactly.
- Place user-provided signatures or personal marks exactly where requested.
- Remind the user when a requested centered brand header has no logo asset available.
- Add technology stack badges when the user asks for badges in the BongoCat/Next.js-style header.

## Good Defaults

- If both languages are needed, choose either one README with paired sections or two README files plus a small switcher.
- If screenshots exist, show them early.
- If the repo ships installers, make the release page the primary download target.
- Use a centered HTML block for a bottom signature image:

```markdown
<p align="center">
  <img src="assets/capwitf.png" alt="Capwitf signature" width="240">
</p>
```

## Quality Checklist

- The first screen answers "what is this?" and "why would I use it?"
- Install and usage commands are copy-ready.
- Every link either points to an existing local file or a known external target.
- Visual assets use stable relative paths.
- No unsupported claims, fake badges, or invented compatibility promises.
- The bottom sections do not distract from the main usage path.

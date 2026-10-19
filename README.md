<p align="center">
  <img src="assets/write-readme-logo.svg" alt="Write Readme logo" width="160">
</p>

<h1 align="center">Write Readme</h1>

<p align="center">
  A Codex skill for creating and polishing GitHub README files with a clean project-homepage structure.
</p>

<p align="center">
  <a href="#中文"><img alt="中文" src="https://img.shields.io/badge/%E8%AF%AD%E8%A8%80-%E4%B8%AD%E6%96%87-black?style=for-the-badge"></a>
  <a href="#english"><img alt="English" src="https://img.shields.io/badge/language-English-black?style=for-the-badge"></a>
  <img alt="Codex Skill" src="https://img.shields.io/badge/Codex-Skill-0A7AFF?style=for-the-badge">
  <img alt="README" src="https://img.shields.io/badge/README-Writer-20B2AA?style=for-the-badge">
</p>

<p align="center">
  <img alt="Markdown" src="https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white">
  <img alt="GitHub" src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white">
  <img alt="shields.io" src="https://img.shields.io/badge/shields.io-000000?style=for-the-badge&logo=shieldsdotio&logoColor=white">
</p>

## 中文

`write-readme` 帮你把仓库首页整理成更像成熟开源项目的 README：标题清楚、价值一句话说透、预览和用法靠前，下载、贡献、许可证和联系信息放在合适的位置。

## 适合处理

- 从零创建 README
- 重写或精简已有 README
- 调整中英文 README 结构
- 同步项目名、安装命令、下载链接、发布链接
- 增加截图、预览、FAQ、贡献、许可证和联系信息

## 结构特点

- 参考 React、Next.js、Vite、shadcn/ui 等高星仓库的组织方式
- 默认保留顶部语言导航和清晰的章节层级
- 每份 README 默认在顶部加入紧凑徽章行，至少包含真实的 Markdown 格式徽章
- 区分库、应用、CLI、Codex skill 等不同项目类型
- 避免伪造徽章、命令、截图、下载地址和兼容性声明
- 在仓库地址已知时，使用 shields.io 动态同步 stars、forks、issues、pulls、release、downloads 等徽章
- 如果需要同步 GitHub 统计但缺少 `OWNER/REPO`，会提醒你提供仓库路径
- 从真实项目文件识别技术栈，并生成语言、框架、运行时、包管理器、平台等技术栈徽章
- 如果需要技术栈徽章但无法确认技术栈，会提醒你补充信息
- 支持把用户指定的联系方式与签名放在 README 底部

## 动态徽章模板

把 `OWNER/REPO` 替换成真实 GitHub 仓库路径后，下面这些徽章会自动同步仓库数据：

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
```

## 技术栈徽章模板

确认项目真实技术栈后，可以加入类似下面的徽章：

```markdown
<p align="center">
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
  <img alt="React" src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB">
  <img alt="Next.js" src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white">
  <img alt="Node.js" src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white">
  <img alt="Tailwind CSS" src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white">
</p>
```

## 安装

将本目录放到 Codex skills 目录中：

```powershell
C:\Users\T\.codex\skills\write-readme
```

或保持当前目录，并在需要时通过路径引用这个 skill。

## 使用

在 Codex 中提出 README 相关任务即可触发，例如：

```text
Use $write-readme to rewrite this repository README.
```

```text
用 $write-readme 优化 README，保留下载链接在底部。
```

## 文件结构

```text
write-readme/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
├── assets/
│   ├── capwitf.png
│   └── write-readme-logo.svg
└── references/
    └── readme-blueprint.md
```

## 校验

可以使用 Codex 自带的 skill 校验脚本检查元数据：

```powershell
python C:\Users\T\.codex\skills\.system\skill-creator\scripts\quick_validate.py C:\Users\T\Desktop\write-readme
```

## English

`write-readme` helps Codex create or polish repository READMEs that feel like mature GitHub project home pages: clear title, crisp summary, early preview or usage path, and well-placed release, contribution, license, and contact sections.

## Good For

- Creating a README from scratch
- Rewriting or simplifying an existing README
- Structuring bilingual Chinese and English READMEs
- Updating project names, install commands, download links, and release URLs
- Adding screenshots, previews, FAQs, contribution notes, licenses, and contact details

## What It Adds

- README structure inspired by high-star repositories such as React, Next.js, Vite, and shadcn/ui
- Clear section ordering for libraries, apps, CLIs, and Codex skills
- A compact badge row in every README by default, including at least a factual Markdown format badge
- Strong defaults for language links, previews, install commands, usage, releases, and license sections
- Guardrails against invented badges, commands, screenshots, URLs, or compatibility claims
- Dynamic shields.io GitHub badges for stars, forks, issues, pull requests, releases, and downloads when the GitHub `OWNER/REPO` is known
- A reminder to provide the repository path when synced GitHub stats are requested but cannot be resolved
- Technology stack badges for confirmed languages, frameworks, runtimes, package managers, and platforms
- A reminder to provide stack details when tech stack badges are requested but cannot be verified
- Support for user-specified contact details and bottom-centered signature assets

## Contact

Email: [capwitf@outlook](mailto:capwitf@outlook)

<p align="center">
  <img src="assets/capwitf.png" alt="Capwitf signature" width="240">
</p>

## 许可证

本项目采用 [MIT License](LICENSE)。

## License

This project is licensed under the [MIT License](LICENSE).

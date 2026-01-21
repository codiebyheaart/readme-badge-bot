# 🏷️ README Badge Bot

<!-- BADGES:START -->
![Build](https://img.shields.io/badge/Build-passing-brightgreen?logo=github) ![Version](https://img.shields.io/badge/Version-1.0.0-blue?logo=npm) ![License](https://img.shields.io/badge/License-MIT-green) ![GitHub Actions](https://github.com/username/readme-badge-bot/workflows/CI/badge.svg?branch=main) ![Last Commit](https://img.shields.io/github/last-commit/username/readme-badge-bot) ![Issues](https://img.shields.io/github/issues/username/readme-badge-bot) ![Stars](https://img.shields.io/github/stars/username/readme-badge-bot?style=social)
<!-- BADGES:END -->

**Automatically generate and update beautiful badges in your README.md using GitHub Actions!**

## 🌟 Overview

README Badge Bot is a lightweight, automated solution that keeps your project's README badges up-to-date without manual intervention. Perfect for open-source projects, it displays real-time information about build status, test coverage, version, license, and more!

### ✨ Features

- ✅ **Automatic Badge Updates** - Runs on every push, pull request, or on a schedule
- 📊 **Multiple Badge Types** - Build status, version, coverage, license, stars, issues, and more
- 🔧 **Highly Configurable** - Customize badge placement, colors, and content
- 🚀 **Zero Maintenance** - Set it up once and forget about it
- 🐛 **Framework Agnostic** - Works with any Node.js project
- 🌐 **Universal Use Case** - Useful for any GitHub repository

## 💻 Suggested Repository Name

**`readme-badge-bot`** - Clear, descriptive, and SEO-friendly!

Alternative names:
- `auto-badge-updater`
- `github-badge-generator`
- `readme-shield-bot`
- `badge-automation-action`

## 🚀 Quick Start

### 1. Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/readme-badge-bot.git
cd readme-badge-bot

# Install dependencies
npm install
```

### 2. Add Badge Markers to Your README

Add these HTML comments where you want badges to appear:

```markdown
# Your Project Name

<!-- BADGES:START -->
<!-- BADGES:END -->

Your project description...
```

### 3. Set Up GitHub Actions

Copy the workflow file to your repository:

```bash
mkdir -p .github/workflows
cp .github/workflows/update-badges.yml .github/workflows/
```

### 4. Configure (Optional)

Create a `.badgerc.json` file in your project root:

```json
{
  "readmePath": "README.md",
  "packageJsonPath": "package.json",
  "coveragePath": "coverage/coverage-summary.json",
  "badgeSection": "<!-- BADGES:START -->",
  "badgeEndSection": "<!-- BADGES:END -->"
}
```

### 5. Push and Watch the Magic! ✨

```bash
git add .
git commit -m "Add README Badge Bot"
git push origin main
```

The GitHub Action will automatically run and update your badges!

## 🛠️ How It Works

1. **Trigger**: The workflow runs on push, pull request, or schedule (daily at midnight)
2. **Analyze**: Reads your `package.json`, test coverage, and repository metadata
3. **Generate**: Creates beautiful shields.io badges with current data
4. **Update**: Automatically commits changes to your README.md
5. **Repeat**: Keeps badges fresh with every update!

## 🎯 Supported Badges

| Badge Type | Description | Source |
|------------|-------------|--------|
| Build Status | CI/CD pipeline status | GitHub Actions |
| Version | Current package version | package.json |
| Coverage | Test coverage percentage | Coverage reports |
| License | Project license | package.json |
| Node Version | Required Node.js version | package.json engines |
| Last Commit | Most recent commit date | GitHub API |
| Issues | Open issues count | GitHub API |
| Stars | Repository stars | GitHub API |
| Forks | Repository forks | GitHub API |

## 📚 Usage Examples

### Run Locally

```bash
# Generate badges manually
node src/badge-generator.js

# With custom configuration
README_PATH=docs/README.md node src/badge-generator.js
```

### Use in Your Project

```javascript
const BadgeGenerator = require('./src/badge-generator');

const generator = new BadgeGenerator({
  readmePath: 'README.md',
  packageJsonPath: 'package.json'
});

await generator.updateReadme();
```

## 🔧 Configuration Options

| Option | Default | Description |
|--------|---------|-------------|
| `readmePath` | `README.md` | Path to README file |
| `packageJsonPath` | `package.json` | Path to package.json |
| `coveragePath` | `coverage/coverage-summary.json` | Path to coverage file |
| `badgeSection` | `<!-- BADGES:START -->` | Start marker |
| `badgeEndSection` | `<!-- BADGES:END -->` | End marker |

## 🌐 Use Cases for Everyone

- **Open Source Maintainers**: Show project health at a glance
- **Development Teams**: Display CI/CD status and code quality
- **Portfolio Projects**: Make your GitHub profile stand out
- **Learning Projects**: Demonstrate best practices
- **Documentation Sites**: Keep docs synchronized with code
- **API Libraries**: Show version and compatibility info

## 📝 Workflow Triggers

The badge updater runs automatically:

- ✅ On every push to `main`, `master`, or `develop` branches
- ✅ On pull requests to main branches
- ✅ Daily at midnight (UTC) via cron schedule
- ✅ Manually via workflow dispatch

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Your Name** - Initial work

## 🚀 Roadmap

- [ ] Support for Python projects (requirements.txt, setup.py)
- [ ] Custom badge templates
- [ ] Badge positioning options (top, bottom, custom)
- [ ] Integration with codecov, coveralls
- [ ] Support for monorepos
- [ ] Custom badge colors and styles
- [ ] Slack/Discord notifications on badge updates

## ❓ FAQ

**Q: Will this work with private repositories?**  
A: Yes! Just ensure your workflow has the correct permissions.

**Q: Can I customize badge colors?**  
A: Yes, modify the `createBadge()` method in `badge-generator.js`.

**Q: Does it work with other languages besides Node.js?**  
A: Currently optimized for Node.js, but you can adapt it for Python, Ruby, etc.

**Q: Will it create infinite commit loops?**  
A: No! The workflow uses `[skip ci]` in commit messages to prevent loops.

## 💬 Support

If you have questions or need help:

- 🐛 [Open an issue](https://github.com/yourusername/readme-badge-bot/issues)
- ⭐ Star this repo if you find it useful!
- 👁️ Watch for updates

## 🎉 Acknowledgments

- [Shields.io](https://shields.io/) for providing awesome badge generation
- [GitHub Actions](https://github.com/features/actions) for automation platform
- The open-source community for inspiration

---

**Made with ❤️ and automated with GitHub Actions**

<!-- BADGES:START -->
<!-- BADGES:END -->

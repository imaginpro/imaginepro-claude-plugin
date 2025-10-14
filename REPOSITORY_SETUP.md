# GitHub Repository Setup Guide

Complete guide for configuring the GitHub repository settings.

## Repository Description

**Short Description (160 characters max for GitHub):**
```
Professional AI image and video generation plugin for Claude Code. Create web assets, UI components, marketing materials, and videos with specialized agents.
```

**Alternative Shorter Version (100 characters):**
```
AI image & video generation for Claude Code. Specialized agents for web, UI/UX, marketing, and video.
```

## Repository Topics/Tags

Add these topics to improve discoverability:

**Primary Topics:**
- `claude-code`
- `claude-code-plugin`
- `ai`
- `image-generation`
- `video-generation`

**Feature Topics:**
- `artificial-intelligence`
- `creative-tools`
- `web-development`
- `ui-design`
- `marketing`
- `design-system`

**Technology Topics:**
- `mcp-server`
- `model-context-protocol`
- `imaginepro`
- `prompt-engineering`

**Suggested Full Tag List:**
```
claude-code, claude-code-plugin, ai, image-generation, video-generation,
artificial-intelligence, creative-tools, web-development, ui-design, marketing,
design-system, mcp-server, model-context-protocol, imaginepro, prompt-engineering
```

## About Section Configuration

### Website
```
https://imaginepro.ai
```

### Description
Use the short description above.

### Topics
Use the tag list above (GitHub allows up to 20 topics).

## Repository Settings

### General Settings

**Default branch:** `main` ✓

**Features to Enable:**
- ✅ Issues (for bug reports and feature requests)
- ✅ Discussions (for community Q&A and feedback)
- ✅ Projects (optional - for roadmap tracking)
- ❌ Wiki (not needed - documentation is in repo)
- ❌ Sponsorships (unless you want to enable GitHub Sponsors)

**Pull Requests:**
- ✅ Allow squash merging
- ✅ Allow merge commits
- ✅ Allow rebase merging
- ✅ Automatically delete head branches

### Discussion Categories

Create these categories in Discussions:

1. **General** - General discussion about the plugin
2. **Q&A** - Questions and answers
3. **Ideas** - Feature requests and suggestions
4. **Show and Tell** - Share your creations made with the plugin
5. **Announcements** - Updates and releases (admin only)

### Issue Templates

Create these issue templates in `.github/ISSUE_TEMPLATE/`:

**1. Bug Report**
```yaml
name: Bug Report
about: Report a bug or issue with the plugin
title: '[BUG] '
labels: bug
assignees: ''
```

**2. Feature Request**
```yaml
name: Feature Request
about: Suggest a new feature or enhancement
title: '[FEATURE] '
labels: enhancement
assignees: ''
```

**3. Prompt Contribution**
```yaml
name: Prompt Contribution
about: Submit a new prompt to the library
title: '[PROMPT] '
labels: prompt-library
assignees: ''
```

**4. Documentation Improvement**
```yaml
name: Documentation Improvement
about: Suggest improvements to documentation
title: '[DOCS] '
labels: documentation
assignees: ''
```

### Labels

Create these labels for issues and PRs:

**Type Labels:**
- `bug` (red) - Something isn't working
- `enhancement` (blue) - New feature or request
- `documentation` (green) - Documentation improvements
- `prompt-library` (purple) - Prompt library additions
- `workflow` (teal) - Workflow guide improvements
- `example` (yellow) - Example project additions

**Priority Labels:**
- `priority-high` (red)
- `priority-medium` (orange)
- `priority-low` (yellow)

**Status Labels:**
- `good-first-issue` (green) - Good for newcomers
- `help-wanted` (blue) - Extra attention needed
- `wontfix` (white) - This will not be worked on
- `duplicate` (gray) - This issue or PR already exists

### README.md Badges

Add these badges to the top of README.md:

```markdown
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Plugin-5865F2)](https://docs.claude.com/en/docs/claude-code)
[![GitHub release](https://img.shields.io/github/v/release/imaginpro/imaginepro-claude-plugin)](https://github.com/imaginpro/imaginepro-claude-plugin/releases)
[![GitHub stars](https://img.shields.io/github/stars/imaginpro/imaginepro-claude-plugin)](https://github.com/imaginpro/imaginepro-claude-plugin/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/imaginpro/imaginepro-claude-plugin)](https://github.com/imaginpro/imaginepro-claude-plugin/issues)
```

## Social Preview Image

Create a social preview image (1200x630 pixels) showing:
- Plugin name and logo
- Key features (4 agents, 5 commands)
- "For Claude Code" branding
- ImaginePro branding

**Prompt for Social Preview:**
```
/imagine-pro GitHub repository social preview image for ImaginePro Claude Code
Plugin, modern tech aesthetic, shows "4 Specialized Agents" and "5 Smart Commands",
purple #7C3AED and blue #2563EB brand colors, clean professional design, 1200x630
pixels, includes plugin icon, "Claude Code Plugin" text, modern SaaS marketing
style, high quality professional
```

Upload to: Repository Settings → Options → Social preview

## Release Configuration

### First Release (v1.0.0)

Create a release with:

**Tag:** `v1.0.0`

**Release Title:** `v1.0.0 - Initial Release`

**Release Notes:**
```markdown
# 🎉 Initial Release: ImaginePro Claude Code Plugin v1.0.0

Professional AI image and video generation directly within Claude Code.

## ✨ Features

### 4 Specialized Agents
- 🌐 **Web Asset Producer** - Hero images, backgrounds, web-optimized assets
- 🎨 **UI/UX Asset Generator** - Icons, illustrations, design system components
- 📱 **Marketing Creative Specialist** - Ads, social media, campaign materials
- 🎬 **Video Workflow Director** - Motion content and video animations

### 5 Smart Commands
- `/imagine-pro` - Intelligent generation with prompt guidance
- `/upscale-it` - Quick production-quality enhancement
- `/vary-it` - Smart variations and refinements
- `/video-flow` - Complete video workflow automation
- `/imagine-guide` - Interactive learning and best practices

## 📚 Documentation

- Complete workflow guides for Web, UI/UX, Marketing, and Video
- Extensive prompt libraries with hundreds of ready-to-use prompts
- Real-world project walkthroughs (SaaS landing page, Mobile app design system)
- Comprehensive troubleshooting and quick start guides

## 🚀 Installation

```bash
# Add the ImaginePro marketplace
/plugin marketplace add imaginpro/claude-marketplace

# Install the plugin
/plugin install imaginepro

# Set your API key
export IMAGINEPRO_API_KEY="sk-your-api-key-here"
```

Get your free API key at [imaginepro.ai](https://imaginepro.ai)

## 📖 Getting Started

Check out the [Quick Start Guide](docs/quick-start.md) to begin creating professional visual assets in minutes!

## 🙏 Credits

Built with the [Model Context Protocol](https://modelcontextprotocol.io) and [ImaginePro API](https://imaginepro.ai).

---

**Full Changelog**: https://github.com/imaginpro/imaginepro-claude-plugin/commits/v1.0.0
```

## Security

### Security Policy

Create `.github/SECURITY.md`:

```markdown
# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability in the ImaginePro Claude Code Plugin,
please report it to us privately.

**Do NOT create a public GitHub issue for security vulnerabilities.**

Instead, please email: security@imaginepro.ai

We will acknowledge your email within 48 hours and provide a detailed response
within 7 days indicating the next steps in handling your report.

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |

## Security Best Practices

When using this plugin:

- Never commit your `IMAGINEPRO_API_KEY` to version control
- Use environment variables for API keys
- Keep your API keys private and rotate them regularly
- Review the plugin code before installation if you have security concerns
```

## Quick Setup Checklist

- [ ] Set repository description
- [ ] Add repository topics/tags
- [ ] Set website URL (https://imaginepro.ai)
- [ ] Enable Issues and Discussions
- [ ] Create Discussion categories
- [ ] Create issue templates (optional - can wait for feedback)
- [ ] Create labels
- [ ] Generate and upload plugin icon
- [ ] Create social preview image
- [ ] Create v1.0.0 release
- [ ] Add badges to README
- [ ] Create SECURITY.md

---

**Priority Setup Steps:**
1. Description and topics (5 minutes) - IMPORTANT for discoverability
2. Enable Issues and Discussions (1 minute)
3. Create first release v1.0.0 (5 minutes)
4. Generate icon and social preview (15 minutes when you have time)

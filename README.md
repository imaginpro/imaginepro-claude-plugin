# ImaginePro Claude Code Plugin

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Plugin-5865F2)](https://docs.claude.com/en/docs/claude-code)

**Professional AI image and video generation without leaving Claude Code.** Generate web assets, UI components, marketing materials, and videos with specialized agents and intelligent workflows.

## 🎯 What Makes This Plugin Special

Unlike directly using the ImaginePro MCP server, this plugin provides:

- **🤖 4 Specialized Agents** - Domain experts for web dev, UI/UX, marketing, and video
- **⚡ Smart Commands** - Workflow automation beyond basic MCP tool calls
- **📚 Educational** - Learn prompt engineering and best practices
- **🎨 Production-Ready** - Platform-specific optimization and quality guidance
- **🚀 Workflow Focus** - Complete pipelines, not just individual tools

## ✨ Features

### Specialized Agents

1. **🌐 Web Asset Producer** - Hero images, backgrounds, web-optimized assets
2. **🎨 UI/UX Asset Generator** - Icons, illustrations, design system components
3. **📱 Marketing Creative Specialist** - Ads, social media, campaign materials
4. **🎬 Video Workflow Director** - Motion content and video animations

### Smart Commands

- `/imagine-pro` - Intelligent generation with prompt guidance
- `/upscale-it` - Quick production-quality enhancement
- `/vary-it` - Smart variations and refinements
- `/video-flow` - Complete video workflow automation
- `/imagine-guide` - Interactive learning and best practices

### Underlying Power

Access to 8 ImaginePro MCP tools:
- Text-to-image generation
- Multi-modal generation (Gemini)
- Video generation
- Image upscaling
- Variants and rerolls
- Inpainting
- Status tracking

## 🚀 Quick Start

### Prerequisites

- [Claude Code](https://claude.ai/claude-code) >= 2.0.0
- Node.js >= 18.0.0
- ImaginePro API key ([get one free](https://imaginepro.ai))

### Installation

#### Option 1: From ImaginePro Marketplace (Recommended)

```bash
# Add the ImaginePro marketplace
/plugin marketplace add imaginpro/claude-marketplace

# Install the plugin
/plugin install imaginepro

# Set your API key
export IMAGINEPRO_API_KEY="sk-your-api-key-here"
```

#### Option 2: From GitHub

```bash
# Add the plugin repository
/plugin marketplace add imaginpro/imaginepro-claude-plugin

# Install
/plugin install imaginepro

# Set your API key
export IMAGINEPRO_API_KEY="sk-your-api-key-here"
```

#### Option 3: Local Development

```bash
git clone https://github.com/imaginpro/imaginepro-claude-plugin.git
cd imaginepro-claude-plugin

# Add local plugin
/plugin marketplace add ./

# Set your API key
export IMAGINEPRO_API_KEY="sk-your-api-key-here"
```

### Get Your API Key

1. Sign up at [imaginepro.ai](https://imaginepro.ai)
2. Navigate to account settings
3. Generate an API key
4. Copy and export it: `export IMAGINEPRO_API_KEY="sk-your-key"`

Make it permanent:
```bash
echo 'export IMAGINEPRO_API_KEY="sk-your-key"' >> ~/.zshrc
source ~/.zshrc
```

## 📖 Usage Examples

### Web Development

```
# Activate Web Asset Producer agent
"I need a hero image for my SaaS landing page"

# Or use the command directly
/imagine-pro modern SaaS hero image, professional team collaborating,
blue color scheme, space for headline in upper third, 1920x1080

# Upscale for production
/upscale-it [messageId]
```

### UI/UX Design

```
# Activate UI/UX Asset Generator
"Create 5 navigation icons for my mobile app"

# Agent guides you through creating a consistent set

# Or generate individually
/imagine-pro minimal line icon for home navigation, clean geometric,
64px, monochrome, 3px stroke weight
```

### Marketing

```
# Activate Marketing Creative Specialist
"Create 3 Instagram ad variants for my product launch"

# Agent creates A/B test-ready variants

# Or use command
/imagine-pro Instagram ad creative, 1:1 format, productivity app,
scroll-stopping visual, mobile-optimized
```

### Video Production

```
# Use the automated workflow
/video-flow product reveal: wireless headphones from box to wearing,
studio photography style

# Or work with Video Director agent for more control
"Create a day-to-night city timelapse video"
```

## 🎓 Learning Resources

### Interactive Guide

```bash
/imagine-guide

# Or ask specific questions:
/imagine-guide how do I create a hero image?
/imagine-guide best practices for icon sets
/imagine-guide tips for smooth video transitions
```

### Documentation

- [Quick Start Guide](docs/quick-start.md) - Get up and running in 5 minutes
- [Workflow Guides](docs/workflows/) - Complete workflows for each use case
- [Prompt Library](docs/prompt-library/) - Curated, proven prompts
- [Examples](examples/) - Real-world project walkthroughs
- [Troubleshooting](docs/troubleshooting.md) - Common issues and solutions

## 📂 Repository Structure

```
imaginepro-claude-plugin/
├── .claude-plugin/
│   └── plugin.json           # Plugin manifest
├── .mcp.json                 # MCP server configuration
├── agents/                   # 4 specialized agents
│   ├── web-asset-producer.md
│   ├── ui-asset-generator.md
│   ├── marketing-creative.md
│   └── video-director.md
├── commands/                 # 5 smart commands
│   ├── imagine-pro.md
│   ├── upscale-it.md
│   ├── vary-it.md
│   ├── video-flow.md
│   └── imagine-guide.md
├── docs/                     # Documentation
│   ├── quick-start.md
│   ├── workflows/
│   ├── prompt-library/
│   └── troubleshooting.md
└── examples/                 # Real-world examples
```

## 🎯 Common Workflows

### Image Generation Workflow
```
1. Generate initial image
   /imagine-pro [detailed prompt]

2. Explore variations
   /vary-it [messageId]

3. Choose best version

4. Upscale for production
   /upscale-it [best-messageId]

5. Download and use!
```

### Video Creation Workflow
```
1. Describe transformation
   /video-flow [clear transformation description]

2. Review generated video
   (automatically creates frames and video)

3. Use in project!
```

### A/B Testing Workflow
```
1. Generate initial creative
   /imagine-pro [prompt]

2. Create test variants
   /vary-it [messageId]  # Variant A
   /vary-it [messageId]  # Variant B
   /vary-it [messageId]  # Variant C

3. Test all variants

4. Upscale winner
   /upscale-it [winning-messageId]
```

## 💡 Why Use This Plugin?

### vs. Direct MCP Server Usage
- ✅ **Easier**: Specialized agents make it accessible
- ✅ **Smarter**: Workflow automation and intelligent routing
- ✅ **Educational**: Learn best practices as you work
- ✅ **Optimized**: Domain-specific prompting expertise

### vs. External Tools (Midjourney, DALL-E, etc.)
- ✅ **Integrated**: No context switching from Claude Code
- ✅ **Conversational**: Natural language, no special syntax
- ✅ **Workflow-Aware**: Understands your development context
- ✅ **Automated**: Multi-step processes in single commands

### vs. Generic Image Generation
- ✅ **Specialized**: Purpose-built for development workflows
- ✅ **Production-Ready**: Knows specs, dimensions, use cases
- ✅ **Complete**: Video generation, not just images
- ✅ **Professional**: Business/development focus

## 🛠️ Configuration

### Environment Variables

```bash
# Required
export IMAGINEPRO_API_KEY="sk-your-api-key"

# Optional
export IMAGINEPRO_BASE_URL="https://api.imaginepro.ai"  # Custom endpoint
export IMAGINEPRO_TIMEOUT="300000"                       # Timeout in ms
```

### Plugin Settings

The plugin automatically configures the ImaginePro MCP server. Configuration is in `.mcp.json`:

```json
{
  "mcpServers": {
    "imaginepro": {
      "command": "npx",
      "args": ["-y", "imaginepro-mcp-server"],
      "env": {
        "IMAGINEPRO_API_KEY": "${IMAGINEPRO_API_KEY}"
      }
    }
  }
}
```

## 🤝 Contributing

We welcome contributions! Whether it's:

- 🐛 Bug reports
- 💡 Feature requests
- 📝 Documentation improvements
- 🎨 Prompt library additions
- 🔧 Code contributions

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## 🔗 Links

- **ImaginePro API**: [imaginepro.ai](https://imaginepro.ai)
- **MCP Server**: [imaginepro-mcp-server](https://github.com/imaginpro/imaginepro-mcp-server)
- **Issues**: [Report bugs or request features](https://github.com/imaginpro/imaginepro-claude-plugin/issues)
- **Discussions**: [Community forum](https://github.com/imaginpro/imaginepro-claude-plugin/discussions)
- **Documentation**: [Full docs](https://github.com/imaginpro/imaginepro-claude-plugin/tree/main/docs)

## 💬 Support

- 📚 **Documentation**: Start with [Quick Start Guide](docs/quick-start.md)
- 💭 **Community**: [GitHub Discussions](https://github.com/imaginpro/imaginepro-claude-plugin/discussions)
- 🐛 **Issues**: [GitHub Issues](https://github.com/imaginpro/imaginepro-claude-plugin/issues)
- 🌐 **Website**: [imaginepro.ai/support](https://imaginepro.ai/support)

## 🙏 Acknowledgments

Built with:
- [Model Context Protocol](https://modelcontextprotocol.io)
- [ImaginePro API](https://imaginepro.ai)
- [Claude Code](https://docs.claude.com/en/docs/claude-code)

---

**Made with ❤️ for the Claude Code community**

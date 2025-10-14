# ImaginePro MCP Server Setup

The imaginepro-mcp-server has been added to your Claude Code configuration!

## ✅ What's Been Configured

The MCP server has been added to:
```
~/Library/Application Support/Claude/claude_desktop_config.json
```

Configuration added:
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

## 🔑 Set Your API Key

You need to set your ImaginePro API key as an environment variable.

### Step 1: Get Your API Key

1. Go to [imaginepro.ai](https://imaginepro.ai)
2. Sign up or log in
3. Navigate to Account Settings → API Keys
4. Generate a new API key
5. Copy the key (starts with `sk-`)

### Step 2: Set the Environment Variable

**For your shell (permanent):**

If you use **zsh** (macOS default):
```bash
echo 'export IMAGINEPRO_API_KEY="sk-your-actual-api-key-here"' >> ~/.zshrc
source ~/.zshrc
```

If you use **bash**:
```bash
echo 'export IMAGINEPRO_API_KEY="sk-your-actual-api-key-here"' >> ~/.bashrc
source ~/.bashrc
```

**For Claude Code specifically:**

You can also set it directly in the Claude Code configuration file instead of using environment variables:

Edit: `~/Library/Application Support/Claude/claude_desktop_config.json`

Change:
```json
"env": {
  "IMAGINEPRO_API_KEY": "${IMAGINEPRO_API_KEY}"
}
```

To:
```json
"env": {
  "IMAGINEPRO_API_KEY": "sk-your-actual-api-key-here"
}
```

**⚠️ Warning:** If you set it directly in the config file, be careful not to commit this file to version control!

### Step 3: Restart Claude Code

After setting your API key:
1. **Quit Claude Code completely** (Cmd+Q)
2. **Restart Claude Code**
3. The imaginepro-mcp-server will now be available!

## 🧪 Test the Installation

Once Claude Code restarts, you can test if it's working by asking Claude:

```
"What MCP tools are available?"
```

You should see imaginepro tools listed, including:
- generate-image
- upscale-image
- create-variant
- generate-video
- And more...

Or try generating an image:
```
"Use the generate-image tool to create a simple test image of a sunset"
```

## 🎨 Using the Plugin

Now that the MCP server is installed, you can use the plugin features:

### Try the Agents

```
"I need a hero image for my SaaS landing page"
```
(This will activate the Web Asset Producer agent)

### Try the Commands

```
/imagine-pro a serene mountain lake at sunset
```

### Check the Documentation

- Quick Start: `docs/quick-start.md`
- Workflow Guides: `docs/workflows/`
- Prompt Libraries: `docs/prompt-library/`

## 🔧 Troubleshooting

### MCP Server Not Found

If you see "MCP server not found" errors:
1. Verify your API key is set correctly
2. Restart Claude Code completely
3. Check the config file syntax is valid JSON

### API Key Issues

If you get authentication errors:
1. Verify your API key is correct (starts with `sk-`)
2. Check you have API credits at [imaginepro.ai/account](https://imaginepro.ai/account)
3. Ensure the environment variable is set: `echo $IMAGINEPRO_API_KEY`

### Server Won't Start

If the MCP server won't start:
1. Ensure Node.js 18+ is installed: `node --version`
2. Clear npm cache: `npm cache clean --force`
3. Try manual installation: `npm install -g imaginepro-mcp-server`

### Still Having Issues?

Check the troubleshooting guide: `docs/troubleshooting.md`

Or open an issue: https://github.com/imaginpro/imaginepro-claude-plugin/issues

## 📚 Next Steps

1. ✅ Set your API key (see above)
2. ✅ Restart Claude Code
3. ✅ Try generating your first image
4. 📖 Read the Quick Start Guide: `docs/quick-start.md`
5. 🎨 Explore the Prompt Libraries: `docs/prompt-library/`

---

**Happy Creating!** 🚀

The imaginepro-mcp-server provides the infrastructure, and this plugin provides the specialized agents, commands, and educational resources to make you productive quickly!

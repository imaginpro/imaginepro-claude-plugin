# Troubleshooting Guide

Common issues and solutions for the ImaginePro Claude Code Plugin.

## Installation Issues

### Plugin Not Found

**Error**: `Plugin 'imaginepro' not found`

**Solutions**:
1. Ensure marketplace is added:
   ```bash
   /plugin marketplace add imaginpro/claude-marketplace
   ```

2. List available plugins:
   ```bash
   /plugin list
   ```

3. Try direct GitHub install:
   ```bash
   /plugin marketplace add imaginpro/imaginepro-claude-plugin
   /plugin install imaginepro
   ```

### Command Not Recognized

**Error**: `/imagine-pro: command not found`

**Solutions**:
1. Verify plugin is installed:
   ```bash
   /plugin list
   ```

2. Restart Claude Code

3. Check plugin is enabled (not disabled)

4. Reinstall plugin:
   ```bash
   /plugin uninstall imaginepro
   /plugin install imaginepro
   ```

## API Key Issues

### Missing API Key Error

**Error**: `IMAGINEPRO_API_KEY environment variable is required`

**Solutions**:
1. Set the environment variable:
   ```bash
   export IMAGINEPRO_API_KEY="sk-your-actual-key"
   ```

2. Verify it's set:
   ```bash
   echo $IMAGINEPRO_API_KEY
   ```

3. Make it permanent (add to ~/.zshrc or ~/.bashrc):
   ```bash
   echo 'export IMAGINEPRO_API_KEY="sk-your-key"' >> ~/.zshrc
   source ~/.zshrc
   ```

4. Restart Claude Code after setting

### Invalid API Key

**Error**: `Authentication failed` or `Invalid API key`

**Solutions**:
1. Check your key at [imaginepro.ai/account](https://imaginepro.ai/account)
2. Ensure you copied the full key (starts with `sk-`)
3. Check for extra spaces or quotes:
   ```bash
   # Wrong
   export IMAGINEPRO_API_KEY=" sk-key "  # Has spaces

   # Right
   export IMAGINEPRO_API_KEY="sk-key"
   ```
4. Generate a new API key if needed

### API Key Not Recognized

**Error**: Works in terminal but not in Claude Code

**Solutions**:
1. Restart Claude Code completely (quit and reopen)
2. Check Claude Code can access environment:
   ```
   "What's my IMAGINEPRO_API_KEY?" (Claude should see it)
   ```
3. Set in .mcp.json directly (not recommended for security):
   ```json
   {
     "mcpServers": {
       "imaginepro": {
         "env": {
           "IMAGINEPRO_API_KEY": "sk-your-key"
         }
       }
     }
   }
   ```

## Generation Issues

### Generation Takes Too Long

**Issue**: Image/video generation seems stuck

**Expected Times**:
- Images: 30-60 seconds
- Videos: 2-5 minutes

**Solutions**:
1. Wait patiently (especially for videos)
2. Check status manually:
   ```
   "Check the status of generation [messageId]"
   ```
3. If >5 minutes for image or >10 minutes for video, may have failed
4. Try again with simpler prompt

### Generation Failed

**Error**: `Failed to generate image/video`

**Common Causes & Solutions**:

1. **Insufficient Credits**
   - Check account balance at [imaginepro.ai/account](https://imaginepro.ai/account)
   - Add credits if needed

2. **Prompt Violates Policy**
   - Review ImaginePro content policy
   - Try more general, appropriate prompts

3. **Network Issues**
   - Check internet connection
   - Try again after a moment

4. **Server Issues**
   - Check [imaginepro.ai/status](https://imaginepro.ai/status)
   - Try again later

### Poor Quality Results

**Issue**: Generated images don't match expectations

**Solutions**:

1. **Improve your prompt** - Be more specific:
   ```bash
   # Vague
   /imagine-pro a website image

   # Better
   /imagine-pro modern SaaS landing page hero image, professional team
   working in bright office, blue brand colors, 1920x1080, space for
   headline text in upper third, photorealistic, high quality
   ```

2. **Use /imagine-guide** for prompt engineering tips:
   ```bash
   /imagine-guide how to write better prompts
   ```

3. **Try variations**:
   ```bash
   /vary-it [messageId]
   ```

4. **Work with specialized agents** - They know best practices:
   ```
   "I need help creating [type of asset]"
   ```

### Inconsistent Icon Sets

**Issue**: Icons in set don't match visually

**Solutions**:

1. **Use exact same style descriptors** for all icons:
   ```bash
   # All icons must have identical style keywords
   "minimal line icon, 3px stroke, monochrome, 64px, clean geometric"
   ```

2. **Generate sequentially** with UI/UX Asset Generator agent:
   ```
   "Create 5 navigation icons: home, search, profile, settings, help"
   ```
   Agent maintains consistency across set.

3. **Reference previous icons**:
   ```bash
   /imagine-pro minimal line icon for search, MATCHING STYLE of previous
   home icon, same line weight and visual density
   ```

### Video Transitions Are Choppy

**Issue**: Video doesn't transition smoothly

**Solutions**:

1. **Ensure frame compatibility**:
   - Same camera angle
   - Same lighting (or intentional transition)
   - Similar composition
   - Aligned perspective

2. **Use /video-flow** (handles compatibility automatically):
   ```bash
   /video-flow day to night cityscape, same camera position
   ```

3. **Work with Video Director agent**:
   ```
   "Create a smooth video transition showing [concept]"
   ```
   Agent ensures frames are compatible.

4. **Simplify transformation**:
   - Change fewer elements between frames
   - Keep background and perspective identical
   - Only transform main subject

## Command Issues

### /imagine-pro Doesn't Provide Guidance

**Issue**: Command acts like basic generation

**Solutions**:

1. Include enough detail for analysis:
   ```bash
   # Too short
   /imagine-pro mountain

   # Better
   /imagine-pro mountain landscape for website hero, modern aesthetic
   ```

2. Ask questions after generation:
   ```
   "What could I improve about this prompt?"
   ```

### /vary-it Always Creates Random Variants

**Issue**: Guided changes don't work

**Current Limitation**:
Targeted regional editing (inpainting) requires mask URLs. For now:

1. Use descriptive guidance:
   ```bash
   /vary-it [msg-id] make the colors warmer and more vibrant
   ```

2. Or use inpaint tool directly with mask:
   ```
   "Use inpaint-image to change the background to mountains"
   (requires providing mask URL)
   ```

### /upscale-it Returns Error

**Error**: `Failed to upscale` or `Message ID not found`

**Solutions**:

1. **Verify message ID** is correct:
   - Check you copied full ID
   - Ensure no extra spaces

2. **Original image must exist**:
   - Can't upscale if original generation failed
   - Verify original exists first

3. **Try again** (temporary API issue):
   ```bash
   /upscale-it [messageId]
   ```

## Agent Issues

### Agent Not Activating

**Issue**: Specialized agent doesn't engage

**Solutions**:

1. **Be explicit** about what you need:
   ```
   # Vague
   "Create an image"

   # Specific
   "I need a hero image for my SaaS landing page"
   ```

2. **Mention the context**:
   ```
   "Create navigation icons for my mobile app"  # Activates UI/UX agent
   "Create Instagram ads for my product"        # Activates Marketing agent
   "Create a product reveal video"              # Activates Video agent
   ```

3. **Ask directly**:
   ```
   "Activate the Web Asset Producer agent to help with my project"
   ```

### Agent Asks Too Many Questions

**Issue**: Agent keeps asking instead of generating

**Why**: Agent needs context for optimized results

**Solutions**:

1. **Provide comprehensive initial info**:
   ```
   "Create a hero image for my project management SaaS. Target audience
   is enterprise teams. Brand colors are blue and white. Need space for
   headline in upper third. Professional and collaborative mood."
   ```

2. **Answer questions** (helps get better results!)

3. **Skip to generation** if you prefer:
   ```bash
   /imagine-pro [detailed prompt]
   ```

## Performance Issues

### Slow Response Times

**Issue**: Everything feels slow

**Causes & Solutions**:

1. **AI Generation is Slow** (expected):
   - Images: 30-60 seconds
   - Videos: 2-5 minutes
   - This is normal API processing time

2. **Network Issues**:
   - Check internet connection
   - Try again on better connection

3. **High API Load**:
   - Try during off-peak hours
   - Check [imaginepro.ai/status](https://imaginepro.ai/status)

### Plugin Uses Too Many Credits

**Issue**: Running out of credits quickly

**Solutions**:

1. **Generate at standard quality first**:
   - Only upscale final/winning versions
   - Don't upscale every variant

2. **Optimize workflow**:
   ```
   Generate (1 credit)
   → Vary 2-3x (2-3 credits)
   → Upscale winner (1 credit)
   = 4-5 total instead of 10+
   ```

3. **Use /vary-it strategically**:
   - Don't create endless variants
   - 3-5 variants is usually enough

4. **Batch related assets**:
   - Generate icon set in one session
   - Maintain consistency (fewer retries)

## MCP Server Issues

### MCP Server Not Starting

**Error**: Plugin installed but tools unavailable

**Solutions**:

1. **Check npx can access package**:
   ```bash
   npx -y imaginepro-mcp-server --help
   ```

2. **Verify npm is working**:
   ```bash
   npm --version
   ```

3. **Clear npx cache**:
   ```bash
   npx clear-npx-cache
   ```

4. **Check .mcp.json exists** in plugin directory

5. **Restart Claude Code**

### MCP Connection Errors

**Error**: `Failed to connect to MCP server`

**Solutions**:

1. Check Node.js version:
   ```bash
   node --version  # Should be 18+
   ```

2. Update npm:
   ```bash
   npm install -g npm@latest
   ```

3. Reinstall MCP server package:
   ```bash
   npm install -g imaginepro-mcp-server
   ```

4. Check firewall isn't blocking Node

## Getting Help

### Still Having Issues?

1. **Check Logs**:
   - Claude Code logs may have error details
   - MCP server logs show connection issues

2. **Search Issues**:
   - [GitHub Issues](https://github.com/imaginpro/imaginepro-claude-plugin/issues)
   - Someone may have solved it already

3. **Ask the Community**:
   - [GitHub Discussions](https://github.com/imaginpro/imaginepro-claude-plugin/discussions)
   - Helpful community members

4. **Report a Bug**:
   - [Create new issue](https://github.com/imaginpro/imaginepro-claude-plugin/issues/new)
   - Include: error message, what you tried, system info

5. **Contact Support**:
   - [imaginepro.ai/support](https://imaginepro.ai/support)
   - For API-specific issues

### Information to Include When Reporting Issues

- Plugin version: `/plugin list`
- Claude Code version: `/help`
- Node.js version: `node --version`
- Operating system
- Error message (full text)
- Steps to reproduce
- What you've already tried

## Useful Commands for Debugging

```bash
# Check environment
echo $IMAGINEPRO_API_KEY

# Verify plugin installed
/plugin list

# Check command availability
/help

# Test MCP server
npx -y imaginepro-mcp-server

# Check Node version
node --version

# Clear caches
npx clear-npx-cache
```

---

**Most issues are solved by**:
1. Restarting Claude Code
2. Verifying API key is set correctly
3. Ensuring latest plugin version
4. Checking API credit balance

If you're still stuck, don't hesitate to ask for help! 🤝

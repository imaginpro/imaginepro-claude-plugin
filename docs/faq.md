# Frequently Asked Questions

Common questions and answers about the ImaginePro Claude Code plugin.

## Getting Started

### What is the ImaginePro Claude Code plugin?

The ImaginePro plugin brings professional AI image and video generation directly into Claude Code. Instead of switching between applications, you can generate web assets, UI components, marketing materials, and videos without leaving your development workflow.

### How do I install the plugin?

**Option 1: From Marketplace (Recommended)**
```bash
/plugin marketplace add imaginpro/claude-marketplace
/plugin install imaginepro
```

**Option 2: From GitHub**
```bash
/plugin marketplace add imaginpro/imaginepro-claude-plugin
/plugin install imaginepro
```

**Option 3: Local Development**
```bash
git clone https://github.com/imaginpro/imaginepro-claude-plugin.git
/plugin marketplace add ./imaginepro-claude-plugin
/plugin install imaginepro
```

### Do I need an API key?

Yes, you need an ImaginePro API key to use the plugin. Sign up at [imaginepro.ai](https://imaginepro.ai) (free tier available) and get your API key from account settings.

Set it permanently:
```bash
echo 'export IMAGINEPRO_API_KEY="sk-your-key"' >> ~/.zshrc
source ~/.zshrc
```

### What are the system requirements?

- **Claude Code**: Version 2.0.0 or higher
- **Node.js**: Version 18.0.0 or higher
- **Internet Connection**: Required for API calls
- **API Key**: Valid ImaginePro account

## Using the Plugin

### How do the agents work?

The plugin includes 4 specialized agents, each with deep expertise in their domain:

- **Web Asset Producer**: Creates website images (hero banners, backgrounds, etc.)
- **UI/UX Asset Generator**: Generates icons, illustrations, empty states
- **Marketing Creative Specialist**: Produces ads, social media content, campaigns
- **Video Workflow Director**: Guides video creation from concept to final animation

Activate an agent by mentioning their role in your request, e.g., "I need help from the Web Asset Producer to create a hero image."

### What's the difference between commands and agents?

- **Commands** (`/imagine-pro`, `/upscale-it`, etc.): Quick tools for specific tasks
- **Agents**: Conversational experts that guide you through complex workflows

Use commands for simple tasks, agents for guidance and complex projects.

### How do I create good prompts?

**Be Specific**: Include style, colors, composition, and use case
**Use Examples**:
- ❌ "Make a logo"
- ✅ "Minimalist line icon for a music app, 64px, white background, simple geometric shapes"

**Include Context**: Mention platform (Instagram, web, mobile) and purpose
**Reference Quality**: Add "high quality", "professional", "4k"

### What's the typical workflow?

1. **Generate**: `/imagine-pro [detailed prompt]`
2. **Refine**: `/vary-it [messageId]` to explore alternatives
3. **Select**: Choose your favorite variant
4. **Enhance**: `/upscale-it [chosen-messageId]` for production quality
5. **Use**: Download and implement in your project

### How long do generations take?

- **Images**: 10-30 seconds
- **Variants**: 15-45 seconds
- **Upscaling**: 30-60 seconds
- **Videos**: 2-5 minutes
- **Complex requests**: Up to 3 minutes

You can continue working while generations process.

## Image Generation

### Why doesn't my image look like what I expected?

**Common Issues:**
1. **Vague Prompts**: Add specific details about style, colors, composition
2. **Missing Context**: Include platform dimensions and use case
3. **Style Conflicts**: Be consistent (don't mix "photorealistic" with "cartoon")

**Solutions:**
- Use `/imagine-guide` for prompt improvement tips
- Try `/vary-it` to explore different interpretations
- Reference the examples in our documentation

### What's the difference between variants and rerolls?

- **Variants** (`/vary-it`): Explore different creative interpretations while keeping the core concept
- **Rerolls**: Regenerate with the same prompt but different random seed for subtle variations

Use variants for exploration, rerolls when the concept is right but execution isn't.

### When should I upscale images?

**Always upscale for:**
- Production websites
- Marketing materials
- Print materials
- High-resolution displays
- Professional presentations

**Skip upscaling for:**
- Quick prototypes
- Internal reviews
- Low-resolution mockups
- Placeholder content

### What's the image quality like?

- **Standard Generation**: High quality, suitable for web and social media
- **Upscaled**: Production-ready, crisp at any size, suitable for print
- **Formats**: PNG with transparency support
- **Resolution**: Up to 4K after upscaling

## Video Creation

### How does video generation work?

Videos are created from two compatible image frames:
1. **Start Frame**: Beginning state of your transformation
2. **End Frame**: Ending state
3. **AI Animation**: Smooth transition between the frames

The key is **frame compatibility** - same camera angle, lighting, and composition.

### What makes frames compatible?

**Essential for smooth videos:**
- Same camera position and angle
- Compatible lighting (or intentional lighting changes)
- Similar color palette
- Logical transformation between states
- Matching background elements

**Pro Tip**: Use the Video Director agent to ensure compatibility.

### Can I create videos longer than 5 seconds?

Currently, videos are optimized for 3-5 second animations. For longer content:
- Create multiple short videos
- Combine them in video editing software
- Use for different sections of longer content

### What's the video quality and format?

- **Format**: MP4 video
- **Resolution**: HD (1920x1080)
- **Frame Rate**: 30fps
- **File Size**: 1-5MB depending on length
- **Transparency**: Not supported (solid backgrounds only)

## Troubleshooting

### I'm getting "API key invalid" errors

**Check:**
1. API key is correctly set: `echo $IMAGINEPRO_API_KEY`
2. Key starts with "sk-" and is complete
3. Account has credits remaining
4. Key hasn't expired

**Fix:**
```bash
export IMAGINEPRO_API_KEY="sk-your-correct-key"
```

### Generations are failing or taking too long

**Possible Causes:**
1. **Rate Limiting**: Too many requests - wait 60 seconds
2. **Credit Issues**: Check account balance
3. **Content Policy**: Prompt may violate guidelines
4. **Server Load**: Try again in a few minutes

**Check Status:**
```bash
# For long-running jobs
/fetch-status messageId:"your-message-id"
```

### Images aren't the right dimensions

**Solutions:**
1. **Specify explicitly**: Include dimensions in prompt (1920x1080)
2. **Use aspect ratios**: "16:9 aspect ratio", "square format"
3. **Platform-specific**: "Instagram square", "Facebook post dimensions"

### Plugin commands aren't working

**Check:**
1. Plugin is installed: `/plugin list` should show "imaginepro"
2. MCP server is running: Check for connection errors
3. Environment variables are set
4. You're using the correct command syntax

**Reinstall if needed:**
```bash
/plugin uninstall imaginepro
/plugin install imaginepro
```

## Billing & Credits

### How much does it cost?

- **Free Tier**: Limited credits for testing
- **Pay-as-you-go**: Credits based on usage
- **Enterprise**: Custom pricing for high volume

**Approximate Costs:**
- Basic image: 1-2 credits
- Upscaling: 2-4 credits
- Video generation: 10-15 credits

### How do I check my credit balance?

Visit your [ImaginePro dashboard](https://imaginepro.ai/dashboard) or contact support@imaginepro.ai.

### What happens when I run out of credits?

Generations will fail with "insufficient credits" error. Top up your account at imaginepro.ai to continue.

## Advanced Usage

### Can I use this commercially?

Yes! Generated content can be used commercially. You're responsible for ensuring usage complies with your organization's policies and any applicable laws.

### How do I maintain brand consistency?

**Techniques:**
1. **Style Guides**: Define consistent descriptors ("professional", "minimalist", "blue and green palette")
2. **Reference Images**: Use existing brand assets as references
3. **Prompt Templates**: Create reusable prompt structures
4. **Agent Guidance**: Use agents for complex brand-aligned projects

### Can I integrate this into my workflow?

**Options:**
1. **Scripts**: Use MCP tools directly in automation
2. **Batch Processing**: Generate multiple assets at once
3. **Templates**: Create prompt libraries for common needs
4. **CI/CD**: Integrate into development pipelines

### What's the difference from direct MCP server usage?

**Plugin Advantages:**
- Specialized agents with domain expertise
- Educational guidance and best practices
- Workflow automation commands
- Comprehensive documentation
- Easier onboarding for new users

**Direct MCP Usage:**
- More control for advanced users
- Integration into existing MCP setups
- Lighter weight (no plugin overhead)

## Getting Help

### Where can I find more examples?

Check our [examples directory](../examples/) with real-world walkthroughs:
- SaaS landing page creation
- Mobile app design system
- Marketing campaign assets
- Product video production

### How do I get support?

- **Documentation**: Start with [Quick Start Guide](quick-start.md)
- **Interactive Guide**: Use `/imagine-guide` command
- **GitHub Issues**: [Report bugs](https://github.com/imaginpro/imaginepro-claude-plugin/issues)
- **Discussions**: [Community forum](https://github.com/imaginpro/imaginepro-claude-plugin/discussions)
- **Email**: support@imaginepro.ai

### Can I contribute to the plugin?

Yes! We welcome contributions:
- **Prompt Libraries**: Share successful prompts
- **Examples**: Add real-world use cases
- **Documentation**: Improve guides and tutorials
- **Code**: Enhance the plugin functionality

See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

## Technical Details

### What MCP tools are available?

The plugin provides access to 8 ImaginePro MCP tools:
1. `generate-image` - Primary image generation
2. `create-variant` - Alternative versions
3. `reroll-image` - Same prompt, different result
4. `upscale-image` - Quality enhancement
5. `inpaint-image` - Regional modifications
6. `generate-video` - Video animations
7. `fetch-status` - Job status checking
8. `imagine-gemini` - Multi-modal generation

### Is my data secure?

- API keys are stored locally (not transmitted to Anthropic)
- Generations happen on ImaginePro's secure infrastructure
- No training data is collected from your prompts
- Standard HTTPS encryption for all communications

### Can I use this offline?

No, internet connection is required for:
- API calls to generate content
- Downloading generated assets
- Plugin updates and documentation access

---

**Still have questions?** Check the [troubleshooting guide](troubleshooting.md) or ask the `/imagine-guide` command for specific guidance!
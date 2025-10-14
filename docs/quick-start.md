# Quick Start Guide

Get up and running with the ImaginePro Claude Code Plugin in 5 minutes.

## Prerequisites Checklist

- [ ] Claude Code 2.0+ installed
- [ ] Node.js 18.0+ installed (`node --version`)
- [ ] ImaginePro API key ([get one here](https://imaginepro.ai))

## Step 1: Get Your API Key (2 minutes)

1. Go to [imaginepro.ai](https://imaginepro.ai)
2. Sign up for a free account
3. Navigate to **Account Settings** → **API Keys**
4. Click **Generate New Key**
5. Copy your API key (starts with `sk-`)

## Step 2: Install the Plugin (1 minute)

Open Claude Code and run:

```bash
# Add the ImaginePro marketplace
/plugin marketplace add imaginpro/claude-marketplace

# Install the plugin
/plugin install imaginepro
```

## Step 3: Configure API Key (1 minute)

Set your API key as an environment variable:

```bash
export IMAGINEPRO_API_KEY="sk-your-actual-api-key-here"
```

**Make it permanent** (add to your shell profile):

```bash
# For zsh (macOS default)
echo 'export IMAGINEPRO_API_KEY="sk-your-key"' >> ~/.zshrc
source ~/.zshrc

# For bash
echo 'export IMAGINEPRO_API_KEY="sk-your-key"' >> ~/.bashrc
source ~/.bashrc
```

## Step 4: Verify Installation (30 seconds)

Test that everything works:

```bash
# Try the interactive guide
/imagine-guide

# Or generate your first image
/imagine-pro a serene mountain lake at sunset
```

If you see a response, you're all set! 🎉

## Your First Creations (1 minute)

### Generate a Web Hero Image

```
/imagine-pro modern SaaS landing page hero image, professional team
collaborating in bright office, blue and white color scheme, space for
headline text in upper third, photorealistic, 1920x1080
```

### Create an Icon

```
/imagine-pro minimal line icon for settings, gear symbol, clean geometric
lines, 64px, monochrome black on white, 3px stroke weight
```

### Make a Social Media Image

```
/imagine-pro Instagram post image for productivity tip, 1:1 square format,
clean modern design, vibrant colors, mobile-friendly composition
```

### Generate a Video

```
/video-flow sunrise to sunset over mountain landscape, same camera angle,
smooth time progression, cinematic
```

## Next Steps

### Learn the Workflow

Basic workflow for any asset:
```
1. Generate    → /imagine-pro [prompt]
2. Vary        → /vary-it [messageId]
3. Choose best → Review variants
4. Upscale     → /upscale-it [messageId]
5. Use         → Download and integrate
```

### Explore Specialized Agents

Try working with domain experts:

**For Web Development:**
```
"I need a hero image for my portfolio website"
```
(Activates Web Asset Producer agent)

**For UI Design:**
```
"Create 5 navigation icons for my mobile app"
```
(Activates UI/UX Asset Generator agent)

**For Marketing:**
```
"Create Instagram ad variants for my product launch"
```
(Activates Marketing Creative Specialist agent)

**For Video:**
```
"Create a product reveal video showing transformation"
```
(Activates Video Workflow Director agent)

### Master the Commands

- **`/imagine-pro`** - Your main generation command with guidance
- **`/upscale-it`** - Make images production-ready
- **`/vary-it`** - Explore alternatives and refinements
- **`/video-flow`** - Complete video workflow automation
- **`/imagine-guide`** - Interactive learning and help

### Dive into Documentation

- [Web Development Workflow](workflows/web-development.md)
- [UI/UX Design Workflow](workflows/ui-ux-design.md)
- [Marketing Content Workflow](workflows/marketing-content.md)
- [Video Creation Workflow](workflows/video-creation.md)
- [Prompt Library](prompt-library/) - Curated examples
- [Troubleshooting](troubleshooting.md) - Common issues

## Common First-Time Questions

### Q: How much does this cost?

A: The plugin is free. You only pay for ImaginePro API usage (credits per generation). Check [imaginepro.ai/pricing](https://imaginepro.ai/pricing) for current rates.

### Q: Can I use generated images commercially?

A: Yes! Check ImaginePro's terms of service for specific usage rights.

### Q: How long does generation take?

- Images: 30-60 seconds
- Videos: 2-5 minutes (includes frame generation)

### Q: What if I get an error?

See [Troubleshooting Guide](troubleshooting.md) or check:
1. Is your API key set correctly? `echo $IMAGINEPRO_API_KEY`
2. Do you have API credits? Check your [imaginepro.ai account](https://imaginepro.ai/account)
3. Is Claude Code up to date? `/help` to check version

### Q: Can I use this offline?

No, it requires internet connection to access the ImaginePro API.

### Q: How do I update the plugin?

```bash
/plugin update imaginepro
```

## Tips for Success

### 1. Be Specific in Prompts
❌ "make a website image"
✅ "modern SaaS hero image, 1920x1080, professional team collaborating, blue color scheme, space for text overlay"

### 2. Iterate with Variants
Don't upscale immediately. Create 2-3 variants first, then upscale the best one.

### 3. Use the Right Agent
Activate specialized agents for domain expertise:
- Web Asset Producer for websites
- UI/UX Asset Generator for app design
- Marketing Creative for ads/social
- Video Director for motion content

### 4. Learn from /imagine-guide
Ask questions! The guide teaches you prompt engineering and best practices.

### 5. Check Examples
Browse [examples/](../examples/) for real-world project walkthroughs.

## Workflow Cheat Sheet

```bash
# Standard Image Workflow
/imagine-pro [prompt]          # Generate
/vary-it [msg-id]              # Create variants (2-3x)
/upscale-it [best-msg-id]      # Upscale winner

# Video Workflow
/video-flow [transformation]   # Automated complete workflow

# Learning
/imagine-guide [question]      # Get help anytime

# Iteration
/imagine-pro [prompt]          # Initial
/vary-it [msg-id] [changes]    # Refine
/vary-it [new-msg-id] [more]   # Refine again
/upscale-it [final-msg-id]     # Finalize
```

## You're Ready! 🚀

Start creating professional visual assets without leaving Claude Code.

**First project ideas:**
- Update your personal website hero image
- Create icons for a side project
- Design social media posts for your brand
- Generate marketing visuals for a launch
- Build a complete asset set for an app

Need help? Use `/imagine-guide` or check the [full documentation](README.md).

Happy creating! 🎨

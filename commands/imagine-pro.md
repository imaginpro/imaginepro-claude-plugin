Generate an AI image with ImaginePro using best practices and intelligent guidance.

This command provides an enhanced image generation experience with:
- Prompt analysis and improvement suggestions
- Optimal generation settings
- Clear next-step recommendations
- Prompt engineering education

When you use this command, Claude will:

1. **Analyze your prompt** for clarity and effectiveness
2. **Suggest improvements** if your prompt could be more specific
3. **Generate the image** using the `generate-image` MCP tool
4. **Display the message ID** clearly for follow-up actions
5. **Recommend next steps** like upscaling or creating variants
6. **Provide prompt tips** to help you improve future generations

## Usage

```
/imagine-pro [your detailed prompt]
```

## Examples

### Basic Usage
```
/imagine-pro a serene mountain lake at sunset with mist rising from the water
```

### Web Development
```
/imagine-pro modern SaaS hero image, collaborative team working, blue color scheme, space for headline text in upper third
```

### UI Design
```
/imagine-pro minimal line icon for home navigation, simple house symbol, clean geometric, 64px, monochrome
```

### Marketing
```
/imagine-pro Instagram ad creative, productivity app for remote workers, before/after split, aspirational lifestyle
```

## Tips for Better Results

### Be Specific About:
- **Style**: photorealistic, illustration, 3D render, hand-drawn, minimalist
- **Composition**: centered, rule of thirds, negative space, text overlay area
- **Colors**: specific palette, brand colors, mood-based colors
- **Lighting**: natural, studio, dramatic, soft, golden hour
- **Quality**: high quality, 4k, professional, detailed

### For Web Assets:
- Mention dimensions or use case (hero image, background, card)
- Specify where text will appear
- Include mood/emotion to convey

### For Icons:
- State the size (design at 64px for clarity)
- Mention style (minimal, filled, outlined)
- Specify single color or brand colors

### For Marketing:
- Include platform (Instagram, Facebook, LinkedIn)
- Mention target audience or emotion
- Specify room for CTA or headline

## After Generation

Once your image is generated, you'll receive a message ID. You can then:

- **Upscale for production**: `/upscale-it [messageId]`
- **Create variations**: `/vary-it [messageId]`
- **Generate more**: Use /imagine-pro again with refined prompt

## What Makes This Different?

Unlike directly calling the `generate-image` MCP tool, `/imagine-pro`:
- Guides you toward better prompts
- Educates you on prompt engineering
- Suggests platform-specific optimizations
- Provides structured next steps
- Helps you learn for future generations

## Related Commands

- `/upscale-it` - Enhance image quality for production
- `/vary-it` - Create variations or refinements
- `/video-flow` - Create video animations
- `/imagine-guide` - Learn more about ImaginePro workflows

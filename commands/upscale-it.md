Upscale an ImaginePro generated image to higher resolution and enhanced quality.

This command provides quick, friction-free upscaling for production-ready assets.

## Usage

```
/upscale-it [messageId]
```

The message ID is provided when you generate an image using `/imagine-pro` or the `generate-image` MCP tool.

## When to Upscale

**Always upscale before using images in production:**
- Web hero images and backgrounds
- Marketing materials and ads
- Print materials
- High-quality presentations
- Final product assets

**You can skip upscaling for:**
- Quick prototypes and mockups
- Internal review and iteration
- Placeholder images during development
- Proof-of-concept demonstrations

## What Upscaling Does

Upscaling enhances your image with:
- **Higher Resolution**: Increased pixel dimensions for sharper display
- **Enhanced Detail**: AI-powered detail enhancement
- **Better Quality**: Improved clarity and sharpness
- **Production-Ready**: Suitable for professional use cases

## Examples

### After Generating an Image
```
[You just used /imagine-pro and got message ID: abc123xyz]

/upscale-it abc123xyz
```

### Multiple Images
```
# Upscale your best variant
/upscale-it variant-1-abc
/upscale-it variant-2-def
/upscale-it variant-3-ghi
```

## Workflow Integration

### Typical Image Workflow
1. Generate initial image: `/imagine-pro [prompt]`
2. Review result (message ID: abc123)
3. Optionally create variants: `/vary-it abc123`
4. Choose best version
5. Upscale for production: `/upscale-it [best-messageId]`
6. Download and use in project

### A/B Testing Workflow
1. Generate 3 variants for testing
2. Test all three at standard quality
3. Identify winning variant
4. Upscale only the winner: `/upscale-it [winner-messageId]`
5. Use upscaled version in production

## Performance Notes

- **Processing Time**: Upscaling typically takes 30-60 seconds
- **New Message ID**: Upscaling creates a new message ID for the enhanced version
- **Original Preserved**: Your original image remains available at its original ID

## Tips

### For Web Development
- Upscale hero images, feature sections, and prominent visuals
- Consider file size after upscaling - may need compression
- Export at 2x or 3x for retina display support

### For Marketing
- Always upscale final ad creatives before launching campaigns
- Upscale images for print materials (flyers, brochures)
- High-res versions for press kits and media

### For UI/UX Design
- Upscale icon sets for crisp rendering at all sizes
- Enhance illustrations used in final product
- Create 1x, 2x, 3x variants from upscaled version

### For Video
- Consider upscaling video keyframes before generating video
- Higher quality frames often result in better video output
- Especially important for professional/commercial videos

## Cost Consideration

Upscaling uses ImaginePro API credits. Best practices:
- Generate and review at standard quality first
- Only upscale images you're confident about using
- Upscale winning A/B test variants, not all variants
- Skip upscaling for internal/prototype work

## Related Commands

- `/imagine-pro` - Generate images with guidance
- `/vary-it` - Create variations before upscaling
- `/video-flow` - Create videos (consider upscaling frames first)
- `/imagine-guide` - Learn more about workflows

## Quick Reference

```bash
# Basic upscale
/upscale-it abc123

# Typical workflow
/imagine-pro [prompt]           # Returns: msg-001
/vary-it msg-001                # Returns: msg-002
/upscale-it msg-002             # Production ready!
```

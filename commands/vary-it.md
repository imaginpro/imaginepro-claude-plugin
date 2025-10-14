Create intelligent variations and refinements of an existing ImaginePro generated image.

This command smartly decides the best approach for creating variations based on your request, using the appropriate MCP tool (variant, reroll, or inpaint).

## Usage

```bash
# Random variation
/vary-it [messageId]

# Guided variation with description
/vary-it [messageId] [what to change]
```

## How It Works

`/vary-it` intelligently chooses the right technique:

### Random Variation (No Description)
```
/vary-it abc123
```
Uses the `create-variant` tool to generate alternative versions exploring different interpretations while maintaining the core concept.

### Reroll (Same Prompt, Different Result)
```
/vary-it abc123 try a completely different take
```
Uses the `reroll-image` tool to regenerate from the same original prompt with different random seed.

### Guided Changes (Future: Inpainting)
```
/vary-it abc123 make the background mountains instead of ocean
```
Currently suggests using the `inpaint-image` tool with a mask for targeted regional changes.

## Common Use Cases

### Exploring Alternatives
```
# Generate initial image
/imagine-pro modern office workspace, minimalist, blue tones

# Explore variations
/vary-it [messageId]  # Get 2-3 alternative interpretations
```

### Refining Details
```
# Initial generation
/imagine-pro product hero image for wireless earbuds

# Adjust colors
/vary-it [messageId] make colors warmer and more inviting

# Try different angle
/vary-it [messageId] show from a different perspective
```

### A/B Testing
```
# Original version
/imagine-pro landing page hero image, SaaS product

# Create test variants
/vary-it [messageId]  # Variant A
/vary-it [messageId]  # Variant B
/vary-it [messageId]  # Variant C

# Test all, upscale winner
/upscale-it [winning-messageId]
```

### Iteration Workflow
```
# Round 1
/imagine-pro professional team collaboration scene
# Result: msg-001

# Round 2 - Explore variations
/vary-it msg-001
# Result: msg-002 (like this direction!)

# Round 3 - Refine the variant
/vary-it msg-002 add more natural lighting
# Result: msg-003 (perfect!)

# Finalize
/upscale-it msg-003
```

## Examples by Use Case

### Web Development
```
# Hero image variations
/vary-it hero-img-123

# Try different color schemes
/vary-it hero-img-123 use cooler blue tones instead

# Adjust composition
/vary-it hero-img-123 more negative space in upper third for text
```

### UI/UX Design
```
# Icon variations
/vary-it icon-abc make the lines slightly thicker

# Illustration style shifts
/vary-it illustration-xyz try a more playful, hand-drawn style

# Color palette changes
/vary-it empty-state-123 use purple and pink instead of blue
```

### Marketing
```
# Ad creative variations for A/B testing
/vary-it ad-001  # Different composition
/vary-it ad-001  # Another alternative
/vary-it ad-001  # Third variant

# Mood adjustments
/vary-it social-post-456 make it feel more energetic and vibrant

# Element changes
/vary-it email-header-789 change the product from silver to black
```

### Video Frames
```
# Refine start frame before video generation
/vary-it start-frame-abc adjust lighting to be more dramatic

# Match end frame to updated start frame
/vary-it end-frame-def match the lighting from the new start frame
```

## What to Expect

### Random Variations
- **Similar but different**: Maintains core concept, explores alternatives
- **Useful for**: Exploring options, A/B testing, finding best version
- **Results in**: New image with new message ID

### Guided Refinements
- **Targeted changes**: Modifies specific aspects you describe
- **Useful for**: Iterative improvement, fixing specific issues
- **Results in**: Refined version addressing your feedback

## Best Practices

### Do:
✅ Generate multiple variants before upscaling
✅ Use clear, specific descriptions for changes
✅ Iterate progressively (don't try to change everything at once)
✅ Create 3-5 variants for A/B testing
✅ Keep track of message IDs for versions you like

### Don't:
❌ Upscale too early (create variants first)
❌ Request too many changes at once
❌ Forget to note which variant you prefer
❌ Generate endless variants (diminishing returns after 5-6)

## Inpainting (Advanced)

For precise regional edits, you'll need to use the `inpaint-image` MCP tool directly with a mask:

```
# This requires a mask image URL
inpaint-image:
  messageId: abc123
  maskUrl: https://your-mask-url.png (white = edit area)
  prompt: "add rainbow in the sky"
```

`/vary-it` will guide you if your request needs inpainting.

## Workflow Integration

### Standard Workflow
```
Generate → Vary → Choose Best → Upscale
```

### Iterative Refinement
```
Generate → Vary → Vary Best → Vary Again → Upscale
```

### A/B Testing Workflow
```
Generate → Vary 3x → Test All → Upscale Winner
```

## Performance Notes

- **Processing Time**: 30-60 seconds per variation
- **New Message IDs**: Each variation gets a unique ID
- **Original Preserved**: Original image remains unchanged
- **Credit Usage**: Each variation uses API credits

## Tips by Agent

### With Web Asset Producer
```
/vary-it [msg-id] adjust for mobile-first composition
/vary-it [msg-id] leave more space for headline text
```

### With UI/UX Asset Generator
```
/vary-it [msg-id] make the icon set more consistent
/vary-it [msg-id] adjust colors for better accessibility contrast
```

### With Marketing Creative
```
/vary-it [msg-id] make more attention-grabbing for social media
/vary-it [msg-id] create urgency in the composition
```

### With Video Director
```
/vary-it [start-frame-id] match lighting to the end frame
/vary-it [msg-id] adjust perspective to be more cinematic
```

## Related Commands

- `/imagine-pro` - Generate initial images
- `/upscale-it` - Enhance quality after choosing best variant
- `/video-flow` - Create videos from refined frames
- `/imagine-guide` - Learn variation strategies

## Quick Reference

```bash
# Random variation
/vary-it abc123

# Guided refinement
/vary-it abc123 make colors warmer

# Multiple variants for testing
/vary-it abc123  # → msg-v1
/vary-it abc123  # → msg-v2
/vary-it abc123  # → msg-v3

# Choose winner and upscale
/upscale-it msg-v2
```

# API Reference - ImaginePro MCP Tools

Complete technical reference for the 8 ImaginePro MCP (Model Context Protocol) tools used by this Claude Code plugin.

## Overview

The ImaginePro plugin integrates with the `imaginepro-mcp-server` npm package, which provides 8 specialized AI generation tools. These tools are automatically configured when you install the plugin and set your `IMAGINEPRO_API_KEY`.

## Tool Categories

### Image Generation Tools
- [`generate-image`](#generate-image) - Primary image generation from text prompts
- [`create-variant`](#create-variant) - Generate alternative versions of existing images
- [`reroll-image`](#reroll-image) - Regenerate image with same prompt, different seed

### Image Enhancement Tools
- [`upscale-image`](#upscale-image) - Increase resolution and quality
- [`inpaint-image`](#inpaint-image) - Modify specific regions of images

### Video Generation Tools
- [`generate-video`](#generate-video) - Create videos from start/end frame pairs

### Utility Tools
- [`fetch-status`](#fetch-status) - Check generation job status
- [`imagine-gemini`](#imagine-gemini) - Multi-modal generation with Gemini

## Tool Specifications

### `generate-image`

Primary tool for creating images from text descriptions.

**Parameters:**
```typescript
{
  messageId?: string,        // Optional: Reference to previous message
  prompt: string,           // Required: Text description of desired image
  model?: string,           // Optional: AI model to use (default: flux-dev)
  aspectRatio?: string,     // Optional: Image aspect ratio (16:9, 1:1, etc.)
  style?: string           // Optional: Style preset
}
```

**Response:**
```typescript
{
  messageId: string,        // Unique identifier for the generated image
  url: string,             // Direct URL to generated image
  status: "completed",     // Generation status
  metadata: {
    width: number,         // Image width in pixels
    height: number,        // Image height in pixels
    model: string,         // AI model used
    prompt: string         // Original prompt used
  }
}
```

**Usage Examples:**
```bash
# Basic image generation
/generate-image prompt:"A serene mountain landscape at sunset"

# With specific dimensions
/generate-image prompt:"Modern office workspace" aspectRatio:"16:9"

# Reference previous generation
/generate-image messageId:"abc123" prompt:"Make the background more dramatic"
```

**Error Responses:**
- `INVALID_PROMPT`: Prompt violates content policy
- `RATE_LIMITED`: API rate limit exceeded
- `INSUFFICIENT_CREDITS`: Account has insufficient credits

---

### `create-variant`

Generate alternative interpretations of an existing image while maintaining the core concept.

**Parameters:**
```typescript
{
  messageId: string,        // Required: ID of image to create variants for
  count?: number           // Optional: Number of variants (default: 2, max: 4)
}
```

**Response:**
```typescript
{
  variants: [
    {
      messageId: string,    // Unique ID for this variant
      url: string,         // Direct URL to variant image
      status: "completed"
    }
  ],
  originalMessageId: string // Reference to original image
}
```

**Usage Examples:**
```bash
# Generate 2 variants (default)
/create-variant messageId:"abc123"

# Generate 4 variants
/create-variant messageId:"abc123" count:4
```

**Best Practices:**
- Use after initial generation to explore alternatives
- Combine with `/vary-it` command for guided variations
- Generate variants before upscaling to find the best version

---

### `reroll-image`

Regenerate an image using the same prompt but different random seed for different results.

**Parameters:**
```typescript
{
  messageId: string         // Required: ID of image to reroll
}
```

**Response:**
```typescript
{
  messageId: string,        // New unique ID for rerolled image
  url: string,             // Direct URL to new image
  status: "completed",
  originalPrompt: string,   // Original prompt reused
  metadata: {
    seed: number           // Random seed used for generation
  }
}
```

**Usage Examples:**
```bash
/reroll-image messageId:"abc123"
```

**Use Cases:**
- When initial result doesn't match vision
- Exploring different interpretations of same concept
- A/B testing with identical prompts

---

### `upscale-image`

Enhance image resolution and quality for production use.

**Parameters:**
```typescript
{
  messageId: string,        // Required: ID of image to upscale
  scale?: number           // Optional: Scale factor (default: 2, max: 4)
}
```

**Response:**
```typescript
{
  messageId: string,        // New unique ID for upscaled image
  url: string,             // Direct URL to enhanced image
  status: "completed",
  metadata: {
    originalWidth: number,
    originalHeight: number,
    newWidth: number,
    newHeight: number,
    scale: number
  }
}
```

**Usage Examples:**
```bash
# 2x upscale (default)
/upscale-image messageId:"abc123"

# 4x upscale for high-res printing
/upscale-image messageId:"abc123" scale:4
```

**Performance Notes:**
- Processing time: 30-120 seconds depending on scale
- File size increases significantly (4x scale = ~16x file size)
- Always upscale final versions, not variants during iteration

---

### `inpaint-image`

Modify specific regions of an existing image using a mask.

**Parameters:**
```typescript
{
  messageId: string,        // Required: ID of image to modify
  maskUrl: string,         // Required: URL to mask image (white = edit area)
  prompt: string,          // Required: Description of desired changes
  strength?: number        // Optional: Modification intensity (0.0-1.0, default: 0.8)
}
```

**Response:**
```typescript
{
  messageId: string,        // New unique ID for modified image
  url: string,             // Direct URL to inpainted image
  status: "completed",
  maskUrl: string,         // Reference to mask used
  prompt: string           // Changes applied
}
```

**Mask Requirements:**
- PNG format with transparency
- White areas = regions to modify
- Black/transparent areas = regions to preserve
- Same dimensions as original image

**Usage Examples:**
```bash
/inpaint-image messageId:"abc123" maskUrl:"https://example.com/mask.png" prompt:"Change the background to a beach scene"
```

**Advanced Use Cases:**
- Background replacement
- Object removal/addition
- Color correction in specific areas
- Text overlay preparation

---

### `generate-video`

Create smooth video animations from two compatible image frames.

**Parameters:**
```typescript
{
  startFrameId: string,     // Required: Message ID of start frame
  endFrameId: string,       // Required: Message ID of end frame
  duration?: number,        // Optional: Video length in seconds (default: 3)
  fps?: number             // Optional: Frames per second (default: 30)
}
```

**Response:**
```typescript
{
  messageId: string,        // Unique ID for generated video
  url: string,             // Direct URL to video file
  status: "completed",
  metadata: {
    duration: number,      // Video length in seconds
    fps: number,          // Frames per second
    startFrameId: string, // Reference to start frame
    endFrameId: string    // Reference to end frame
  }
}
```

**Frame Compatibility Requirements:**
- Same camera angle and perspective
- Compatible lighting conditions
- Similar color palette
- Logical transformation path
- Matching composition where possible

**Usage Examples:**
```bash
# Basic 3-second video
/generate-video startFrameId:"frame1" endFrameId:"frame2"

# Longer 5-second video
/generate-video startFrameId:"frame1" endFrameId:"frame2" duration:5
```

**Best Practices:**
- Upscale frames before video generation
- Test frame compatibility with static comparison
- Use Video Director agent for complex sequences

---

### `fetch-status`

Check the status of long-running generation jobs.

**Parameters:**
```typescript
{
  messageId: string         // Required: ID of job to check
}
```

**Response:**
```typescript
{
  messageId: string,
  status: "pending" | "processing" | "completed" | "failed",
  progress?: number,       // Percentage complete (0-100)
  estimatedTimeRemaining?: number, // Seconds remaining
  result?: {               // Only present when completed
    url: string,
    metadata: object
  },
  error?: string          // Only present when failed
}
```

**Usage Examples:**
```bash
/fetch-status messageId:"abc123"
```

**Common Status Values:**
- `pending`: Job queued, waiting to start
- `processing`: Currently generating (includes progress %)
- `completed`: Finished successfully
- `failed`: Generation failed (check error field)

---

### `imagine-gemini`

Multi-modal generation combining text prompts with reference images using Gemini.

**Parameters:**
```typescript
{
  prompt: string,          // Required: Text description
  referenceImageUrl?: string, // Optional: Reference image URL
  styleReference?: string, // Optional: Style to emulate
  mode?: "generate" | "variations" | "enhance"  // Optional: Generation mode
}
```

**Response:**
```typescript
{
  messageId: string,
  url: string,
  status: "completed",
  metadata: {
    model: "gemini",
    referenceImageUsed: boolean,
    mode: string
  }
}
```

**Usage Examples:**
```bash
# Style transfer
/imagine-gemini prompt:"A city skyline in the style of van gogh" referenceImageUrl:"https://example.com/vangogh.jpg"

# Enhancement
/imagine-gemini prompt:"Improve the lighting and colors" referenceImageUrl:"https://example.com/photo.jpg" mode:"enhance"
```

## Authentication

All tools require a valid `IMAGINEPRO_API_KEY` environment variable:

```bash
export IMAGINEPRO_API_KEY="sk-your-api-key-here"
```

## Rate Limits & Credits

- **Rate Limit**: 10 requests per minute
- **Credit Usage**: Varies by tool and parameters
- **Billing**: Pay-per-use based on generation complexity

**Approximate Credit Costs:**
- `generate-image`: 1-5 credits (based on resolution)
- `upscale-image`: 2-8 credits (based on scale factor)
- `generate-video`: 10-20 credits (based on duration)
- `inpaint-image`: 3-7 credits

## Error Handling

### Common Error Codes

```typescript
{
  code: "INVALID_API_KEY",
  message: "The provided API key is invalid or expired"
}

{
  code: "RATE_LIMIT_EXCEEDED",
  message: "Too many requests. Please wait before retrying.",
  retryAfter: 60  // seconds to wait
}

{
  code: "INSUFFICIENT_CREDITS",
  message: "Account has insufficient credits for this operation"
}

{
  code: "CONTENT_POLICY_VIOLATION",
  message: "The prompt violates content generation policies"
}

{
  code: "INVALID_PARAMETERS",
  message: "One or more parameters are invalid",
  details: { field: "prompt", reason: "cannot be empty" }
}
```

### Error Recovery

```typescript
// Example error handling
try {
  const result = await generateImage({ prompt: "example" });
  // Handle success
} catch (error) {
  if (error.code === "RATE_LIMIT_EXCEEDED") {
    // Wait and retry
    await new Promise(resolve => setTimeout(resolve, error.retryAfter * 1000));
    return retryGeneration();
  }
  // Handle other errors
}
```

## Best Practices

### Performance Optimization
1. **Batch Operations**: Generate multiple variants at once rather than sequentially
2. **Upscale Last**: Only upscale final selected images
3. **Cache Results**: Store successful generations for reuse
4. **Monitor Credits**: Track usage to avoid unexpected limits

### Quality Enhancement
1. **Specific Prompts**: Include style, lighting, composition details
2. **Reference Images**: Use existing images for style consistency
3. **Iterative Refinement**: Generate → vary → select → upscale
4. **Platform Optimization**: Match dimensions to target platforms

### Cost Management
1. **Preview First**: Generate at standard quality before upscaling
2. **Batch Variants**: Create multiple options efficiently
3. **Selective Enhancement**: Only upscale images you'll use
4. **Monitor Usage**: Track spending against budget

## Integration Examples

### Complete Image Workflow
```typescript
// 1. Generate initial image
const image1 = await generateImage({
  prompt: "Modern office workspace, collaborative team"
});

// 2. Create variants for selection
const variants = await createVariant({
  messageId: image1.messageId,
  count: 3
});

// 3. Select best variant and enhance
const final = await upscaleImage({
  messageId: variants.variants[0].messageId, // Best variant
  scale: 2
});
```

### Video Creation Workflow
```typescript
// 1. Generate compatible frames
const startFrame = await generateImage({
  prompt: "Product in box, studio lighting, centered"
});

const endFrame = await generateImage({
  prompt: "Same product revealed, identical lighting and angle"
});

// 2. Create video
const video = await generateVideo({
  startFrameId: startFrame.messageId,
  endFrameId: endFrame.messageId,
  duration: 5
});
```

## Support & Resources

- **Documentation**: https://imaginepro.ai/docs
- **API Status**: https://status.imaginepro.ai
- **Community**: https://github.com/imaginpro/imaginepro-claude-plugin/discussions
- **Support**: support@imaginepro.ai

## Version History

- **v1.0.0**: Initial release with 8 core tools
- **v1.1.0**: Added Gemini multi-modal generation
- **v1.2.0**: Enhanced video generation with custom durations
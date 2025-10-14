Create a complete video animation from a description - automates the full workflow from concept to finished video.

This command handles the entire video generation pipeline: concept analysis, start frame generation, compatible end frame generation, and smooth video transition creation.

## Usage

```bash
/video-flow [description of video transformation]
```

## What It Does

`/video-flow` automates the complete video creation process:

1. **Analyzes** your video concept
2. **Generates** optimized start frame
3. **Generates** compatible end frame (matching composition, lighting, style)
4. **Creates** smooth video transition
5. **Returns** video URL with message ID

This saves you from manually:
- Generating separate frames
- Ensuring frame compatibility
- Managing multiple message IDs
- Coordinating the complete workflow

## Examples

### Product Transformations
```
/video-flow smartphone transforming from off to glowing with colorful display
/video-flow wireless earbuds emerging from premium charging case
/video-flow plain laptop to high-tech gaming laptop with RGB lighting
```

### Environmental Changes
```
/video-flow city skyline transitioning from day to night with lights turning on
/video-flow mountain landscape changing from summer to winter
/video-flow beach scene from sunny afternoon to beautiful sunset
```

### Abstract Animations
```
/video-flow geometric shapes morphing from simple circle to complex flower pattern
/video-flow minimalist logo expanding into full brand lockup
/video-flow abstract waves flowing from calm to energetic motion
```

### Brand & Marketing
```
/video-flow brand logo revealing from dark minimalist to vibrant colored version
/video-flow product before and after transformation showing improvement
/video-flow empty workspace to productive organized home office
```

### App Animations
```
/video-flow meditation app loading lotus flower blooming open
/video-flow fitness app progress bar filling with energy and momentum
/video-flow task completion checkmark appearing with celebration effect
```

## How To Describe Transformations

### Be Clear About States
✅ **Good**: "coffee cup from empty to full with steam rising"
❌ **Vague**: "coffee cup animation"

✅ **Good**: "moon transitioning through phases from new to full"
❌ **Vague**: "moon changing"

### Describe the Movement
✅ **Good**: "flower petals gently opening from closed bud"
❌ **Generic**: "flower blooming"

✅ **Good**: "curtain smoothly pulling aside to reveal window view"
❌ **Generic**: "curtain opening"

### Specify Style
✅ **Good**: "logo reveal with cinematic 3D depth and lighting"
❌ **Missing**: "logo reveal"

✅ **Good**: "product transformation in clean studio photography style"
❌ **Missing**: "product changing"

## Use Cases

### Web Development
```
# Hero section background video
/video-flow abstract gradient waves flowing smoothly, purple to blue color shift

# Loading animation
/video-flow progress circle filling from 0 to 100 percent with smooth motion

# Feature reveal
/video-flow app interface transitioning from desktop to mobile responsive view
```

### Product Marketing
```
# Product reveal
/video-flow premium watch emerging from elegant gift box, studio lighting

# Before/After demonstration
/video-flow messy workspace transforming to organized minimal desk setup

# Feature highlight
/video-flow software dashboard from basic to advanced with features activating
```

### Brand Videos
```
# Logo animation
/video-flow company logo assembling from scattered geometric pieces

# Brand story
/video-flow seed growing into flourishing tree, metaphor for growth

# Season branding
/video-flow winter holiday themed scene to spring fresh aesthetic
```

### UI/UX Animation
```
# Onboarding
/video-flow welcome screen with app logo animating into main interface

# Empty to filled state
/video-flow empty inbox illustration to notification arriving with subtle motion

# Success animation
/video-flow loading spinner to success checkmark with celebratory feel
```

## What to Expect

### Timeline
- **Start frame generation**: ~30-60 seconds
- **End frame generation**: ~30-60 seconds
- **Video generation**: ~1-3 minutes
- **Total**: ~2-5 minutes for complete video

### Output
- **Format**: Video file (typically MP4)
- **Duration**: Usually 3-5 seconds
- **Quality**: HD resolution
- **Message ID**: For reference and potential regeneration

### Frame Compatibility
The command automatically ensures:
- Matching camera angles
- Compatible lighting
- Consistent color grading
- Similar composition
- Smooth transition potential

## Best Practices

### Do:
✅ Describe a clear transformation (A → B)
✅ Specify style (photorealistic, 3D render, illustration)
✅ Mention desired mood or energy
✅ Keep transformations focused (one main change)
✅ Consider where the video will be used

### Don't:
❌ Request multiple unrelated changes
❌ Use overly complex transformations
❌ Forget to specify visual style
❌ Expect instant results (video takes time)
❌ Request very long duration videos (AI works best with 3-7s)

## Advanced Tips

### Looping Videos
```
# Describe full-circle transformations
/video-flow day to night city, suitable for seamless loop

# Create reversible animations
/video-flow flower opening (can be played forward/backward)
```

### Platform Optimization
```
# For social media
/video-flow [description], optimized for Instagram Stories vertical format

# For website backgrounds
/video-flow [description], subtle ambient motion for web background

# For product pages
/video-flow [description], clean professional product reveal
```

### Cinematic Quality
```
# Add cinematography keywords
/video-flow [description], cinematic camera movement, professional lighting

# Specify mood
/video-flow [description], dramatic and epic feel

# Define energy level
/video-flow [description], smooth and calm vs. energetic and dynamic
```

## Troubleshooting

### If transition seems jarring:
- Try describing a more gradual transformation
- Simplify the concept (fewer elements changing)
- Ensure start/end states are visually related

### If video takes too long:
- Normal for complex transformations (up to 3 minutes)
- You can continue working on other tasks
- Use `fetch-status` to check progress

### If you want more control:
- Use the Video Director agent directly
- Manually generate and refine frames first
- Then create video with `generate-video` MCP tool

## Manual Workflow (Alternative)

If you need more control, work with the Video Director agent:

```
# Activate Video Director agent
"I need to create a video showing [concept]. Let's design the frames carefully."

# Agent will guide you through:
1. Start frame generation
2. End frame review and compatibility check
3. End frame adjustments if needed
4. Video generation with optimized settings
```

## Related Commands

- `/imagine-pro` - Generate individual frames manually
- `/vary-it` - Adjust frames before creating video
- `/upscale-it` - Enhance frame quality (recommended before video)
- `/imagine-guide` - Learn video creation strategies

## Performance Notes

- **Credit Usage**: Uses credits for 2 images + 1 video
- **Processing Time**: 2-5 minutes total
- **Quality**: Consider upscaling frames first for premium results
- **File Size**: Videos are larger than images (typically 1-5MB)

## Quick Reference

```bash
# Basic usage
/video-flow sunrise to sunset over mountain lake

# With style
/video-flow logo reveal, cinematic 3D render style

# Product focused
/video-flow headphones from box to wearing, studio photography

# Abstract
/video-flow geometric pattern morphing, blue to purple gradient

# Brand animation
/video-flow company name appearing with dynamic motion
```

## Example Workflow

```
# Step 1: Create video
/video-flow product reveal: smartphone from box to glowing screen

# Step 2: Review result (msg-video-123)
# If frames need adjustment:

# Step 3: Work with Video Director for refinement
"Can we regenerate the end frame with brighter screen glow?"

# Step 4: Recreate video with improved frames
# Step 5: Use in production!
```

## Where to Use Your Videos

- **Website backgrounds**: Ambient, subtle animations
- **Hero sections**: Attention-grabbing reveal animations
- **Product pages**: Product transformations and reveals
- **Social media**: Instagram/Facebook ads and stories
- **Presentations**: Slide transitions and reveals
- **App interfaces**: Loading, transitions, celebrations
- **Email marketing**: Animated headers (GIF export)
- **Digital signage**: Looping brand content

`/video-flow` makes professional video creation accessible without complex video editing software or frame management!

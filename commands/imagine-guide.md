Get interactive guidance on using ImaginePro effectively in Claude Code.

This command provides a comprehensive learning experience for mastering AI image and video generation workflows, best practices, and prompt engineering techniques.

## Usage

```bash
/imagine-guide

# Or ask specific questions:
/imagine-guide [your question]
```

## What You'll Learn

### 1. Prompt Engineering Fundamentals
- How to write effective prompts for better results
- Essential keywords and descriptors
- Style specifications (photorealistic, illustration, 3D, etc.)
- Composition and layout guidance
- Quality and detail modifiers

### 2. Workflow Mastery
- Complete workflows for common tasks
- When to use each command and MCP tool
- Iteration strategies (generate → vary → refine → upscale)
- A/B testing approaches
- Quality optimization techniques

### 3. Use Case Specific Guidance
- **Web Development**: Hero images, backgrounds, assets
- **UI/UX Design**: Icons, illustrations, empty states, onboarding
- **Marketing**: Ads, social media, email headers, campaigns
- **Video Production**: Animations, transitions, reveals

### 4. Platform Optimization
- Dimension requirements for each platform
- Format specifications (Instagram, Facebook, web, email)
- Mobile vs. desktop considerations
- Accessibility best practices

### 5. Advanced Techniques
- Multi-asset campaigns
- Brand consistency across generations
- Frame compatibility for video
- Performance optimization

## Example Interactions

### Getting Started
```
User: /imagine-guide

Guide: Welcome to the ImaginePro Interactive Guide!

I can help you with:

📚 **Learn the Basics**
- Prompt engineering fundamentals
- Understanding the generation workflow
- Best practices for quality results

🎯 **Specific Use Cases**
- Web asset creation (hero images, backgrounds)
- UI/UX design (icons, illustrations)
- Marketing content (ads, social media)
- Video animation creation

🔧 **Tools & Commands**
- When to use /imagine-pro vs /vary-it
- Upscaling strategies
- Video workflow optimization

❓ **Common Questions**
- "How do I create a hero image for my landing page?"
- "What's the best workflow for making consistent icons?"
- "How can I generate better marketing ads?"
- "Tips for smooth video transitions?"

What would you like to learn about?
```

### Specific Question Example 1
```
User: /imagine-guide How do I create a hero image?

Guide: Great question! Here's the complete workflow for creating professional
hero images for web development:

## Hero Image Creation Workflow

### Step 1: Define Requirements
Consider:
- Dimensions: 1920x1080 minimum (full HD)
- Where will text overlay appear? (usually upper or lower third)
- Brand colors or mood
- Target audience and message

### Step 2: Generate with /imagine-pro
Example prompt structure:
```
/imagine-pro [subject/scene], [style], [composition details],
[color palette], [lighting], space for text overlay in [position],
[quality modifiers]
```

**Real example**:
```
/imagine-pro modern collaborative workspace, professional team working
on laptops, clean minimalist aesthetic, blue and white color scheme,
natural lighting, wide composition with negative space in upper third
for headline text, photorealistic, high quality, 4k
```

### Step 3: Review and Refine
- Check if text overlay areas are clear
- Ensure focal point doesn't compete with CTA
- Verify mood matches brand

If needed:
```
/vary-it [messageId] adjust lighting to be brighter
/vary-it [messageId] more negative space in upper third
```

### Step 4: Production Quality
```
/upscale-it [best-messageId]
```

### Step 5: Implementation Tips
- Export at 2x and 3x for retina displays
- Optimize file size (aim for <300KB)
- Test with actual headline text overlaid
- Ensure mobile responsiveness

**Pro Tips for Hero Images:**
✅ Leave ample space for text (upper third or lower third)
✅ Avoid busy backgrounds that compete with headline
✅ Use mood that matches product/service personality
✅ Consider different versions for A/B testing
✅ Ensure high contrast for text readability

Want to try generating your hero image now? Tell me about your project!
```

### Specific Question Example 2
```
User: /imagine-guide best practices for making icon sets

Guide: Excellent! Creating consistent icon sets requires a systematic approach.
Here's how to master it:

## Icon Set Creation Best Practices

### Key Principles
1. **Consistency is Critical**: Same style, line weight, visual density across all icons
2. **Clarity at Small Sizes**: Icons must be recognizable at 16-24px
3. **Distinctive Silhouettes**: Each icon clearly different from others
4. **Optical Balance**: Not just geometric centering

### Recommended Workflow

**Step 1: Define Your Style**
Decide on:
- Line style: Minimal line, filled, outlined, rounded
- Line weight: Thin (2px), medium (3px), thick (4px) at 64px scale
- Color: Monochrome (recommended) or multi-color
- Corners: Sharp, rounded, or mixed

**Step 2: Generate Icons Sequentially**
Use Web Asset Producer or UI/UX Asset Generator agents.

Example for first icon:
```
/imagine-pro minimal line icon for home navigation, simple house
symbol, clean geometric lines, 3px stroke weight, monochrome black,
centered composition on white background, 64x64 resolution, icon design
```

**Step 3: Generate Remaining Icons WITH SAME DESCRIPTORS**
Critical: Use identical style descriptors!

```
/imagine-pro minimal line icon for [search] navigation, simple
[magnifying glass] symbol, clean geometric lines, 3px stroke weight,
monochrome black, centered composition on white background, 64x64
resolution, icon design, MATCHING STYLE of previous icon
```

Repeat for all icons in set.

**Step 4: Review for Consistency**
Check:
- ✓ Same line weight across all icons
- ✓ Similar visual complexity
- ✓ Consistent spacing/padding
- ✓ Matching style and mood

If inconsistent:
```
/vary-it [outlier-icon-id] match the line weight of the other icons
```

**Step 5: Upscale Set**
```
/upscale-it [icon-1-id]
/upscale-it [icon-2-id]
# ... for all icons
```

### Common Icon Mistakes to Avoid

❌ **Mixing styles** in the same set
✅ Define style once, apply to all

❌ **Too much detail** (becomes muddy at small sizes)
✅ Keep simple, focus on recognizable shapes

❌ **Inconsistent line weight** (some thick, some thin)
✅ Use exact same stroke weight descriptor

❌ **Poor optical centering** (geometrically centered but looks off)
✅ Use "optical balance" in prompts

### Icon Set Sizes to Export
- **1x**: 24px (baseline)
- **2x**: 48px (retina)
- **3x**: 72px (high-res displays)

Start from your 64px generated icons, then scale down with your design tool.

### Recommended Icon Dimensions by Use Case
- **Navigation**: 24-32px displayed
- **Feature highlights**: 48-64px displayed
- **App icons**: 512px+ (upscale heavily)
- **Toolbar**: 16-24px displayed

Want me to help you generate an icon set? Tell me how many icons and what they represent!
```

### Specific Question Example 3
```
User: /imagine-guide tips for better video transitions

Guide: Video transitions can make or break your animation! Here's what makes
them smooth:

## Smooth Video Transition Mastery

### The Golden Rule
**Frame compatibility is everything.** Your start and end frames must be designed
as a pair, not independently.

### Critical Compatibility Factors

**1. Camera Angle Must Match**
❌ Start frame: eye-level view
❌ End frame: aerial view
✅ Both frames: exact same camera position

**2. Lighting Should Be Consistent or Intentionally Transitional**
✅ Same lighting (product reveal)
✅ Gradual change (day → night)
❌ Completely different lighting with no relationship

**3. Composition Should Align**
✅ Subject in same relative position
✅ Background elements aligned
❌ Subject moves drastically across frame

**4. Color Palette Should Flow**
✅ Same colors
✅ Gradual palette shift (blue → purple → pink)
❌ Jarring unrelated colors

**5. Perspective Must Be Preserved**
✅ Same 3D perspective and depth
❌ Flat → 3D or vice versa (unless intentional)

### Workflow for Smooth Transitions

**Option A: Use /video-flow** (Automatic)
```
/video-flow clear description of transformation including style
```
The command handles frame compatibility automatically.

**Option B: Work with Video Director Agent** (Manual Control)
```
# Activate agent
"I need to create a video showing [concept]"

# Agent guides you through:
1. Planning the transformation
2. Generating compatible start frame
3. Generating matching end frame
4. Creating the video
```

### What Transitions Work Best

**Excellent for Smooth Transitions:**
- ✅ Day → Night (same scene, lighting changes)
- ✅ Product states (off → on, closed → open)
- ✅ Seasonal changes (summer → winter landscape)
- ✅ Progressive reveals (logo assembly, building up)
- ✅ Color shifts (blue mood → warm mood)
- ✅ Simple morphs (circle → flower, geometric evolution)

**Challenging Transitions:**
- ⚠️ Complete scene changes (office → beach)
- ⚠️ Different camera angles
- ⚠️ Unrelated subjects (car → plane)
- ⚠️ Dramatically different compositions

### Pro Tips

**Tip 1: Design End Frame to Match Start**
Don't generate end frame independently! Reference the start frame explicitly:

```
/imagine-pro [end state description], SAME CAMERA ANGLE as previous
image, matching lighting and composition, same background elements,
identical perspective
```

**Tip 2: Use Consistent Style Descriptors**
Both frames should use identical style keywords:
- "photorealistic" in both or neither
- "studio lighting" in both
- "clean white background" in both

**Tip 3: Consider Upscaling Frames First**
```
/imagine-pro [start frame]  → msg-start
/upscale-it msg-start       → msg-start-hd
/imagine-pro [end frame]    → msg-end
/upscale-it msg-end         → msg-end-hd
# Then generate video from HD frames
```

Higher quality frames often = smoother video.

**Tip 4: Test with Simple Transformations First**
Master simple transitions before complex ones:
1. Start: Color change (blue sphere → red sphere)
2. Then: State change (closed flower → open flower)
3. Then: Scene evolution (day → night)
4. Finally: Complex narratives

Want to create a video together? Describe your concept and I'll guide you through
ensuring smooth, professional transitions!
```

## Topics You Can Ask About

### Prompt Engineering
- "How do I write better prompts?"
- "What keywords improve quality?"
- "How specific should I be?"

### Workflows
- "What's the typical workflow for [use case]?"
- "When should I upscale vs. create variants?"
- "How do I iterate effectively?"

### Use Cases
- "How to create web hero images?"
- "Best approach for icon sets?"
- "Creating marketing ads workflow?"
- "Video generation best practices?"

### Technical
- "What dimensions for Instagram ads?"
- "How to ensure brand consistency?"
- "Tips for accessibility?"
- "Platform-specific optimization?"

### Troubleshooting
- "Why are my icons inconsistent?"
- "How to improve video smoothness?"
- "My images don't match my vision - what to do?"
- "How to make colors more vibrant?"

## Learning Paths

### Beginner Path
1. Start here: Basic prompt engineering
2. Then: Simple image generation workflow
3. Next: Upscaling and quality
4. Finally: Variations and refinement

### Intermediate Path
1. Platform-specific optimization
2. Multi-asset campaigns
3. A/B testing strategies
4. Brand consistency techniques

### Advanced Path
1. Complex video workflows
2. Design system creation
3. Advanced prompt engineering
4. Performance optimization

## Quick Tips Reference

### Prompt Engineering
- Be specific about style, composition, lighting, colors
- Include quality keywords: "high quality", "4k", "professional"
- Mention where text will overlay
- Specify mood and emotion

### Commands
- `/imagine-pro`: Start with guidance
- `/vary-it`: Explore alternatives
- `/upscale-it`: Production quality
- `/video-flow`: Complete video workflow

### Workflow
1. Generate → 2. Vary → 3. Choose → 4. Upscale → 5. Use

### Quality
- Generate at standard quality first
- Create variants before upscaling
- Only upscale final/winning versions
- Test before committing to upscale

## Related Commands

- `/imagine-pro` - Put learning into practice
- `/vary-it` - Iterate on generations
- `/upscale-it` - Finalize assets
- `/video-flow` - Create videos

---

**Ready to learn?** Ask me any question about ImaginePro workflows, or say "I want to create [type of asset]" and I'll guide you through the complete process!

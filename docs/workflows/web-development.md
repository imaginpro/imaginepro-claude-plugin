# Web Development Workflow

Complete guide to creating web assets with the ImaginePro plugin.

## Overview

Web development requires various visual assets: hero images, backgrounds, feature section images, CTA backgrounds, and more. This guide shows you how to create professional, web-optimized assets efficiently.

## Quick Reference

| Asset Type | Recommended Size | Best Approach |
|------------|------------------|---------------|
| Hero Image | 1920x1080+ | Web Asset Producer agent |
| Background | 1920x1080 - 4K | Web Asset Producer + subtle keyword |
| Feature Section | 1200x675 | /imagine-pro with context |
| OG Image | 1200x630 | /imagine-pro + upscale |
| Blog Featured | 1200x675 | /imagine-pro + brand aligned |
| CTA Section | Variable | Marketing Creative agent |

## Complete Workflows

### Hero Image Creation

**Goal**: Create a professional hero image for your landing page

**Workflow**:

```
Step 1: Activate Web Asset Producer
"I need a hero image for my [type] website"

Step 2: Agent asks clarifying questions:
- Website purpose (SaaS, portfolio, e-commerce, etc.)
- Target mood (professional, friendly, innovative)
- Brand colors
- Text overlay needs

Step 3: Agent generates optimized image:
- Proper dimensions (1920x1080)
- Appropriate composition
- Space for text
- Brand-aligned aesthetic

Step 4: Review and refine:
/vary-it [msg-id] if adjustments needed

Step 5: Production quality:
/upscale-it [final-msg-id]
```

**Alternative - Direct Command**:
```bash
/imagine-pro modern [your industry] landing page hero image, [describe scene],
[brand colors], [mood], space for headline text in [position], 1920x1080,
photorealistic, professional photography, high quality
```

**Example**:
```bash
/imagine-pro modern SaaS collaboration platform hero image, diverse professional
team working together in bright modern office, laptops and large screen visible,
blue and white color scheme, innovative and productive atmosphere, space for
headline text in upper third, 1920x1080, photorealistic, professional photography,
high quality, natural lighting
```

### Background Pattern/Texture

**Goal**: Subtle background for sections

**Workflow**:

```bash
/imagine-pro subtle [style] background pattern for web, [colors],
minimalist and non-distracting, seamless tileable design if possible,
high resolution, barely visible texture, professional clean aesthetic

# Example:
/imagine-pro subtle geometric background pattern for web, soft blue and
purple gradient, minimalist hexagonal shapes, barely visible, seamless
tileable design, 4K resolution, modern tech aesthetic, clean professional
```

**Tips**:
- Use "subtle", "barely visible", "non-distracting"
- Mention it's for web background
- Specify tileability if needed
- Higher resolution (4K) works better
- Test file size after download

### Feature Section Images

**Goal**: Images for 3-column feature sections

**Workflow**:

```
Step 1: Plan your 3 features
- Feature 1: Security
- Feature 2: Speed
- Feature 3: Collaboration

Step 2: Generate each with consistent style:
/imagine-pro illustration representing [feature concept], modern flat style,
[brand colors], clean minimalist composition, 600x400, professional,
icon-style illustration, white or subtle background

Step 3: Ensure visual consistency:
Use same style keywords for all 3:
- "modern flat style"
- "clean minimalist"
- Same color palette
- Same dimensions

Step 4: Upscale set:
/upscale-it [feature-1-msg]
/upscale-it [feature-2-msg]
/upscale-it [feature-3-msg]
```

**Example Set**:
```bash
# Security Feature
/imagine-pro illustration representing digital security and protection,
modern flat style, blue accent colors, shield and lock metaphor, clean
minimalist composition, 600x400, professional icon-style illustration,
white background

# Speed Feature
/imagine-pro illustration representing high speed and performance,
modern flat style matching previous image, blue accent colors, lightning
or rocket metaphor, clean minimalist composition, 600x400, professional
icon-style illustration, white background, consistent with security illustration

# Collaboration Feature
/imagine-pro illustration representing team collaboration and communication,
modern flat style matching set, blue accent colors, connected people metaphor,
clean minimalist composition, 600x400, professional icon-style illustration,
white background, consistent with previous illustrations
```

### Call-to-Action Section Background

**Goal**: Eye-catching but not overwhelming CTA background

**Workflow**:

```bash
/imagine-pro energetic gradient background for call-to-action section,
[brand colors], vibrant but professional, supports button and text overlay,
suitable for conversion focus, modern aesthetic, 1920x600 or full width,
high quality

# Example:
/imagine-pro energetic gradient background for CTA section, blue to purple
gradient flow, vibrant yet professional, modern abstract geometric elements,
supports white text and button overlay, conversion-focused aesthetic, dynamic
but not distracting, 1920x600, high quality
```

### About Page / Team Section

**Goal**: Humanizing, professional images

**Workflow**:

```bash
/imagine-pro professional [context] scene for about page, [describe atmosphere],
warm and approachable feel, modern office or workspace, diversity and inclusion,
authentic and relatable, photorealistic, professional photography, natural lighting

# Example:
/imagine-pro professional team collaboration scene for about page, diverse group
in modern bright office discussing ideas around table, warm and approachable
atmosphere, authentic interaction, inclusive representation, natural window
lighting, professional photography style, high quality, friendly and professional
mood
```

## Complete Landing Page Asset Set

**Scenario**: Building a SaaS landing page

**Asset Checklist**:
- [ ] Hero image (1920x1080)
- [ ] 3 Feature section illustrations (600x400 each)
- [ ] CTA background (1920x600)
- [ ] Testimonial section background (optional)
- [ ] About/Team image (1200x800)
- [ ] Footer background pattern (optional)

**Workflow**:

```
Step 1: Activate Web Asset Producer
"I'm building a SaaS landing page and need a complete asset set. The product
is [describe product], target audience is [describe audience], brand colors
are [colors], and the mood should be [professional/friendly/innovative/etc.]"

Step 2: Agent creates a cohesive plan:
- Hero image concept
- Feature illustration style
- CTA approach
- Additional assets

Step 3: Generate assets systematically:
Agent guides through each asset with consistency

Step 4: Review and refine:
Make adjustments with /vary-it as needed

Step 5: Upscale final set:
/upscale-it for all approved assets

Step 6: Download and implement:
Use assets in your landing page
```

## Best Practices

### Dimensions

**Hero Sections**:
- Minimum: 1920x1080 (Full HD)
- Recommended: 2560x1440 (for 4K displays)
- Ultra-wide: 3440x1440 (for wide screens)

**Feature Sections**:
- Card images: 400x300 or 600x400
- Full-width features: 1200x675

**Backgrounds**:
- Patterns: Tileable or 4K (3840x2160)
- Section backgrounds: 1920x1080

**Social/SEO**:
- Open Graph: 1200x630
- Twitter Card: 1200x675

### Composition

**For Text Overlays**:
- Specify "space for headline in [upper/lower] third"
- Mention "room for CTA button"
- Use "negative space" keywords

**Visual Hierarchy**:
- Clear focal point (doesn't compete with text)
- Sufficient contrast for readability
- Mobile-friendly composition (test at small sizes)

### Style Consistency

**Maintain across assets**:
- Color palette (use brand colors)
- Photography style OR illustration style (don't mix)
- Mood and energy level
- Level of detail and complexity

**Example Consistent Set**:
```
All assets use:
- Modern flat illustration style
- Blue and purple brand colors
- Clean minimalist compositions
- Professional but approachable mood
```

### Performance

**Optimization**:
- Generate at needed size (don't oversized unnecessarily)
- Upscale only final versions
- Compress after download (aim for <300KB for web)
- Use modern formats (WebP with fallbacks)
- Consider lazy loading for below-fold images

**Testing**:
- Test with actual text overlaid
- Check mobile responsiveness
- Verify contrast for accessibility
- Test loading speed

## Common Prompts

### Hero Images by Industry

**SaaS/Tech**:
```bash
/imagine-pro modern SaaS platform interface on laptop screen, clean minimal
workspace, professional developer working, blue tech aesthetic, innovative mood,
space for headline top third, 1920x1080, professional photography, high quality
```

**E-commerce**:
```bash
/imagine-pro lifestyle product photography, person happily using [product type],
natural home environment, warm inviting atmosphere, authentic moment, space for
headline and CTA, 1920x1080, professional photography, natural lighting
```

**Agency/Services**:
```bash
/imagine-pro creative professionals collaborating in modern bright office,
brainstorming session, diverse team, energy and innovation, warm professional
atmosphere, space for headline text, 1920x1080, professional photography
```

**Portfolio/Personal**:
```bash
/imagine-pro minimal elegant workspace setup, laptop with clean interface,
coffee and notebook, creative professional atmosphere, aspirational aesthetic,
negative space for text overlay, 1920x1080, professional photography, natural light
```

### Backgrounds

**Subtle Patterns**:
```bash
/imagine-pro subtle geometric pattern background, [brand colors], barely visible
texture, seamless tileable, modern minimalist, professional web aesthetic, 4K
```

**Gradients**:
```bash
/imagine-pro smooth gradient background, [color 1] to [color 2], modern clean
aesthetic, subtle flow, professional web design, high resolution
```

**Abstract**:
```bash
/imagine-pro abstract flowing shapes background, [brand colors], soft and subtle,
non-distracting, modern aesthetic, suitable for text overlay, web optimized
```

## Workflow Optimization

### A/B Testing Heroes

```
Generate 3 hero variants for testing:

Variant A: Scene-based
/imagine-pro [detailed scene with people/environment]

Variant B: Product-focused
/imagine-pro [product/interface prominently displayed]

Variant C: Abstract/Conceptual
/imagine-pro [metaphorical representation of value prop]

Test all three with same copy
Scale winner
```

### Batch Asset Creation

```
1. Define complete asset list
2. Work with Web Asset Producer agent
3. Generate all assets in one session (consistency)
4. Review complete set together
5. Batch upscale approved assets
6. Implement as cohesive set
```

### Iteration Strategy

```
Round 1: Generate initial assets (standard quality)
Round 2: Review with team, gather feedback
Round 3: Refine with /vary-it based on feedback
Round 4: Upscale finals with /upscale-it
Round 5: Implement and test on actual site
```

## Next Steps

- See [UI/UX Workflow](ui-ux-design.md) for icons and illustrations
- See [Marketing Workflow](marketing-content.md) for ads and social
- Check [Prompt Library](../prompt-library/) for more examples
- Review [Examples](../../examples/) for real project walkthroughs

---

**Pro Tip**: Always upscale and test hero images with your actual headline text overlaid before finalizing. What looks good standalone may not work with text!

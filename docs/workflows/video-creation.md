# Video Creation Workflow

Complete guide to creating video animations with the ImaginePro plugin.

## Overview

Video content creates dynamic, engaging experiences that static images can't match. This guide shows you how to create professional video animations using ImaginePro's video generation capabilities - from product reveals to loading animations to environmental transformations.

## Quick Reference

| Video Type | Typical Duration | Best Approach |
|------------|------------------|---------------|
| Product Reveal | 3-5 seconds | Video Director agent |
| Logo Animation | 2-4 seconds | /video-flow with simple concept |
| Loading Animation | 2-3 seconds (looped) | Video Director agent |
| Environmental Change | 4-6 seconds | /video-flow with locked camera |
| UI Transition | 1-3 seconds | Video Director for frame design |
| Explainer Sequence | 3-5 seconds per segment | Video Director agent |
| Brand Video Clip | 4-7 seconds | Video Director with storyboard |

## Understanding Video Generation

### The Process

**ImaginePro video generation works in 3 steps**:

```
1. Create Start Frame (image)
   ↓
2. Create End Frame (image that's compatible with start)
   ↓
3. Generate Video (smooth transition between frames)
```

### Critical Success Factor: Frame Compatibility

**For smooth videos, your start and end frames MUST have**:
- ✅ Same camera angle and perspective
- ✅ Compatible lighting (or intentional shift)
- ✅ Same background elements in same positions
- ✅ Consistent color grading
- ✅ Matching composition and framing
- ✅ Subject in related positions

**What changes between frames**:
- Subject state/position (slightly)
- Time-based elements (lighting, sky, shadows)
- Product state (boxed → unboxed, off → on)
- Specific transformations you want to show

## Complete Workflows

### Product Reveal Video

**Goal**: Showcase product transformation or reveal

**Workflow**:

```
Step 1: Activate Video Workflow Director
"Create a video showing [product transformation]"

Step 2: Agent asks clarifying questions:
- What's the product?
- What transformation to show?
- Style (product photography, lifestyle, studio)
- Brand colors?
- Duration target?
- Where will video be used?

Step 3: Agent storyboards:
- Defines start state clearly
- Defines end state clearly
- Plans matching elements for smooth transition
- Ensures compatibility

Step 4: Generate start frame:
Agent creates first frame with consideration for
the planned end state and transition

Step 5: Generate end frame:
Agent creates second frame specifically matching
camera angle, lighting, and composition of start

Step 6: Generate video:
Agent calls video generation tool with both frames
and clear transition description

Step 7: Review and refine:
- Video plays smoothly?
- Transition makes sense?
- Duration appropriate?
- Quality sufficient?

If adjustments needed, agent can regenerate frames
```

**Alternative - Direct /video-flow Command**:

```bash
/video-flow [clear transformation description from A to B]

# Examples:
/video-flow wireless headphones transforming from closed product box to
beautifully displayed open position, studio product photography, smooth reveal

/video-flow smartphone screen turning on from black to bright colorful app
interface, clean product shot, smooth power-on animation

/video-flow coffee cup filling from empty to full with steam rising, cafe
setting, smooth pouring motion visualization
```

**Manual Approach - Full Control**:

```bash
# Step 1: Generate start frame
/imagine-pro professional product photography of [product in state A], studio
lighting, [brand colors], centered composition, [specific camera angle], high
quality, 4K, photorealistic, clean background

# [Note the message ID: start-frame-abc]

# Step 2: Generate end frame (matching start)
/imagine-pro professional product photography of [same product in state B],
EXACT SAME camera angle as previous image, same studio lighting, [same brand
colors], same centered composition, matching previous shot perfectly, high
quality, 4K, photorealistic, same clean background

# [Note the message ID: end-frame-def]

# Step 3: Request video generation
"Generate a video using start frame [start-frame-abc] and end frame
[end-frame-def] showing [smooth transformation description]"
```

**Complete Example - Headphones Product Reveal**:

```bash
# Start Frame
/imagine-pro premium wireless headphones in black product box packaging, studio
product photography, soft professional lighting, black and silver headphones
visible in box, minimal white background, centered front view composition,
high-end product shot, photorealistic, 4K quality

# [start-abc123]

# End Frame
/imagine-pro same premium wireless headphones now displayed outside box,
studio product photography matching previous shot EXACTLY, same soft professional
lighting, same black and silver headphones, same minimal white background, SAME
centered front view angle as before, headphones elegantly positioned, high-end
product photography, photorealistic, 4K, matches previous composition precisely

# [end-def456]

# Generate Video
"Create a smooth product reveal video using frames start-abc123 and end-def456,
showing elegant transformation from boxed to showcased, professional product
reveal animation, 5 seconds"
```

### Environmental Transformation

**Goal**: Day-to-night, season change, weather shift

**Critical**: Camera position must be LOCKED (identical in both frames)

**Workflow**:

```bash
# These work great with /video-flow:
/video-flow modern city skyline transitioning from bright sunny day to glowing
night cityscape, same camera position locked, rooftop viewpoint, smooth time-lapse
style progression

/video-flow forest landscape changing from summer green to autumn orange and red,
same camera angle locked, natural photography, smooth seasonal transition

/video-flow beach scene transforming from clear sunny weather to dramatic storm
clouds, same viewpoint exactly, cinematic photography, smooth weather progression
```

**Manual Frame Creation**:

```bash
# Start: Daytime
/imagine-pro modern city skyline viewed from rooftop, bright daytime, blue sky,
sunlight on skyscrapers, professional photography, 4K, specific camera angle at
eye level, wide city view, photorealistic

# [day-xyz]

# End: Nighttime (MUST match camera position exactly)
/imagine-pro modern city skyline from EXACT SAME rooftop viewpoint as previous,
same buildings in same positions, nighttime scene, dark blue evening sky, building
windows glowing warmly, same professional photography, 4K, IDENTICAL camera angle
and framing, only time of day changed, photorealistic

# [night-xyz]

# Generate time-lapse video
"Create smooth day-to-night timelapse video using day-xyz and night-xyz frames,
gradual sky darkening, progressive window light activation, cinematic timelapse,
5 seconds"
```

### App Loading Animation

**Goal**: Engaging loading sequence for app

**Workflow**:

```bash
# Concept examples:

# Logo Reveal
/video-flow company logo assembling from scattered pieces to complete form,
clean white background, smooth assembly animation, modern brand animation

# Progress Indicator
/video-flow circular progress ring filling from empty 0% to complete 100%,
[brand colors], clean minimal design, smooth loading animation

# Themed Animation (meditation app example)
/video-flow lotus flower opening from closed bud to full bloom, peaceful zen
aesthetic, purple and white colors, soft gradient background, calm smooth
blooming animation, 4 seconds

# Abstract Motion
/video-flow abstract flowing shapes morphing smoothly, [brand colors] gradient,
modern minimal design, satisfying smooth motion, loading screen optimized
```

**Manual Approach - Lotus Bloom Example**:

```bash
# Closed state (loading start)
/imagine-pro closed lotus flower bud, minimal zen aesthetic, soft purple and
white colors, light blue to white gradient background, centered composition,
peaceful mood, high quality 3D render style, square format mobile app optimized

# [lotus-start]

# Open state (loading complete)
/imagine-pro fully bloomed open lotus flower, SAME composition and camera angle
as previous, purple white petals spread, same light blue to white gradient
background, same centered position, same peaceful zen aesthetic, same lighting
and 3D render style, square format, matches previous frame exactly

# [lotus-end]

# Generate animation
"Create peaceful blooming animation using lotus-start and lotus-end frames,
gentle smooth opening motion, meditation app aesthetic, calm zen movement,
4 seconds"
```

### Logo Animation Concept

**Goal**: Animated logo for video intros

**Workflow**:

```bash
# Simple to Complex
/video-flow logo starting as simple minimal form then expanding to full detailed
logo with tagline, [brand colors], clean background, smooth professional reveal,
modern brand animation

# Assembly Animation
/video-flow logo elements assembling from separate floating pieces into complete
logo, [brand colors], clean background, satisfying construction animation,
professional brand video intro

# Glow/Emphasis
/video-flow logo transitioning from flat basic version to highlighted glowing
emphasized version, [brand colors], adds energy and impact, clean background,
professional brand treatment
```

### UI/App Transition Animation

**Goal**: Screen state change animation concept

**Workflow**:

```bash
# Empty to Filled
/video-flow mobile app screen transforming from empty state placeholder to filled
with content, [app style], smooth content loading animation, professional UI
animation concept

# Feature Reveal
/video-flow app interface highlighting specific feature, from normal state to
feature emphasized with glow or zoom, [brand colors], smooth UI transition,
professional app animation

# Mode Switch
/video-flow app interface changing from light mode to dark mode, same layout
and content, smooth color theme transition, modern app design, professional
mode switching animation
```

## Best Practices

### Frame Compatibility Checklist

Before generating your video, ensure:

**Camera/Perspective**:
- [ ] Same camera angle (front, side, aerial, etc.)
- [ ] Same distance from subject
- [ ] Same framing and composition
- [ ] Same aspect ratio

**Lighting**:
- [ ] Compatible light direction
- [ ] Similar lighting intensity (or intentional shift)
- [ ] Matching shadows (if not time-based change)
- [ ] Consistent light color temperature

**Composition**:
- [ ] Background elements in same positions
- [ ] Subject similarly placed
- [ ] Matching overall layout
- [ ] Same color grading approach

**Style**:
- [ ] Same visual style (photo, illustration, 3D render)
- [ ] Matching level of detail
- [ ] Consistent mood/atmosphere
- [ ] Same resolution and quality

### Prompt Strategies for Compatibility

**In Start Frame Prompt**:
```
- Be specific about camera angle
- Mention "front view" or "side angle" or "aerial view"
- Define lighting setup clearly
- Establish composition explicitly
```

**In End Frame Prompt**:
```
- ALWAYS reference matching the previous frame
- Use "EXACT SAME camera angle as previous"
- "same lighting setup"
- "same composition"
- "matching previous shot"
- "IDENTICAL framing"
```

**Example Comparison**:

❌ **Poor (likely incompatible)**:
```
Start: /imagine-pro smartphone on desk
End: /imagine-pro smartphone with screen on
```
Too vague - camera angle, lighting, position all undefined and likely different

✅ **Good (high compatibility)**:
```
Start: /imagine-pro smartphone on wooden desk, front view straight on, centered,
soft diffused lighting from above, clean minimal white background, product
photography style, photorealistic

End: /imagine-pro same smartphone on same wooden desk, EXACT SAME front view
angle, same centered position, same soft diffused lighting from above, screen
now glowing with interface visible, same clean white background, same product
photography style matching previous, photorealistic
```

### Transformation Types That Work Well

**Product Transformations**:
- Packaged → Unpackaged
- Off → On (screens, lights)
- Closed → Open
- Plain → Enhanced/Featured
- Small → Large (zoom)
- Individual → Multiple/Arranged

**Environmental Changes**:
- Day → Night (most popular)
- Season shifts (summer → autumn)
- Weather changes (clear → storm)
- Time progression (sunrise → sunset)
- Empty → Crowded spaces

**Abstract/Motion**:
- Simple shapes → Complex forms
- Scattered → Assembled
- Minimal → Detailed
- One color → Multiple/Gradient
- Static → Dynamic composition

**UI/Digital**:
- Loading → Loaded
- Empty → Filled with content
- Normal → Highlighted/Active
- Light mode → Dark mode
- Low → High detail/quality

## Use Cases by Industry

### E-commerce

```bash
# Product Reveal
/video-flow product emerging from shipping box, smooth unboxing reveal, studio
photography, professional e-commerce video

# 360-Degree Rotation Concept
/video-flow product rotating from front view to side view, smooth rotation,
e-commerce product display, clean background, professional photography

# Before/After (clothing, beauty)
/video-flow transformation showing before and after using product, lifestyle
photography, smooth transition, professional e-commerce demo
```

### SaaS/Tech

```bash
# Feature Demo Concept
/video-flow software interface showing feature activation, from inactive to
active highlighted state, modern UI design, smooth professional demo

# Data Visualization
/video-flow dashboard chart animating from empty to filled with data, smooth
data loading visualization, modern SaaS aesthetic, professional interface

# Integration Concept
/video-flow showing connection between apps, from separate to connected with
visual link, modern tech illustration, smooth integration visualization
```

### Real Estate/Architecture

```bash
# Property Tour Transition
/video-flow modern interior room transitioning from day to evening lighting,
same camera position, architectural photography, smooth time progression

# Before/After Renovation
/video-flow room transformation from old dated style to modern renovated,
same camera angle, smooth renovation reveal, professional real estate video

# Seasonal Property Views
/video-flow property exterior changing from winter to summer, same viewpoint,
smooth seasonal transition, professional real estate photography
```

### Food & Beverage

```bash
# Preparation Sequence
/video-flow plate going from empty to beautifully plated dish, overhead food
photography, smooth plating sequence, professional culinary video

# Pouring/Filling
/video-flow glass filling from empty to full with beverage, smooth pouring
motion concept, professional food photography, appealing presentation

# Cooking Transformation
/video-flow ingredient transforming from raw to cooked, same angle, smooth
cooking progression, professional culinary video
```

### Entertainment/Media

```bash
# Scene Transitions
/video-flow movie scene transitioning between locations or times, cinematic
style, smooth professional transition, film quality

# Mood Changes
/video-flow scene changing from happy bright to dramatic dark mood, same
composition, cinematic lighting shift, professional film aesthetic

# Title Reveal
/video-flow movie or show title emerging from simple to full elaborate version,
cinematic style, smooth professional reveal, entertainment branding
```

## Advanced Techniques

### Multi-Segment Videos

Create longer sequences by combining multiple video clips:

```
Segment 1: A → B (product in box → product emerging)
Segment 2: B → C (product emerging → product fully displayed)
Segment 3: C → D (product displayed → product in use)

Generate each 3-5 second segment separately
Combine in video editor for longer narrative
```

### Looping Animations

Design for seamless loops:

```
Create end frame that can smoothly transition back to start
Useful for: loading animations, background videos, ambient content

Example:
Start: Circle at 0% progress
End: Circle at 100% progress that visually matches 0%
Result: Infinitely looping progress indicator
```

### Reverse Animations

Generate the reverse for different use cases:

```
Original: App opening (simple → detailed)
Reverse: App closing (detailed → simple)

Original: Product reveal (boxed → displayed)
Reverse: Product packup (displayed → boxed)
```

### Style Variations

Generate same transformation in different styles:

```
Version A: Photorealistic product photography
Version B: Illustrated/stylized version
Version C: 3D rendered version

Test which style resonates with audience
```

## Troubleshooting

### Video Doesn't Look Smooth

**Problem**: Choppy or jarring transition

**Solutions**:
- ✅ Regenerate end frame with MORE specific matching instructions
- ✅ Emphasize "EXACT SAME camera angle" more strongly
- ✅ Ensure backgrounds truly match
- ✅ Check lighting compatibility
- ✅ Simplify transformation (less changes at once)

### Frames Don't Match Well

**Problem**: End frame looks different from start

**Solutions**:
- ✅ When generating end frame, reference the start frame message ID
- ✅ Use phrases like "matching previous image exactly"
- ✅ Copy most of start frame prompt into end frame prompt
- ✅ Only change the specific transformation elements

### Motion Doesn't Make Sense

**Problem**: Unclear how A becomes B

**Solutions**:
- ✅ Choose more logical transformation
- ✅ Ensure visible change path
- ✅ Simplify the transformation
- ✅ Add intermediate frame (A → B → C)

### Video is Too Short/Long

**Problem**: Duration doesn't match needs

**Solutions**:
- ⚠️ ImaginePro generates fixed duration (typically 4-6 seconds)
- ✅ Plan for post-production speed adjustment if needed
- ✅ Design transformation complexity for target duration
- ✅ Can loop shorter animations

## Workflow Optimization

### Planning Multiple Videos

```
1. Create style guide for video series:
   - Consistent visual style
   - Matching quality level
   - Similar durations
   - Coordinated themes

2. Generate all start frames in batch:
   - Establishes visual consistency
   - Easier to maintain style
   - More efficient workflow

3. Generate matching end frames:
   - Reference start frames specifically
   - Maintain established style

4. Generate videos in sequence:
   - Review and refine as you go
   - Apply learnings to next videos
```

### Iteration Strategy

```
Round 1: Generate initial frames and video
Round 2: Review - is transition smooth enough?
Round 3: If needed, regenerate end frame with better matching
Round 4: Generate updated video
Round 5: Upscale final frames if video is approved
Round 6: Potentially regenerate video with upscaled frames for maximum quality
```

## Next Steps

- See [Web Development Workflow](web-development.md) for static web assets
- See [Marketing Workflow](marketing-content.md) for campaign videos
- Check [Video Prompt Library](../prompt-library/video-concepts.md) for more examples
- Review [Examples](../../examples/) for complete video projects

---

**Pro Tip**: The `/video-flow` command is perfect for straightforward transformations. For complex, multi-step videos or when you need maximum control over frame compatibility, work directly with the Video Workflow Director agent who will guide you through optimal frame creation!

# UI/UX Design Workflow

Complete guide to creating UI/UX assets with the ImaginePro plugin.

## Overview

UI/UX design requires consistent, accessible, and professional visual assets: icons, illustrations, empty states, onboarding screens, and more. This guide shows you how to create cohesive design system assets efficiently.

## Quick Reference

| Asset Type | Recommended Size | Best Approach |
|------------|------------------|---------------|
| Navigation Icons | 64px (design), export multiple | UI/UX Asset Generator agent |
| Feature Icons | 48-64px | /imagine-pro with style consistency |
| Empty States | 300x300 to 400x400 | UI/UX agent or /imagine-pro |
| Onboarding | Device-specific (9:16 mobile) | UI/UX agent for series |
| App Illustrations | Variable, context-dependent | /imagine-pro with clear style |
| UI Backgrounds | Subtle, non-distracting | /imagine-pro with "subtle" keywords |

## Complete Workflows

### Icon Set Creation

**Goal**: Create a consistent set of navigation icons

**Workflow**:

```
Step 1: Activate UI/UX Asset Generator
"I need [number] navigation icons for my [app type]"

Step 2: Agent asks clarifying questions:
- App purpose and style
- Icon names/functions
- Style preference (minimal line, filled, rounded)
- Color approach (monochrome or brand colors)

Step 3: Define style once:
- Icon style (minimal line, filled, outlined)
- Line weight (e.g., 3px at 64px scale)
- Color palette
- Level of detail

Step 4: Generate sequentially for consistency:
Agent creates each icon one by one, maintaining:
- Same line weight
- Same visual complexity
- Same style descriptors
- Distinctive silhouettes

Step 5: Quality check:
- Review set together
- Ensure visual consistency
- Check distinctive shapes
- Verify optical balance

Step 6: Production ready:
/upscale-it [msg-id] for each icon
Export at multiple resolutions (1x, 2x, 3x)
```

**Alternative - Direct Command**:
```bash
# Define style first, then use for all icons
/imagine-pro minimal line icon for [function], [shape description],
clean geometric lines, [X]px stroke weight, monochrome [color],
centered composition, 64x64 resolution, icon design, sharp and clear

# Repeat with same style keywords for consistency
```

**Example 5-Icon Set**:
```bash
# Icon 1: Home
/imagine-pro minimal line icon for home navigation, simple house symbol
with pitched roof, clean geometric lines, 3px stroke weight, monochrome
black, centered composition on white background, 64x64 resolution, icon
design, sharp and clear

# Icon 2: Search
/imagine-pro minimal line icon for search, magnifying glass symbol, clean
geometric lines matching previous icon style, 3px stroke weight, monochrome
black, centered composition on white background, 64x64 resolution, icon
design, same visual weight as home icon

# Icon 3: Profile
/imagine-pro minimal line icon for user profile, simple person silhouette,
clean geometric lines matching set, 3px stroke weight, monochrome black,
centered composition on white background, 64x64 resolution, icon design,
consistent with previous icons

# Icon 4: Settings
/imagine-pro minimal line icon for settings, gear or cog symbol, clean
geometric lines matching icon set, 3px stroke weight, monochrome black,
centered composition on white background, 64x64 resolution, icon design,
same style consistency

# Icon 5: Notifications
/imagine-pro minimal line icon for notifications, bell symbol, clean
geometric lines matching complete set, 3px stroke weight, monochrome black,
centered composition on white background, 64x64 resolution, icon design,
maintains visual consistency
```

### Empty State Illustrations

**Goal**: Friendly illustrations for "no content" states

**Workflow**:

```
Step 1: Identify empty states needed:
- Empty inbox/messages
- No search results
- No notifications
- Empty favorites/bookmarks
- 404 page not found
- No data/analytics

Step 2: For each state, activate UI/UX agent or use command:
"Create an empty state illustration for [specific context]"

Step 3: Agent/you define:
- App's design style (minimal, playful, professional)
- Illustration style (flat, isometric, hand-drawn)
- Brand colors
- Emotional tone (reassuring, friendly, helpful)
- Size constraints

Step 4: Generate with appropriate mood:
- Non-threatening
- Friendly and helpful
- Clear metaphor
- Brand-aligned

Step 5: Ensure consistency across all empty states:
Same illustration style throughout app
```

**Example Empty State Prompts**:

```bash
# Empty Inbox
/imagine-pro empty state illustration for mobile app inbox, peaceful mailbox
with check mark indicating zero messages, minimal flat design style, friendly
calming mood, blue and purple gradient colors, simple geometric shapes,
centered composition, 400x400 pixels, modern UI illustration, clean professional,
positive "inbox zero" concept

# No Search Results
/imagine-pro empty state illustration for no search results, magnifying glass
finding nothing concept, minimal flat design matching previous style, helpful
friendly mood, same blue purple colors, simple shapes, centered 400x400,
suggests trying different search terms, modern UI illustration, reassuring tone

# Empty Notifications
/imagine-pro empty state illustration for no notifications, peaceful bell icon
with zen feeling, minimal flat design matching app style, calming positive mood,
blue purple brand colors, simple geometric minimal, centered 400x400, conveys
it's good to have no notifications, modern UI illustration, peaceful aesthetic

# 404 Page Not Found
/imagine-pro empty state illustration for 404 error page, lost person with map
or confused explorer concept, minimal flat design friendly style, lighthearted
not frustrating mood, blue purple colors, 400x400 centered, helps user not feel
bad about error, modern UI illustration, helpful guiding tone
```

### Onboarding Illustration Series

**Goal**: Create 3-step onboarding flow

**Workflow**:

```
Step 1: Define your 3 onboarding steps:
Example for Task Management App:
- Step 1: Create tasks easily
- Step 2: Organize and prioritize
- Step 3: Track progress and achieve goals

Step 2: Activate UI/UX Asset Generator:
"I need 3 onboarding illustrations showing [your app's key features]"

Step 3: Agent creates consistent series:
- Same illustration style
- Same character design (if applicable)
- Same color palette
- Same device orientation
- Progressive story arc

Step 4: Review series together:
- Does it tell a clear story?
- Visual consistency maintained?
- Right emotional progression?

Step 5: Upscale finals:
/upscale-it for each step
```

**Example Onboarding Series**:

```bash
# Step 1: Getting Started
/imagine-pro mobile onboarding illustration step 1, person easily creating
first task on phone, modern flat illustration style, simple friendly character
adding item to clean list interface, blue primary color with white background,
minimalist geometric shapes, portrait orientation 9:16, approachable welcoming
mood, UI illustration, clear simple composition, beginning of journey

# Step 2: Organization
/imagine-pro mobile onboarding illustration step 2, same person organizing
tasks with colorful category tags, modern flat illustration matching previous
exact style, same character design, task cards with vibrant tag labels floating
organized, blue primary with accent colors, portrait 9:16, satisfying organized
feeling, matches step 1 illustration style, middle progress

# Step 3: Achievement
/imagine-pro mobile onboarding illustration step 3, same person celebrating
completed tasks with progress chart, modern flat illustration matching complete
set, exact same character style, completion checkmarks and upward trending graph,
blue color scheme with success green, portrait 9:16, achievement pride mood,
maintains series consistency, finale celebration moment
```

### Feature Icon Set

**Goal**: Icons for marketing page or app features

**Workflow**:

```bash
# Feature icons can be more detailed than navigation icons
# Common features to illustrate:

# Speed/Performance
/imagine-pro feature icon for speed and performance, lightning bolt or rocket
symbol, modern style with slight detail, blue brand color with white background,
48px size, clean professional, icon design with small highlights

# Security
/imagine-pro feature icon for security and protection, shield with checkmark or
lock symbol, modern style matching speed icon, blue brand color with white
background, 48px, same detail level, professional icon design

# Analytics/Insights
/imagine-pro feature icon for analytics and data insights, chart or graph symbol
trending upward, modern style matching set, blue brand color, white background,
48px, consistent detail level, professional icon matching previous

# Collaboration
/imagine-pro feature icon for team collaboration, connected people or chat
bubbles, modern style matching complete set, blue brand color, white background,
48px, same visual weight, completes professional icon set

# Integration
/imagine-pro feature icon for integrations and connections, puzzle pieces or
connected nodes, modern style consistent with full set, blue brand color, white
background, 48px, maintains style, final icon in professional set
```

## Design System Approach

### Building Cohesive Asset Libraries

**Strategy**:

1. **Define Style Guide First**
   ```
   Icon Style: Minimal line, 3px stroke at 64px
   Illustration Style: Flat geometric, friendly
   Color Palette: Primary blue (#2563EB), Accent purple (#7C3AED)
   Mood: Professional but approachable
   Level of Detail: Minimal, focus on clarity
   ```

2. **Create Master Examples**
   - Generate 2-3 "reference" assets first
   - Use these to establish style
   - Reference them when generating additional assets

3. **Maintain Consistency**
   ```bash
   # Always reference previous work:
   /imagine-pro [new asset description], matching style of previous [asset type],
   same [specific style attributes], consistent with existing set
   ```

4. **Batch Generation**
   - Generate complete sets in one session
   - Agent maintains context and consistency
   - Review entire set together before upscaling

### Accessibility Considerations

**Contrast Ratios**:
- Text: Minimum 4.5:1 (WCAG AA)
- UI Elements: Minimum 3:1
- Test your assets with contrast checker tools

**Color Blindness**:
- Don't rely solely on color for meaning
- Use shapes, patterns, or labels too
- Test with color blindness simulators

**Meaningful Imagery**:
- Every illustration should communicate purpose
- Avoid decorative-only assets
- Consider alternative text descriptions

**Inclusive Representations**:
- Diverse character representations
- Culturally neutral symbols when possible
- Avoid stereotypes and bias

## Platform-Specific Optimization

### Mobile Apps (iOS/Android)

**Icon Sizes to Export**:
- 1x: 24px, 32px, 48px
- 2x: 48px, 64px, 96px
- 3x: 72px, 96px, 144px

**Onboarding Dimensions**:
- iOS: 9:16 portrait (1170x2532 for iPhone 13 Pro)
- Android: 9:16 portrait (1080x1920 common)

**Design Considerations**:
- Thumb-friendly tap targets
- Bottom-heavy navigation icon placement
- Clear against both light/dark mode

### Web Applications

**Icon Sizes**:
- Standard: 24px, 32px
- Retina: 48px, 64px
- Favor SVG format when possible

**Illustration Sizes**:
- Empty states: 300-400px
- Feature sections: 400-600px
- Headers: Variable based on layout

**Responsive Considerations**:
- Works at multiple breakpoints
- Scales gracefully
- Mobile-first design

### Design Tools Integration

**Export Recommendations**:
- **Icons**: SVG (scalable) or PNG with multiple resolutions
- **Illustrations**: PNG with transparency
- **Backgrounds**: JPEG or WebP for photos, PNG for graphics

**Naming Conventions**:
```
icon-[name]-[size]@[scale]x.png
Example: icon-home-24@2x.png

illustration-[context]-[size].png
Example: illustration-empty-inbox-400.png
```

## Common Workflows

### Complete App Icon Set (10 Icons)

```
1. List all needed icons
2. Define unified style (minimal line, filled, etc.)
3. Activate UI/UX Asset Generator
4. Generate all 10 sequentially in one session
5. Review complete set for consistency
6. Adjust any outliers with /vary-it
7. Upscale approved set
8. Export multiple resolutions
9. Implement in design system
```

### Empty State Suite (5 States)

```
1. Identify all empty states in app
2. Define illustration style and mood
3. Generate each with consistent style
4. Ensure friendly, helpful tone
5. Maintain brand alignment
6. Review complete suite
7. Upscale finals
8. Add to design system with guidelines
```

### Onboarding Flow (3-4 Screens)

```
1. Map user journey and key messages
2. Work with UI/UX agent for series
3. Define character style (if using characters)
4. Generate progressive sequence
5. Ensure story flow is clear
6. Review narrative arc
7. Upscale complete series
8. Implement with appropriate copy
```

## Best Practices

### Icon Design

**Do**:
- ✅ Design at 64px for clarity, export smaller
- ✅ Maintain consistent line weight across set
- ✅ Use distinctive, recognizable shapes
- ✅ Ensure optical balance (not just geometric)
- ✅ Test at target size (24px, 32px)
- ✅ Keep simple - remove unnecessary detail

**Don't**:
- ❌ Mix styles (outlined + filled in same set)
- ❌ Overcomplicate - too much detail at small size
- ❌ Use inconsistent visual weight
- ❌ Create ambiguous symbols
- ❌ Ignore cultural symbol meanings

### Illustration Design

**Do**:
- ✅ Establish style guide before generating set
- ✅ Use consistent color palette
- ✅ Match level of detail across illustrations
- ✅ Communicate clear purpose/meaning
- ✅ Test in actual UI context
- ✅ Consider animation potential

**Don't**:
- ❌ Mix illustration styles in same app
- ❌ Create decorative-only assets
- ❌ Ignore brand personality
- ❌ Overcomplicate empty states
- ❌ Use culturally insensitive imagery

### Workflow Optimization

**Batch Work**:
- Generate complete sets in single sessions
- Maintain agent context for consistency
- Review sets holistically
- Upscale approved assets together

**Iteration Strategy**:
```
Round 1: Generate 2-3 reference assets, establish style
Round 2: Generate remaining set using references
Round 3: Review complete set, refine outliers with /vary-it
Round 4: Upscale approved finals
Round 5: Implement and test in actual UI
```

**Testing Protocol**:
- View at target size
- Test on actual devices/screens
- Check accessibility (contrast, meaning)
- Verify cultural appropriateness
- Get feedback from users/team

## Advanced Techniques

### Creating Multiple States

```bash
# Default state
/imagine-pro settings icon, gear symbol, minimal line style, 3px stroke,
monochrome gray, 64px, icon design

# Active state
/imagine-pro settings icon active state, same gear symbol and style,
highlighted in blue color, same 3px stroke, 64px, matches previous icon,
represents active/selected state

# Disabled state
/imagine-pro settings icon disabled state, same gear symbol and style,
very light gray translucent, same 3px stroke, 64px, matches icon set,
indicates disabled non-interactive state
```

### Animation Frame Concepts

```bash
# Loading animation frames (create 3-4 frames)
/imagine-pro loading spinner frame 1, circular dots, minimal design,
blue brand color, 64px, clean simple, first frame of animation

/imagine-pro loading spinner frame 2, circular dots rotated 45 degrees,
same style and colors, 64px, matches frame 1, animation progression

# Then use video generation to create smooth animation
```

### Style Variations for Testing

```bash
# Create 3 style variants of same icon set, test with users
Variant A: Minimal line icons
Variant B: Filled solid icons
Variant C: Rounded outlined icons

Test which resonates best with your audience
```

## Next Steps

- See [Web Development Workflow](web-development.md) for website assets
- See [Marketing Workflow](marketing-content.md) for promotional content
- Check [UI/UX Prompt Library](../prompt-library/ui-ux-assets.md) for more examples
- Review [Examples](../../examples/) for complete design systems

---

**Pro Tip**: Always generate icon sets sequentially in a single session with the UI/UX Asset Generator agent. This ensures maximum consistency as the agent maintains context of previous icons in the set!

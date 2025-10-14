# Contributing to ImaginePro Claude Code Plugin

Thank you for your interest in contributing to the ImaginePro Claude Code Plugin! This plugin helps developers create professional visual assets directly within Claude Code.

## How You Can Contribute

There are several ways to contribute to this project:

### 1. Prompt Library Contributions

**What We're Looking For:**
- Tested, proven prompts that produce high-quality results
- Prompts for common use cases not yet covered
- Industry-specific prompt templates
- A/B tested variants with performance notes

**How to Contribute Prompts:**

1. **Test Your Prompt**: Generate the asset multiple times to ensure consistency
2. **Document Results**: Note what works well and any tips for customization
3. **Follow Format**: Use existing prompt library format (see `docs/prompt-library/`)
4. **Submit**: Open a Pull Request with your addition

**Prompt Submission Template:**
```markdown
### [Asset Type Name]
```
[Your detailed prompt here, following the format:
- Clear description of what it generates
- Specific dimensions
- Style keywords
- Brand color placeholders
- Quality descriptors
]
```

**Tips for Success:**
- Include [bracketed placeholders] for customization
- Specify exact dimensions
- Note platform (Instagram, email, web, etc.)
- Include mood/style descriptors
```

### 2. Workflow Guide Improvements

**What Helps:**
- Additional workflow examples for specific industries
- Alternative approaches to existing workflows
- Tips and tricks learned from experience
- Common mistakes and how to avoid them

**How to Contribute:**
- Add sections to existing workflow guides in `docs/workflows/`
- Propose new workflow guides for uncovered use cases
- Share optimization strategies

### 3. Real-World Examples

**We Love:**
- Complete project walkthroughs showing start-to-finish asset creation
- Before/after case studies
- Multi-asset campaigns with results
- Industry-specific examples (e-commerce, healthcare, finance, etc.)

**Example Structure:**
```markdown
# Example: [Project Name]

## Project Overview
- Company/product description
- Goals and requirements
- Brand guidelines
- Timeline

## Complete Workflow
- Asset-by-asset walkthrough
- Actual prompts used
- Results and message IDs
- Refinements made

## Results & Learnings
- Time investment
- Quality achieved
- What worked well
- What you'd do differently
```

### 4. Agent Improvements

**Agent files** (`agents/*.md`) define specialized personas. You can contribute:
- Additional example interactions
- Expanded best practices
- New use case scenarios
- Improved prompting guidance

**Note**: Agent improvements should maintain the consultative, educational tone.

### 5. Command Enhancements

**Commands** (`commands/*.md`) define slash command behavior. Contributions:
- Additional usage examples
- More tips for better results
- Edge case handling guidance
- Related command workflows

### 6. Documentation

**Always Welcome:**
- Typo fixes and clarity improvements
- Additional troubleshooting scenarios
- FAQ additions
- Translation to other languages (future)

## Contribution Guidelines

### Before You Start

1. **Check Existing Issues**: See if your contribution is already planned
2. **Open a Discussion**: For major contributions, discuss first in GitHub Discussions
3. **Follow the Style**: Match the tone and format of existing documentation

### Tone and Style

This plugin is **educational and professional**. When writing:

**Do:**
- ✅ Be clear and concise
- ✅ Use practical, copy-paste ready examples
- ✅ Explain the "why" behind recommendations
- ✅ Share learnings and best practices
- ✅ Use active voice
- ✅ Be encouraging and supportive

**Don't:**
- ❌ Use jargon without explanation
- ❌ Make assumptions about user skill level
- ❌ Be overly casual or use excessive emojis
- ❌ Include generic advice without specifics
- ❌ Promise unrealistic results

### File Organization

```
imaginepro-claude-plugin/
├── agents/                  # Agent persona specifications
├── commands/                # Slash command definitions
├── docs/
│   ├── workflows/           # Complete workflow guides
│   ├── prompt-library/      # Curated prompts
│   └── troubleshooting.md   # Common issues
└── examples/                # Real-world project walkthroughs
```

### Markdown Standards

- Use ATX-style headers (`#` not underlines)
- Include code blocks with language specification
- Use relative links for internal documentation
- Format prompts in code blocks with triple backticks
- Use lists for scannable content

### Prompt Formatting

**Standard Format:**
```
[description of asset], [key visual elements], [style keywords], [brand colors
placeholders], [dimensions], [mood/tone], [quality keywords], [use case context]
```

**Example:**
```
modern SaaS hero image, professional team collaborating in office, blue and
purple color scheme, space for headline in upper third, 1920x1080, innovative
productive atmosphere, photorealistic photography, high quality 4k
```

## Pull Request Process

1. **Fork the Repository**
2. **Create a Feature Branch**: `git checkout -b feature/your-contribution-name`
3. **Make Your Changes**
   - Follow existing file structure
   - Match documentation style
   - Test prompts if contributing to prompt library
4. **Commit with Clear Message**: `git commit -m "Add [what you added]"`
5. **Push to Your Fork**: `git push origin feature/your-contribution-name`
6. **Open Pull Request**
   - Use a clear, descriptive title
   - Explain what you're adding and why
   - Reference any related issues
   - Include examples of generated assets if applicable (can link to images)

### PR Title Format

- `docs: [description]` - Documentation improvements
- `prompts: [description]` - Prompt library additions
- `workflows: [description]` - Workflow guide enhancements
- `examples: [description]` - New example walkthroughs
- `agents: [description]` - Agent persona improvements
- `fix: [description]` - Bug fixes or corrections

## What We Won't Accept

To maintain quality and focus:

- ❌ Prompts that haven't been tested
- ❌ Generic stock prompt lists from other sources
- ❌ Promotional content or self-promotion
- ❌ Duplicate content already covered
- ❌ Off-topic contributions outside the plugin scope
- ❌ Breaking changes to core agent personas without discussion

## Testing Your Contributions

### For Prompt Contributions

Before submitting prompts to the library:

1. **Generate 3-5 times**: Ensure consistency
2. **Test variations**: Try with different bracketed replacements
3. **Check quality**: Results should be professional and production-ready
4. **Note edge cases**: Document any limitations or special considerations

### For Documentation

1. **Read aloud**: Does it flow naturally?
2. **Check links**: All internal links work?
3. **Verify code blocks**: Are examples accurate?
4. **Proofread**: Spelling and grammar check

## Community Guidelines

### Be Respectful

- Respect all contributors regardless of experience level
- Provide constructive feedback
- Assume good intent
- Help others learn

### Share Generously

- Contribute your best prompts and workflows
- Document your learnings
- Answer questions in Discussions
- Help troubleshoot issues

### Give Credit

- If you're building on someone else's work, credit them
- Reference sources for techniques or approaches
- Acknowledge collaborators

## Recognition

Contributors who make significant contributions will be:
- Listed in project README
- Credited in documentation they contribute
- Recognized in release notes

## Questions?

- **Technical Questions**: [GitHub Discussions](https://github.com/imaginpro/imaginepro-claude-plugin/discussions)
- **Bug Reports**: [GitHub Issues](https://github.com/imaginpro/imaginepro-claude-plugin/issues)
- **Feature Requests**: [GitHub Discussions - Ideas](https://github.com/imaginpro/imaginepro-claude-plugin/discussions/categories/ideas)

## License

By contributing to this project, you agree that your contributions will be licensed under the project's MIT License.

---

**Thank you for helping make the ImaginePro Claude Code Plugin better for everyone!** 🎨

Every contribution, whether it's a single prompt, a typo fix, or a complete workflow guide, helps developers create better visual assets more efficiently.

# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the **ImaginePro Claude Code Plugin** - a pure documentation/specification plugin that wraps the ImaginePro MCP server with specialized agents, slash commands, and workflows for professional AI image and video generation within Claude Code.

**Critical Architecture Understanding:**
- This plugin contains **NO implementation code** - it's pure markdown/JSON
- The actual functionality comes from `imaginepro-mcp-server` (npm package)
- The plugin provides UX layer: agents, commands, documentation, workflows
- The MCP server provides infrastructure: 8 MCP tools for image/video generation

## Repository Structure

```
imaginepro-claude-plugin/
├── .claude-plugin/
│   └── plugin.json              # Plugin manifest - defines metadata, features, requirements
├── .mcp.json                    # MCP server config - references imaginepro-mcp-server via npx
├── agents/                      # 4 specialized agent specifications (markdown)
│   ├── web-asset-producer.md    # Web development assets
│   ├── ui-asset-generator.md    # UI/UX design assets
│   ├── marketing-creative.md    # Marketing materials
│   └── directory.md   # Video workflows
├── commands/                    # 5 slash command specifications (markdown)
│   ├── imagine-pro.md          # Intelligent generation with guidance
│   ├── upscale-it.md           # Production quality enhancement
│   ├── vary-it.md              # Smart variations
│   ├── video-flow.md           # Video workflow automation
│   └── imagine-guide.md        # Interactive learning
├── docs/                       # User documentation
│   ├── quick-start.md
│   ├── troubleshooting.md
│   ├── workflows/              # Complete workflow guides
│   └── prompt-library/         # Curated prompt examples
└── examples/                   # Real-world project walkthroughs
```

## Plugin Architecture

### How It Works

```
User installs plugin
   ↓
.mcp.json tells Claude Code to load MCP server
   ↓
npx downloads imaginepro-mcp-server from npm (v1.1.0+)
   ↓
User gets: MCP tools + Agents + Commands + Docs
```

### Three-Layer Design

1. **Infrastructure Layer** (imaginepro-mcp-server npm package)
   - 8 MCP tools: generate-image, upscale-image, create-variant, generate-video, etc.
   - Handles API communication with ImaginePro
   - Client-agnostic (works with any MCP client)

2. **UX Layer** (this plugin)
   - 4 specialized agents for domain expertise
   - 5 smart commands for workflow automation
   - Educational content and prompt engineering guidance

3. **Documentation Layer**
   - Quick starts, workflows, troubleshooting
   - Prompt libraries with proven examples
   - Real-world project walkthroughs

## Key Configuration Files

### `.claude-plugin/plugin.json`
- Defines plugin metadata (name, version, author)
- Declares features (agents, commands, mcpServers)
- Specifies requirements (IMAGINEPRO_API_KEY env var)
- Maps documentation structure
- **Edit this when:** Adding/removing agents or commands, updating version, changing requirements

### `.mcp.json`
- Configures the ImaginePro MCP server connection
- Uses `npx -y imaginepro-mcp-server` for automatic npm package installation
- Passes `IMAGINEPRO_API_KEY` environment variable
- **Edit this when:** Changing MCP server version or configuration

## Agent Specifications

Each agent in `agents/` follows this structure:
- **Expertise section**: Technical knowledge and design principles
- **Workflow section**: Discovery → Planning → Generation → Refinement
- **Best practices**: Asset-type-specific guidance with dimensions, composition tips
- **Example interactions**: Realistic conversation flows
- **Tool usage**: Which MCP tools to use and when
- **Success metrics**: Goals for helping developers

**When modifying agents:**
- Maintain conversational, consultative tone
- Include specific dimensions, formats, and technical specs
- Provide educational content (teach prompt engineering)
- Reference MCP tools by exact names from imaginepro-mcp-server

## Command Specifications

Each command in `commands/` is a markdown file that defines:
- Purpose and benefits
- Usage syntax and examples
- Tips for better results
- Post-generation workflows
- Related commands

**When modifying commands:**
- Keep examples practical and copy-paste ready
- Explain what makes the command different from direct MCP tool usage
- Show progressive workflows (generate → vary → upscale)
- Reference message IDs for follow-up actions

## Development Workflow

### Testing the Plugin Locally

Since this is a documentation-only plugin:

```bash
# Navigate to plugin directory
cd /Users/zenglei/Workspace/imaginepro-claude-plugin

# Validate plugin structure (if validator exists)
# claude plugin validate .

# Test installation via local path
# In Claude Code: /plugin marketplace add ./
# Then: /plugin install imaginepro
```

### Validating Changes

Before committing changes:

1. **Check plugin.json syntax**: Ensure valid JSON
2. **Verify .mcp.json references**: Correct npm package name/version
3. **Test markdown rendering**: Preview agent and command files
4. **Validate links**: All internal documentation links work
5. **Check examples**: Code examples are accurate and tested

### Content Guidelines

**For agents:**
- Specific technical details (dimensions, formats, standards)
- Real-world workflow examples
- Educational tone that teaches best practices
- Clear tool usage patterns

**For commands:**
- Practical, actionable examples
- Progressive disclosure of advanced features
- Clear differentiation from raw MCP tool usage
- Workflow integration guidance

**For documentation:**
- Beginner-friendly quick starts
- Advanced workflow guides for experienced users
- Troubleshooting organized by symptom
- Prompt libraries with proven, copy-paste ready examples

## Important Constraints

### What This Plugin Does NOT Do

- ❌ Implement MCP tools (that's imaginepro-mcp-server's job)
- ❌ Handle API communication
- ❌ Process images or videos
- ❌ Store state or maintain history
- ❌ Require compilation or build steps

### What This Plugin DOES Do

- ✅ Provide specialized agent personas
- ✅ Define workflow automation commands
- ✅ Teach prompt engineering best practices
- ✅ Guide users through domain-specific use cases
- ✅ Configure MCP server integration

## Environment Requirements

**Required:**
- `IMAGINEPRO_API_KEY`: User's API key from imaginepro.ai
- Claude Code >= 2.0.0
- Node.js >= 18.0.0 (for npx to run MCP server)

**MCP Server Dependency:**
- npm package: `imaginepro-mcp-server` ^1.1.0
- Installed automatically via npx when plugin loads

## Common Modifications

### Adding a New Agent

1. Create `agents/new-agent-name.md`
2. Follow existing agent structure (see `agents/web-asset-producer.md`)
3. Update `.claude-plugin/plugin.json` features.agents array
4. Add usage examples to README.md
5. Consider creating a workflow guide in `docs/workflows/`

### Adding a New Command

1. Create `commands/new-command.md`
2. Follow existing command structure (see `commands/imagine-pro.md`)
3. Update `.claude-plugin/plugin.json` features.commands array
4. Add to README.md command list
5. Update quick-start.md if it's a primary workflow command

### Updating Documentation

- `docs/quick-start.md`: First-time user experience
- `docs/troubleshooting.md`: Common error scenarios
- `docs/workflows/`: Complete end-to-end workflows for specific use cases
- `docs/prompt-library/`: Curated, tested prompt examples by category

### Version Management

When bumping version in `.claude-plugin/plugin.json`:
- Follow semantic versioning (major.minor.patch)
- Update IMPLEMENTATION_PLAN.md status if completing milestones
- Consider updating MCP server dependency version if new features available

## Architecture Decisions

### Why Separate Plugin from MCP Server?

**Benefits:**
1. **Separation of concerns**: Infrastructure vs. UX
2. **Independent updates**: Can improve UX without touching server
3. **Lightweight distribution**: Plugin is just markdown/JSON
4. **Reusable infrastructure**: Same MCP server works with other clients
5. **Clear maintenance boundaries**: Different teams can own each layer

### Why Markdown-Based Agents?

- Easily editable without coding
- Version controllable
- Readable documentation doubles as implementation
- Low barrier to community contributions
- Natural language specifications work well with LLMs

## MCP Tool Reference

The underlying `imaginepro-mcp-server` provides these 8 tools:

1. **generate-image**: Text-to-image generation
2. **gemini-imagine**: Multi-modal generation with Gemini
3. **generate-video**: Text-to-video generation
4. **upscale-image**: Enhance image quality/resolution
5. **create-variant**: Generate variations of existing image
6. **reroll-image**: Regenerate with same prompt
7. **inpaint-image**: Edit specific regions
8. **check-status**: Track generation status

Agents and commands reference these tools directly when generating content.

## Contribution Areas

Based on IMPLEMENTATION_PLAN.md, main areas needing expansion:

1. **Additional workflow guides** (docs/workflows/)
   - ui-ux-design.md
   - marketing-content.md
   - video-creation.md

2. **Additional prompt libraries** (docs/prompt-library/)
   - ui-ux-assets.md
   - marketing-assets.md
   - video-concepts.md

3. **Real-world examples** (examples/)
   - Complete project walkthroughs
   - Before/after case studies
   - Multi-asset campaign examples

4. **Supporting documentation**
   - CONTRIBUTING.md (when ready for community contributions)
   - FAQ.md (common questions)
   - api-reference.md (MCP tools detailed reference)

## Testing Strategy

Since no code to test, validation focuses on:

1. **Content accuracy**: Technical specs are correct
2. **Link integrity**: All documentation links work
3. **Example validity**: Prompt examples produce good results
4. **Workflow completeness**: End-to-end workflows have no gaps
5. **User testing**: Real developers can follow quick-start successfully

## Distribution Model

**Current plan** (from README and IMPLEMENTATION_PLAN):

1. **GitHub repository**: Source of truth
2. **ImaginePro marketplace**: Official distribution channel
3. **Community marketplaces**: Secondary distribution
4. **Direct installation**: Local development via file path

Users install via:
```bash
/plugin marketplace add imaginpro/claude-marketplace
/plugin install imaginepro
```

Or local development:
```bash
/plugin marketplace add ./imaginepro-claude-plugin
```

## Future Considerations

From IMPLEMENTATION_PLAN.md, potential v2.0 features:
- State management (gallery, history)
- File operations (auto-save to project)
- Design tool integrations
- Enterprise team features

These would likely require actual implementation code, moving beyond pure markdown.

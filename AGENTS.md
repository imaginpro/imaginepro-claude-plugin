# Agent Guidelines for ImaginePro Claude Plugin

## Build/Lint/Test Commands

This is a documentation-only plugin with no build process. Validation commands:

- **Validate plugin structure**: Check `.claude-plugin/plugin.json` for valid JSON syntax
- **Verify MCP config**: Ensure `.mcp.json` references correct npm package version
- **Test links**: Validate all internal documentation links work
- **Preview markdown**: Check agent/command files render properly

## Code Style Guidelines

### JSON Files
- Use 2-space indentation
- Sort object keys alphabetically where possible
- Include trailing commas for multi-line arrays/objects
- Use double quotes for strings

### Markdown Files
- Use `#` for main headers, `##` for sections, `###` for subsections
- Use bullet points (`-`) for lists, numbered lists (`1.`) for sequences
- Use code blocks with language specifiers for examples
- Keep lines under 100 characters where possible
- Use consistent heading capitalization (Title Case)

### File Naming
- Use kebab-case for file names (e.g., `web-asset-producer.md`)
- Agent files: descriptive names ending with role (e.g., `marketing-creative.md`)
- Command files: action-oriented names (e.g., `imagine-pro.md`)

### Content Structure
- Agents: Follow Expertise → Workflow → Best Practices → Examples format
- Commands: Purpose → Usage → Examples → Tips structure
- Include specific technical specs (dimensions, formats, tools)
- Reference MCP tools by exact names from imaginepro-mcp-server

### Error Handling
- Validate JSON syntax before committing changes
- Check all internal links in documentation
- Ensure examples are accurate and tested
- Follow semantic versioning for plugin updates
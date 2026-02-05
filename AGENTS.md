# Seemodo Documentation Agent Instructions

This is the documentation repository for Seemodo - an AI-powered development platform.

## Project Structure

```
docs/
├── seemodo/              # Main app documentation
│   ├── introduction.mdx  # Overview and getting started
│   ├── getting-started.mdx
│   ├── visual-designer.mdx
│   ├── ai-coder.mdx
│   ├── cloud.mdx
│   ├── sandbox.mdx
│   ├── architecture.mdx
│   ├── configuration.mdx
│   ├── api-reference.mdx
│   ├── credits.mdx
│   └── troubleshooting.mdx
├── api-reference/        # API endpoint documentation
│   ├── introduction.mdx
│   └── endpoint/         # Individual endpoint docs
├── apps/                 # Symlink to source code (READ ONLY)
│   └── seemodo-app/      # -> /Users/chris/Documents/apps/seemodo/seemodo-app
└── docs.json             # Navigation configuration
```

## Critical Rules

1. **NEVER write to `/apps`** - This folder contains symlinks to live source code for reference only
2. Configuration lives in `docs.json` - check it before making structural changes
3. Use MDX format for all documentation pages
4. Run `mint dev` locally to preview changes

## Mintlify Components

Use Mintlify's built-in components. Key ones for this project:

- `<Steps>` - For procedures and tutorials
- `<Tabs>` - For platform-specific or alternative approaches
- `<CodeGroup>` - For showing code in multiple languages
- `<AccordionGroup>` - For FAQ sections and expandable content
- `<CardGroup>` - For feature grids and navigation
- `<ParamField>` - For API parameters
- `<ResponseField>` - For API responses
- `<Warning>`, `<Note>`, `<Tip>` - For callouts

See https://mintlify.com/docs/components for all components.

## Style Guidelines

- Use active voice and second person ("you")
- Keep sentences concise - one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for: file names, commands, paths, code references
- Include mermaid diagrams for architecture and flows

## Content Structure

- Add frontmatter (title, description, icon) to every page
- Include introductory context before diving into steps
- Add "Next steps" or related links where helpful
- Use realistic examples, not placeholders

## Seemodo-Specific Terminology

- **Visual Designer** - The canvas-based UI at `/start`
- **AI Coder** - The OpenCode-powered chat panel
- **Sandbox** - Cloud development environment (Modal/E2B/Vercel)
- **Seemodo Cloud** - Supabase integration feature
- **Flow Generation** - Multi-screen generation (Autoflow)
- **Deep Design** - Enhanced generation mode
- **Max Mode** - Maximum quality generation

## Commands

```bash
# Preview documentation locally
mint dev

# Check for broken links
mint broken-links

# Build for production
mint build
```

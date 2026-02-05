# Seemodo Documentation

Official documentation for [Seemodo](https://seemodo.ai) - the AI-powered development platform.

Built with [Mintlify](https://mintlify.com).

## Documentation Structure

```
docs/
├── seemodo/                    # Seemodo App Documentation
│   ├── introduction.mdx        # Platform overview
│   ├── getting-started.mdx     # Installation & setup
│   ├── visual-designer.mdx     # Canvas-based UI designer
│   ├── ai-coder.mdx            # OpenCode AI assistant
│   ├── cloud.mdx               # Supabase integration
│   ├── sandbox.mdx             # Sandbox providers
│   ├── architecture.mdx        # System architecture
│   ├── configuration.mdx       # Config reference
│   ├── api-reference.mdx       # API overview
│   ├── credits.mdx             # Credit system
│   └── troubleshooting.mdx     # Common issues
│
├── api-reference/              # API Reference
│   ├── introduction.mdx        # API overview
│   └── endpoint/               # Endpoint documentation
│       ├── generate-screen.mdx
│       ├── generate-flow.mdx
│       ├── edit-screen.mdx
│       ├── create-sandbox.mdx
│       ├── sandbox-status.mdx
│       ├── sandbox-files.mdx
│       ├── enhance-prompt.mdx
│       ├── scrape-website.mdx
│       └── seemodo-cloud.mdx
│
├── apps/                       # Source code reference (symlink)
│   └── seemodo-app/            # -> actual app source
│
├── images/                     # Documentation images
├── logo/                       # Brand assets
└── docs.json                   # Navigation config
```

## Symlinked Folders

The `apps/` folder contains symbolic links to the actual app source code for reference:

| Symlink | Target |
|---------|--------|
| `apps/seemodo-app` | `/Users/chris/Documents/apps/seemodo/seemodo-app` |

### Creating the Symlink

```bash
cd /Users/chris/Documents/apps/seemodo/docs
mkdir -p apps
ln -s /Users/chris/Documents/apps/seemodo/seemodo-app apps/seemodo-app
```

> **Important:** Never write to the `apps/` folder - it contains live source code.

## Development

### Prerequisites

Install the Mintlify CLI:

```bash
npm i -g mint
```

### Local Preview

```bash
# Start local server
mint dev

# View at http://localhost:3000
```

### Validation

```bash
# Check for broken links
mint broken-links

# Update CLI
mint update
```

## Publishing

Changes pushed to the main branch are automatically deployed via the Mintlify GitHub app.

Configure deployment at: [Mintlify Dashboard](https://dashboard.mintlify.com)

## Documentation Guidelines

- Use MDX format for all pages
- Include frontmatter (title, description, icon)
- Use Mintlify components for consistent formatting
- Follow the style guide in `AGENTS.md`

## Resources

- [Mintlify Documentation](https://mintlify.com/docs)
- [Mintlify Components](https://mintlify.com/docs/components)
- [Seemodo App](https://seemodo.ai)

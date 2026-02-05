# Seemodo Documentation

Documentation for the Seemodo app, built with [Mintlify](https://mintlify.com).

## Project structure

```
docs/
├── apps/
│   └── seemodo-app -> /Users/chris/Documents/apps/seemodo/seemodo-app (symlink)
├── ai-tools/
├── api-reference/
├── essentials/
├── images/
├── snippets/
└── docs.json
```

## Symlinked folders

The `apps/` folder contains symbolic links to the actual app source code. This allows the documentation to reference and read the real codebase without duplicating files.

### seemodo-app symlink

**Location:** `apps/seemodo-app`  
**Target:** `/Users/chris/Documents/apps/seemodo/seemodo-app`

This symlink provides direct access to the seemodo-app source code from within the docs project. Any changes in the original folder are immediately reflected here.

#### Creating the symlink

```bash
# Navigate to the docs directory
cd /Users/chris/Documents/apps/seemodo/docs

# Create the apps folder
mkdir -p apps

# Create the symbolic link
ln -s /Users/chris/Documents/apps/seemodo/seemodo-app apps/seemodo-app
```

#### Verifying the symlink

```bash
ls -la apps/
# Output: seemodo-app -> /Users/chris/Documents/apps/seemodo/seemodo-app
```

> **Note:** Symlinks are not copies - they reference the original files. Deleting the symlink does not delete the source files.

## Development

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) to preview your documentation changes locally. To install, use the following command:

```
npm i -g mint
```

Run the following command at the root of your documentation, where your `docs.json` is located:

```
mint dev
```

View your local preview at `http://localhost:3000`.

## Publishing changes

Install our GitHub app from your [dashboard](https://dashboard.mintlify.com/settings/organization/github-app) to propagate changes from your repo to your deployment. Changes are deployed to production automatically after pushing to the default branch.

## Need help?

### Troubleshooting

- If your dev environment isn't running: Run `mint update` to ensure you have the most recent version of the CLI.
- If a page loads as a 404: Make sure you are running in a folder with a valid `docs.json`.

### Resources
- [Mintlify documentation](https://mintlify.com/docs)

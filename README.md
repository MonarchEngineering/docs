# Airtop Documentation

This repository contains the documentation for Airtop, built with [Mintlify](https://mintlify.com).

## Prerequisites

- Node.js v19 or higher
- npm package manager

## Installation

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd docs
   ```

2. Install the Mintlify CLI globally:
   ```bash
   npm i -g mint
   ```

   Alternatively, you can run without installing globally:
   ```bash
   npx mint dev
   ```

## Development

To run the documentation site locally:

```bash
mint dev
```

This will start the development server at `http://localhost:3000`. The site will automatically reload when you make changes to the documentation files.

### Custom Ports

To run on a different port:

```bash
mint dev --port 3333
```

If the default port is in use, it will automatically use the next available port.

### Preview as Specific Group

If you use partial authentication, you can preview as a specific group:

```bash
mint dev --groups admin
```

## Additional CLI Commands

### Find Broken Links
```bash
mint broken-links
```

### Find Accessibility Issues
```bash
mint a11y
```

### Check OpenAPI Spec
```bash
mint openapi-check <OpenAPI filename or URL>
```

### Rename Files
```bash
mint rename <path/to/old-filename> <path/to/new-filename>
```

### Update CLI
```bash
mint update
```

## Deployment

The documentation is automatically deployed when changes are pushed to the main branch. The deployment process is handled by Mintlify's hosting service.

## Project Structure

```
docs/
├── guides/                 # User guides and tutorials
│   ├── introduction.mdx
│   ├── quick-start.mdx
│   ├── authentication.mdx
│   ├── bot-detection.mdx
│   └── triggers.mdx
├── integrations/          # Integration documentation
│   ├── airtable.mdx
│   ├── github.mdx
│   ├── google-*.mdx
│   └── ...
├── connections/           # External service integrations
│   ├── make.mdx
│   ├── n8n.mdx
│   ├── zapier.mdx
│   └── ...
├── images/               # Static images
├── logo/                 # Logo assets
├── docs.json            # Mintlify configuration
└── README.md            # This file
```

## Writing Documentation

- All documentation is written in MDX format
- Images should be placed in the `images/` directory
- Use the existing page structure as a template for new pages
- Follow the navigation structure defined in `docs.json`

## Configuration

The main configuration is in `docs.json`. This file contains:
- Site metadata (name, colors, favicon)
- Navigation structure
- Global settings
- Footer configuration

## Troubleshooting

### Common Issues

**Error: Could not load the "sharp" module using the darwin-arm64 runtime**
1. Remove the currently-installed version: `npm uninstall -g mint`
2. Upgrade to Node.js v19 or higher
3. Reinstall the CLI: `npm install -g mint`

**Permission denied error**
Run with sudo: `sudo npm i -g mint`

**Local preview doesn't match production**
Run `mint update` to get the latest changes.

**Unknown error**
Delete the `~/.mintlify` folder and run `mint dev` again

## Getting Help

- [Mintlify Documentation](https://mintlify.com/docs)
- [Mintlify Community](https://mintlify.com/community)
- [MDX Documentation](https://mdxjs.com/)

## Contributing

1. Make your changes to the documentation files
2. Test locally using `mint dev`
3. Commit your changes
4. Push to the main branch for automatic deployment

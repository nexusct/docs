# NexusCT Documentation

This is the official documentation site for NexusCT, built with [Mintlify](https://mintlify.com). The site is written in MDX (Markdown + JSX) and includes:

- Guide pages
- Navigation
- Customizations
- API Reference pages
- Interactive components

## Getting Started

### Prerequisites

- Node.js version 18.10.0 or higher
- npm or yarn package manager

### Local Development

1. **Clone the repository**

   ```bash
   git clone https://github.com/nexusct/docs.git
   cd docs
   ```

2. **Install the Mintlify CLI globally**

   ```bash
   npm i -g mintlify
   ```

   Or with yarn:

   ```bash
   yarn global add mintlify
   ```

3. **Start the development server**

   Run the following command at the root of your documentation (where `mint.json` is located):

   ```bash
   mintlify dev
   ```

   The documentation website will be available at `http://localhost:3000`.

4. **Using custom ports**

   If port 3000 is already in use, specify a different port:

   ```bash
   mintlify dev --port 3333
   ```

### Configuration

The main configuration file is `mint.json` at the root of the repository. This file controls:

- Site name and branding
- Navigation structure
- Color scheme
- API reference integration
- Footer links and social media

Refer to the [Mintlify documentation](https://mintlify.com/docs) for detailed configuration options.

## Deployment

Changes pushed to the `main` branch are automatically deployed to production via the Mintlify GitHub App. You can monitor deployments from your [Mintlify dashboard](https://dashboard.mintlify.com).

### Manual Deployment

If automatic deployment is not working, you can manually trigger a deployment through the [Mintlify dashboard](https://dashboard.mintlify.com).

## Project Structure

```
.
├── mint.json              # Main configuration file
├── introduction.mdx       # Home page
├── quickstart.mdx         # Quick start guide
├── development.mdx        # Development guide
├── api-reference/         # API documentation
│   ├── introduction.mdx
│   ├── openapi.json      # OpenAPI specification
│   └── endpoint/         # API endpoint examples
├── essentials/           # Essential guides
├── images/               # Image assets
├── logo/                 # Logo assets
└── snippets/             # Reusable content snippets
```

## Troubleshooting

### Mintlify dev isn't running

Run `mintlify install` to re-install dependencies, then try `mintlify dev` again.

### Page loads as a 404

Make sure you are running the command in the folder containing `mint.json`.

### Port already in use

If you see `Error: listen EADDRINUSE: address already in use :::3000`, use a different port with the `--port` flag.

### Local site looks different than production

Update the Mintlify CLI to the latest version:

```bash
npm i -g mintlify@latest
```

## Contributing

1. Create a new branch for your changes
2. Make your changes and test locally with `mintlify dev`
3. Submit a pull request to the `main` branch
4. Wait for review and automatic deployment upon merge

## Security

For security concerns or to report vulnerabilities, please see [SECURITY.md](./SECURITY.md).

## License

This documentation is maintained by NexusCT.

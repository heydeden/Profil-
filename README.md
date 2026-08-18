# DevLens

> Free, fast developer tools for API, JSON, security, and web debugging.

DevLens is a client-side developer toolbox designed to make common development tasks fast and frictionless. It is intentionally lightweight: no account, database, or DevLens backend is required for the current MVP.

## Current tools

- JSON Formatter
- JSON Diff
- JSONPath Tester
- API Request Builder
- cURL Converter
- HTTP Status Codes
- HTTP Headers Analyzer
- JWT Decoder
- Security Headers reference
- URL Toolkit
- SQL Formatter

## Principles

- Free to use
- Client-side processing whenever possible
- No automatic persistence of tool input
- No DevLens API proxy in the MVP
- Minimal dependencies
- Scalable category and tool structure

## Development

This MVP is a dependency-free static web app. Serve the repository with any static server, or use the included npm scripts.

```bash
npm run build
npm run preview
```

## Adding a tool

Keep tool metadata in `src/app.js` for the current MVP. Future iterations should extract the registry into dedicated modules so categories, routes, keywords, and related tools remain data-driven as the toolbox grows.

## Deployment

The repository is intended to work with static hosts such as Netlify. AppDeploy can be used for preview/QA deployments.

## License

See `LICENSE`.

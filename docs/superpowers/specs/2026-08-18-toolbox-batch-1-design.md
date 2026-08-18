# DevLens Toolbox Batch 1 Design

## Goal
Expand DevLens with more than ten high-value client-side developer tools while preserving the current static, privacy-conscious architecture.

## Scope
New tools: JSON → TypeScript, JSON Schema, UUID, Hash, Password, Timestamp/DateTime, Regex, Encoding, Query String, Color/Contrast, Cron, IP/CIDR, Markdown, Case Converter, Mock JSON. Existing JSON Diff, cURL, JWT, URL, API, SQL and HTTP tools remain available.

## Architecture
Keep the single-page hash router and data-driven `TOOLS` registry. Tool logic remains local in `src/app.js` for this batch to avoid an unrelated module migration. All transformations happen in the browser; no new backend, database, account system, analytics, or remote persistence is introduced.

## UX
Every tool has a clear input, action, result, copy action where useful, validation/error output, and related tools. Search remains global. New tools are grouped into JSON & Data, Security, Text & Encoding, Web & URL, and Developer Utilities.

## Security / Privacy
Use Web Crypto for hashes and UUID/password randomness. Never transmit inputs. Escape user-generated HTML. Markdown preview only renders a constrained, escaped subset. JWT remains decode-only and explicitly warns that decoding is not signature verification.

## Testing
Verify build, route rendering, representative happy paths, invalid-input paths, responsive layout, and that existing tools remain reachable. AppDeploy E2E is the deployment gate.

# DevLens Toolbox Batch 1 Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Ship 15 new client-side developer tools without introducing backend dependencies.

**Architecture:** Extend the existing registry/router and keep tool implementations in `src/app.js` for this batch. Reuse existing workspace/card styles and add only focused controls needed by new tools.

**Tech Stack:** Vanilla JavaScript, HTML, CSS, Web Crypto, browser URL/Intl APIs.

**Spec:** `docs/superpowers/specs/2026-08-18-toolbox-batch-1-design.md`

## Global Constraints

- Keep all tool input processing client-side.
- Do not add accounts, database, backend proxy, or analytics.
- Escape user-controlled HTML.
- Use Web Crypto for cryptographic randomness and hashes.
- Keep existing tool routes working.

---

### Task 1: Registry and UX foundation

**Files:** Modify `src/app.js`, `styles.css`.

- [ ] Add the 15 tool registry entries and group them into existing categories.
- [ ] Add reusable copy button behavior and result rendering helpers.
- [ ] Add favorites using opt-in LocalStorage and a recent-tools list using LocalStorage.
- [ ] Preserve existing search and hash routes.
- [ ] Run `npm run build` and confirm exit 0.

### Task 2: JSON and data generators

**Files:** Modify `src/app.js`.

- [ ] Implement JSON → TypeScript with nested objects/arrays.
- [ ] Implement JSON Schema generation.
- [ ] Implement Mock JSON from a small field-definition grammar.
- [ ] Add invalid-input messages and copyable results.
- [ ] Run `npm run build`.

### Task 3: Security and identity tools

**Files:** Modify `src/app.js`.

- [ ] Implement UUID v4 generation/validation using `crypto.randomUUID` or Web Crypto.
- [ ] Implement SHA-1/SHA-256/SHA-384/SHA-512 using `crypto.subtle.digest`.
- [ ] Implement password generation using `crypto.getRandomValues`.
- [ ] Run `npm run build`.

### Task 4: Text and encoding tools

**Files:** Modify `src/app.js`.

- [ ] Implement Regex tester with flags, match summary, and replace preview.
- [ ] Implement Base64, URL, and HTML entity encoding/decoding.
- [ ] Implement case conversion.
- [ ] Implement constrained Markdown preview with escaped source.
- [ ] Run `npm run build`.

### Task 5: Web and developer utility tools

**Files:** Modify `src/app.js`.

- [ ] Implement Timestamp/DateTime conversion.
- [ ] Implement query-string parser/builder.
- [ ] Implement HEX/RGB/HSL conversion and WCAG contrast ratio.
- [ ] Implement five-field Cron builder/explainer.
- [ ] Implement IPv4/CIDR calculator.
- [ ] Run `npm run build`.

### Task 6: Deployment and regression verification

**Files:** Modify `tests/tests.txt` if using AppDeploy snapshot tests.

- [ ] Verify representative routes for new tools and existing JSON/API/JWT tools.
- [ ] Verify mobile workspace layout.
- [ ] Deploy through AppDeploy and inspect QA/runtime output.
- [ ] Update Linear issues to Done only after verification.
- [ ] Record remaining work explicitly in Linear.

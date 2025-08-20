# Accessibility Done Wrong

This project demonstrates how to test against the [WCAG 2.2 Level AA standard](https://www.w3.org/TR/WCAG22/) and ensure accessibility compliance across the full development process.

## How We Ensure WCAG 2.2 Level AA Compliance

- [Use Figma plugins to create accessible designs](#figma-plugins)
- [Test accessibility during local development](#local-development-testing)
- [Run automated accessibility checks in Github Actions](#github-actions)
- [Configure Gemini Code Assist to include accessibility in code reviews](#gemini-code-assist)
- [Manual testing](#manual-testing)

## Figma Plugins

tbd

## Local Development Testing

To catch accessibility issues early in the development cycle, we use the following tools:

- [eslint-plugin-jsx-a11y](https://www.npmjs.com/package/eslint-plugin-jsx-a11y) – Linting rules for accessibility in React JSX
- [@axe-core/react](https://www.npmjs.com/package/@axe-core/react) – Runtime accessibility checks in React apps
- ...

## Github Actions

Accessibility checks are integrated into our CI pipeline:

- **On every branch**, local development tools continue to run to catch issues early.
- **On every pull request**, we run additional automated auditing tools that warn about accessibility issues without blocking the merge:
  - [lighthouse-ci](https://github.com/GoogleChrome/lighthouse-ci)
  - [pa11y-ci](https://www.npmjs.com/package/pa11y-ci)
  - [@axe-core/cli](https://www.npmjs.com/package/@axe-core/cli)

## Gemini Code Assist

We configure Gemini Code Assist to enforce accessibility guidelines during code reviews. It follows the requirements defined in our [styleguide.md](.gemini/styleguide.md), ensuring consistent accessibility feedback across the codebase.

## Manual testing

While this project uses various tools to help test accessibility against the [WCAG 2.2 Level AA standard](https://www.w3.org/TR/WCAG22/), it’s important to understand that not all accessibility criteria can be fully validated through automated testing. Many guidelines require manual inspection or individual judgment to achieve full accessibility compliance.

_TODO: Add a guide for manual testing to complement automated checks and ensure the application is truly accessible to all users._

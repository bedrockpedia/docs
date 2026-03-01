# 📚 Bedrockpedia Docs

Welcome to the open-source content repository for **[BedrockPedia](https://bedrockpedia.vercel.app)**!

This repository manages the Markdown (`.mdx`) documentation, legal pages, landing page configurations, and resources for the entire BedrockPedia website. We use [Contentlayer](https://contentlayer.dev/) to process these files during build time.

## 🗂️ Directory Structure

```text
docs/
├── pmmp/         # PocketMine-MP Guides & How-To
├── pnx/          # PowerNukkitX Guides & How-To
├── nukkit/       # Nukkit Guides & How-To
├── allay/        # Allay (Coming Soon)
├── dragonfly/    # Dragonfly (Coming Soon)
├── resource-packs/# Resource Packs
├── mods/         # Mods & Addons
└── bedrock-server/# Bedrock Dedicated Server

```

## 📝 How to Contribute to the Docs

We gladly accept contributions to improve or expand the BedrockPedia documentation. To add or modify documentation, follow these structural rules:

### 1. File Format

All documentation files must use the `.mdx` extension. MDX allows you to use Markdown alongside React components.

### 2. Frontmatter

Every single file must start with YAML Frontmatter indicating its metadata:

```yaml
---
title: Introduction to PMMP
description: A complete guide to setting up your first PocketMine-MP server.
---
```

### 3. Adding New Pages

When you add a new page (e.g. `content/docs/pmmp/how-to/my-new-page.mdx`), you **must** also update the appropriate `routes.json` file in that parent directory so that it appears in the sidebar navigation.

Example of a `routes.json` addition:

```json
{
  "title": "My New Page",
  "path": "/docs/pmmp/how-to/my-new-page"
}
```

## ⚙️ Components Available in MDX

Because BedrockPedia runs on modern React tooling, you can use various built-in custom UI components in your markdown. Some useful components include:

- `<CodeBlock />` : For syntax-highlighted code with a copy button.
- `<Callout title="Note" type="info">` : For emphasis or warnings.
- `<Steps>` : For step-by-step tutorials.

## 🤝 Contribution Guidelines

1. **Keep it Objective**: Documentation should be clear, concise, and helpful. Avoid opinionated statements.
2. **Standardize Naming**: Use clear, kebab-casing for filenames (e.g. `server-configuration.mdx`).
3. **Verify locally**: If you're running the actual BedrockPedia frontend locally, make sure your markdown renders without console errors. If you just have this content repository, use standard markdown linting.
4. **Pull Requests**: Submit your changes to the `main` branch. A maintainer will review your additions and merge them.

## 📄 License

The content in this repository is licensed under the MIT License unless stated otherwise.

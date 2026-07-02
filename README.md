# King - Personal Website

A personal website built with Hugo and the Stack theme.

## Features

- Multi-language support (Chinese, English, Arabic)
- Responsive design
- Dark mode toggle
- Search functionality
- Archive and category pages
- Tag cloud
- Social links
- Article pagination

## Tech Stack

- **Hugo** - Static site generator
- **Stack Theme** - Hugo theme for personal blogs
- **GitHub Pages** - Hosting platform
- **GitHub Actions** - CI/CD deployment

## Quick Start

### Prerequisites

- Hugo Extended version 0.150.1 or later
- Git

### Local Development

```bash
# Clone the repository
git clone https://github.com/kinguang3/King.git
cd King

# Start development server
hugo server

# Build for production
hugo --minify
```

### Preview

- Development: http://localhost:1313/King/
- Production: https://kinguang3.github.io/King/

## Project Structure

```
.
├── archetypes/          # Content templates
├── assets/              # Static assets (CSS, JS)
├── content/             # Site content (Markdown)
├── static/              # Static files (images, favicon)
├── themes/              # Hugo themes
│   └── hugo-theme-stack/
├── .github/
│   └── workflows/
│       └── gh-pages.yml # GitHub Actions workflow
├── hugo.yaml            # Hugo configuration
└── .gitignore           # Git ignore rules
```

## Deployment

This site is automatically deployed to GitHub Pages via GitHub Actions.

### Workflow

1. Push changes to the `main` branch
2. GitHub Actions triggers the build workflow
3. Hugo builds the site and deploys to GitHub Pages

### Manual Deployment

```bash
# Build the site
hugo --minify

# The output is in the public/ directory
```

## Configuration

### Base URL

The base URL is configured in `hugo.yaml`:

```yaml
baseurl: https://kinguang3.github.io/King
```

### Languages

Supported languages:
- Chinese (zh-cn) - Default
- English (en)
- Arabic (ar)

### Theme

Using the Stack theme:

```yaml
theme: hugo-theme-stack
```

## License

This project is for personal use.

## Credits

- [Hugo](https://gohugo.io/)
- [Stack Theme](https://github.com/CaiJimmy/hugo-theme-stack)
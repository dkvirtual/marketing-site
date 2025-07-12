# Marketing Site

This repository contains the marketing site for Deutsche Kraniche Virtual.

## Quick Start

### Prerequisites
- Hugo (extended version recommended)
- Node.js and npm (for Tailwind CSS)

### Installation

1. **Install Hugo** (if not already installed):
   ```bash
   # macOS
   brew install hugo
   
   # Or download from https://gohugo.io/installation/
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

### Development

1. **Serve locally with live reload**:
   ```bash
   hugo serve
   ```
   Visit http://localhost:1313 to preview error pages

2. **Build for production**:
   ```bash
   hugo
   ```
   Static files will be generated in `public/` directory

## Adding New Pages

This Hugo site supports multilingual content with separate content directories for each language.

### Content Structure

Content files are organized in the `content/` directory by language:
```
content/
├── en/     # English content
├── de/     # German content  
├── fr/     # French content
├── it/     # Italian content
└── nl/     # Dutch content
```

### Creating a New Page

1. **Create content files for each language**:
   ```bash
   # Example: Adding a new "about" page
   touch content/en/about.md
   touch content/de/about.md
   touch content/fr/about.md
   touch content/it/about.md
   touch content/nl/about.md
   ```

2. **Add front matter and content**:
   ```markdown
   ---
   title: "About Us"
   layout: "standard"  # or custom layout name
   ---
   
   Your page content here...
   ```

3. **Custom layouts** (optional):
   - Create layout files in `layouts/` directory
   - Use existing layouts: `standard.html`, `single.html`, or page-specific layouts like `faq.html`

4. **Add global translations** (if needed):
   - Update translation files in `i18n/` directory (en.yaml, de.yaml, etc.)

### Page Types

- **Standard pages**: Use `layout: standard` for basic content pages
- **Custom pages**: Create specific layouts (like `faq.html`) for pages with special formatting
- **Home pages**: Use `_index.md` files for section landing pages

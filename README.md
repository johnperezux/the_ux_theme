# Teth Space Theme
A custom WordPress theme built from scratch by Johnathan Perez.

## Overview
A fully custom, lightweight WordPress theme with native Gutenberg block support, custom post type architecture, and optimized asset loading via Vite. Built to be compatible with ACF for dynamic customization, WooCommerce, and Gravity Forms without requiring them.

## Features

- Built from scratch and no parent theme or page builder dependency
- Full Gutenberg / block editor support
- Custom post types & taxonomies
- Optimized CSS/JS build process using Vite
- Compatible with Advanced Custom Fields (ACF) — not required
- Compatible with Gravity Forms — not required
- Compatible with WooCommerce — not required
- Responsive, mobile-first layout

## Compatibility

This theme is built to be compatible with (but does not require):

- **Advanced Custom Fields (ACF)** — templates are structured to support dynamic fields and custom blocks if ACF is active
- **Gravity Forms** — includes styling/markup overrides for a seamless, on-brand form experience if the plugin is active
- Works as a standalone theme with core WordPress + Gutenberg if neither plugin is installed

## Requirements

- WordPress 6.x+
- PHP 8.x+
- Node.js (for building/compiling assets via Vite)

## Installation

1. Download or clone this repository into `wp-content/themes/`
2. Activate the theme from the WordPress admin (Appearance > Themes)
3. (Optional) Install ACF, WooCommerce, and Gravity Forms for extended functionality

## Build Process

CSS and JS are authored in `/src` and compiled/minified via [Vite](https://vitejs.dev/).

**Setup**
```bash
npm install
```

**Development (watch mode)**
```bash
npm run dev
```

**Production build**
```bash
npm run build
```

Compiled, minified assets are output to `/assets/css` and `/assets/js` and enqueued automatically via `functions.php`.

## Folder Structure

```
teth_space_theme/
├── src/                 # Vite source files (Sass/JS, not enqueued directly)
├── assets/
│   ├── css/              # Compiled, minified CSS
│   ├── js/                # Compiled, minified JS
│   └── images/
├── template-parts/     # Reusable template partials
├── inc/                    # Functions split by purpose (CPTs, enqueue, ACF)
├── functions.php
├── style.css
├── index.php
├── 404.php
├── header.php
├── footer.php
├── single.php
└── README.md
```

## Custom Post Types

| Post Type | Description |
|---|---|
| `example_cpt` | [What it's for] |

## Database

This theme does not directly interact with the database — all data is retrieved through standard WordPress and ACF functions. No custom tables or direct queries are used.

## Development Notes

- Assets are enqueued conditionally to avoid loading unused CSS/JS
- Cache-busting is handled via file modification time on enqueued assets
- Local dev environment: Local by Flywheel

## Author

**Johnathan Perez**
[Portfolio / contact info]

## License

GPL-2.0+ (standard for WordPress theme distribution)
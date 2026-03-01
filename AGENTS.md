# UX Speed (uxspeed.dev)

Measuring and Improving Speed of User Experience (A/FKA Web Performance).

## Architecture

This is a static website deployed as a **Cloudflare Worker** using the **Workers Assets** feature.

- **Public Assets**: All static files (HTML, CSS, images) are located in the `public/` directory.
- **Configuration Files**: Located in the root (e.g., `package.json`, `wrangler.jsonc`).

## Tech Stack

- **Hosting**: Cloudflare Workers
- **Language**: Static HTML/CSS, no JavaScript for Worker
- **Formatting**: Prettier (configured in `.prettierrc`)
- **Package Manager**: npm

## Configuration

- **wrangler.jsonc**: Configures the Worker name (`uxspeed-dev`), assets directory (`public`), and custom domain (`uxspeed.dev`).
- **.prettierrc**: Provides code formatting and includes overrides for `.jsonc` files to use the JSON parser.

## Deployment

Deployments are done automatically by pushing to GitHub repository main branch.

## Image Standards

Images are stored in `public/images/`.

- Always set explicit `width` and `height` attributes on `<img>` tags to prevent layout shift.
- CSS for `.thumbnail` sets `width: 100%` and `height: auto`.

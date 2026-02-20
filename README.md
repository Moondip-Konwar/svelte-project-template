# Svelte Project Template

A minimal, static SvelteKit project template with Tailwind CSS, TypeScript, and pnpm.  
Designed for static hosting (GitHub Pages, Cloudflare Pages, Netlify, etc.) and easy customization.

## Features

- SvelteKit with `adapter-static`
- TypeScript enabled
- Tailwind CSS (no opinionated plugins by default)
- pnpm package manager
- Static-site friendly configuration
- Minimal project structure for templates



## Project Structure

```

.
├── src/
│   ├── lib/            # Reusable components and assets
│   ├── routes/         # SvelteKit routes
│   └── app.html
├── static/              # Static assets (robots.txt, images, etc.)
├── svelte.config.js
├── tailwind config (via @tailwindcss/vite)
└── vite.config.ts

```

 

## Getting Started

### Create a new project from this template

```sh
git clone https://github.com/YOUR_USERNAME/svelte-project-template.git my-app
cd my-app
pnpm install
```



## Development

Start the dev server:

```sh
pnpm dev
```

Open in browser:

```sh
pnpm dev --open
```


## Build (Static Output)

```sh
pnpm build
```

Preview the production build:

```sh
pnpm preview
```

The static site will be generated in the `build/` directory.

 

## GitHub Pages Deployment

### Set base path in `svelte.config.js`

```js
paths: {
  base: process.env.NODE_ENV === "production" ? "/REPO_NAME" : "",
}
```

Replace `REPO_NAME` with your GitHub repository name.

 

### Optional: Environment-based base path

```sh
BASE_PATH=/my-project pnpm build
```

```js
base: process.env.BASE_PATH || "";
```

 

## Static Routing Notes

- `fallback: "404.html"` is enabled for SPA routing on static hosts.
- Dynamic routes must be prerendered manually if used.

 

## Tailwind CSS

Tailwind is installed with no plugins by default.
Add optional plugins manually if needed:

```sh
pnpm add -D @tailwindcss/typography @tailwindcss/forms
```

 

## Fonts

The template currently uses Google Sans via CSS import.
You may replace it with system fonts or self-hosted fonts for better performance and privacy.

 

## Package Manager

This project uses **pnpm**.

Install pnpm if needed:

```sh
corepack enable
corepack prepare pnpm@latest --activate
```

 

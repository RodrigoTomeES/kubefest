# Repository for hosting the website kubefest.com

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
.
├── infra
│   ├── backend.tf
│   ├── main.tf
│   ├── provider.tf
│   └── variables.tf
├── public
│   ├── CNAME
│   ├── favicon.svg
│   └── images
├── src
│   ├── components
│   ├── layouts
│   ├── pages
│   └── styles
├── astro.config.mjs
├── README.md
├── package.json
├── tsconfig.json
└── yarn.lock
```

Astro looks for `.astro` or `.md` files in the `src/pages/` directory. Each page is exposed as a route based on its file name.

There's nothing special about `src/components/`, but that's where we like to put any Astro/React/Vue/Svelte/Preact components.

Any static assets, like images, can be placed in the `public/` directory.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                | Action                                           |
| :--------------------- | :----------------------------------------------- |
| `yarn install`         | Installs dependencies                            |
| `yarn dev`             | Starts local dev server at `localhost:4321`      |
| `yarn build`           | Build your production site to `./dist/`          |
| `yarn preview`         | Preview your build locally, before deploying     |
| `yarn format`          | Format code with Prettier                        |
| `yarn astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `yarn astro -- --help` | Get help using the Astro CLI                     |

## 🏗️ Infrastructure

### Overview

This Terraform configuration allows you to:

- Provision a Cloudflare zone.
- Manage DNS records within the Cloudflare zone.
- Ensure consistency and reproducibility of infrastructure changes.

### Usage

**_Validate Stage (On Pull Requests)_**
In this stage, Terraform configurations are validated whenever a pull request is opened. This ensures that proposed changes adhere to Terraform best practices and do not introduce syntax errors.

**_Deploy Stage (On Master Branch)_**
In this stage, Terraform configurations are applied to deploy infrastructure when changes are merged into the master branch. This ensures that the changes are automatically deployed to production-like environments.

## 👀 Want to learn more?

Feel free to check [Astro documentation](https://docs.astro.build).

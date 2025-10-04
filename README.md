# TiffyThrifty

This repository contains the monorepo for the **TiffyThrifty** project. The goal of the application is to showcase curated products at different price tiers, allow customers to add items to a cart, and complete a checkout using Stripe. The backend runs on Base44 serverless functions using Deno, and the frontend is built with React and Vite.

## Repository layout

```
tiffythrifty/
├─ apps/
│  ├─ web/                 # React + Vite frontend
│  └─ functions/           # Base44 (Deno) serverless functions
├─ packages/
│  └─ shared/              # Shared types, constants, utilities
├─ infra/
│  ├─ devcontainer/        # Codespaces configuration
│  ├─ docker/              # Dockerfiles & docker-compose definitions
│  ├─ scripts/             # Helper scripts (e.g. Stripe helpers)
│  └─ github/              # GitHub Actions workflows
├─ .editorconfig           # Editor configuration for consistent formatting
├─ .gitignore              # Files and directories to ignore in version control
├─ .gitattributes          # Git configuration attributes
├─ .nvmrc                  # Specifies the Node.js version
├─ deno.json               # Shared Deno configuration for functions
├─ package.json            # Root package configuration with pnpm workspaces
├─ pnpm-workspace.yaml     # pnpm workspace setup
├─ .env.example            # Template for environment variables
└─ README.md               # This documentation
```

## Getting started

This repository uses the [pnpm](https://pnpm.io) package manager. To install dependencies and run the development environment, ensure you have Node.js installed (version 20) and then execute the following commands from the root of the repository:

```bash
corepack enable
pnpm install
pnpm dev
```

The `dev` script will start the frontend development server. Additional scripts such as `build`, `lint`, `typecheck`, and `test` are available via npm scripts defined in the root `package.json`.

See the `infra/` directory for Codespaces and Docker configuration, and refer to the documentation throughout the project for details on deploying functions to Base44 and setting up the backend.

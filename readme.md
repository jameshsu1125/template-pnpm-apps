# pnpm workspace installation guide

```
pnpm add typescript -D -w  # install pkgs globally , -w: --workspace-root
pnpm add typescript -D --filter pkg-a # install certain pkg
```

for more information about the repo workspace, please check the `pnpm-workspace.yaml` config file.

## LIFF (Line In-App Frontend Framework) Web App Project

This is a general guide for LIFF Web App. Please check the specific app for more information.

## Development Guides

Install project dependencies:

```sh
pnpm install
```

Start the development server:

```sh
pnpm dev
```

Because the HTTPS connection is required by LIFF, you can start the https server by

```sh
pnpm dev:https
```

## Technical Stacks

- pnpm
  - package manager
  - workspace for monorepo management
- React
  - frontend UI library
  - React-related ecosystem libs: `react-router-dom`, `react-hook-form`, `react-query`.
- Vite
  - the front end bundler
- Tailwind CSS
  - the popular CSS frameworks
- Prettier & Eslint
  - code formatter and linter
  - custom rules are defined inside `.eslintrc.cjs` and `.prettierrc.json`.
- Netlify
  - Internal testing link deployment environment during the staging phase

## Branch Workflow

- `master`
  - default branch and commonly used for all products.
- `feat`
  - new feature or wish
- `rel`
  - ready to release

When the new release branch is ready, please someone manually sync to the Appier internal repo.

## Testing Environments

There are different `.env` files for deployment listed in the following:

- `.env.example`
  - an env example template file. Please duplicate this file and rename it to the ones below.
- `.env.local`
  - for development use and will be ignored by git.
- `.env.staging`
  - for internal QA testing process.
- `.env.prod`
  - for real world production release.

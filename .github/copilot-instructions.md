# Copilot AI Agent Instructions

## Monorepo & Service Structure

- This repo is a monorepo for multiple services. Each service (e.g., `copilot-service1`) is self-contained under `services/`.
- Each service may have its own `.github/copilot-instructions.md` for service-specific details. This file is the root/global guide.

## Architecture & Patterns

- **Service Isolation:** Each service is independent, with its own dependencies, configs, and workflows.
- **No cross-service imports**: Services do not import code from each other.
- **No shared backend/data layer**: Each service is frontend-only unless otherwise documented.
- **Next.js App Router:** All Next.js services use the `app/` directory (not `pages/`).
- **TypeScript strict mode** and path aliasing (`@/*`) are standard.

## Developer Workflows

- **Install dependencies:** Use the package manager specified in each service's `package.json` (e.g., `yarn install` in `services/copilot-service1/`).
- **Development:** Run `yarn dev` (or `npm run dev`, etc.) in the service directory.
- **Build:** Run `yarn build` in the service directory.
- **Lint:** Run `yarn lint` (uses `eslint-config-next` with custom ignores).
- **Styling:** Tailwind CSS via PostCSS, configured per service.

## Project Conventions

- **No backend logic** in frontend services unless explicitly documented.
- **No custom server**: Use default Next.js server unless noted.
- **Static assets** go in each service's `public/` directory.
- **Fonts:** Use `next/font` and CSS variables for font management.
- **Dark mode:** Handled via CSS variables and `prefers-color-scheme`.

## Integration & External Dependencies

- **Next.js**: See each service's `next.config.ts` for custom config.
- **Tailwind CSS**: Integrated via PostCSS plugin.
- **No database or API** unless documented in the service's instructions.

## Examples

- To edit a service's main page: `services/<service>/app/page.tsx`
- To change global styles: `services/<service>/app/globals.css`
- To update layout or fonts: `services/<service>/app/layout.tsx`

## Additional Notes

- **Deployment:** Each service is deployable independently (Vercel recommended for Next.js).
- **For service-specific rules:** See `services/<service>/.github/copilot-instructions.md` if present.

---

For more, see each service's `README.md` or Next.js docs: https://nextjs.org/docs

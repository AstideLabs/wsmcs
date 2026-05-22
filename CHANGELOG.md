# Changelog

## Responsive Layout Fixes

- **Footer.vue**: Refactored to use Flexbox and CSS Grid, resolving text overlap and optimizing horizontal space usage on mobile.
- **Home.vue**: Fixed horizontal overflow on extremely narrow viewports by replacing fixed widths with max-widths in the Join Banner.
- **Navbar.vue**: Adjusted horizontal paddings to use responsive constraints (`px-4 md:px-11`) to prevent overflow on mobile.
- **FeatureCard & TeamCard**: Removed `whitespace-nowrap` constraints, allowing text to properly wrap or truncate on narrow screens.
- **Hero Section**: Converted the hero banner from absolute positioning with a fixed height to standard document flow with `min-h-[770px]`, preventing content from overflowing into the next section.

## Phase 1 Implementation (Initial Setup)

- **Project Initialization**: Scaffolded a new Vue 3 + TypeScript project using Vite (`pnpm`).
- **Styling**: Installed and configured `@tailwindcss/vite` (Tailwind CSS v4). Extracted design tokens (colors, fonts, etc.) from the Figma design and defined them in `src/styles/tailwind.css` to eliminate magic numbers.
- **Routing**: Installed `vue-router` and set up the base routing for the Home page.
- **Project Structure**: Established the strict directory structure as mandated by `GEMINI.md` (`src/assets`, `src/components/common|layout|ui`, `src/layouts`, `src/pages`, `src/styles`, etc.).
- **Component Development**:
  - **UI Components**: `Button.vue`, `SectionTitle.vue`.
  - **Common Components**: `FeatureCard.vue` (for game modes), `TeamCard.vue` (for team members).
  - **Layout Components**: `Navbar.vue` (header with logo and links), `Footer.vue` (links grid and social icons), and `DefaultLayout.vue`.
- **Page Assembly**: Constructed `Home.vue` matching the "主页" Figma design, including the Hero section, Features section, Team section, and the bottom Join banner.
- **Asset Localization**: Downloaded all remote image assets from Figma into `src/assets/images` and replaced external URLs with local imports.
- **Verification**: Ensured `pnpm build` passes with zero TypeScript or compilation errors.

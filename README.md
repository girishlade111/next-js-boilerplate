# Next.js Boilerplate — Landing Page + UI Component Library

A production-ready Next.js 15 boilerplate for marketing sites: a polished,
animated landing page (hero, features, testimonials, pricing, blog, FAQ, CTA)
plus a browsable **UI component library showcase** with reusable building blocks
— page transitions, scroll reveals, mode toggle, site header/footer, and custom
cursor effects.

## What it does

- **Landing page** (`/`): full marketing homepage with red-glow cursor effect
  (`MouseGlow`), hero, features, component-library showcase, testimonials,
  pricing, blog preview, FAQ, and call-to-action sections.
- **UI Library page** (`/ui-library`): showcases the bundled components/effects
  so you can preview building blocks before using them.
- Reusable section components in `components/sections/`
  (`hero-section`, `features-section`, `pricing-section`, `faq-section`, …)
- Extra effects in `components/ui-library/effects/` (e.g. mouse-glow)
- Helpers: `scroll-reveal`, `page-transition`, `scroll-to-top-button`,
  `use-scroll-position` hook
- Fully responsive, dark/light mode via `next-themes`.

> Note: this repository was originally scaffolded by [v0.app](https://v0.app)
> (project "my-v0-project").

## Features

- Next.js 15 App Router with React 19
- shadcn/ui component library (Radix UI primitives, CVA variants)
- Dark/light theme toggle with system preference support
- Animated section reveals and page transitions
- Custom mouse-glow cursor effect
- Tailwind CSS 3.4 + animations
- Zod + React Hook Form for forms, Recharts for charts
- Skeleton-free: ESLint/TS build errors set to not fail builds

## Tech stack

| Layer      | Technology                                   |
| ---------- | -------------------------------------------- |
| Framework  | Next.js 15.2.8 (App Router, React 19)        |
| Styling    | Tailwind CSS 3.4, tailwindcss-animate        |
| Components | shadcn/ui + Radix UI                         |
| Theming    | next-themes                                  |
| Forms      | React Hook Form, Zod, @hookform/resolvers    |
| Charts     | Recharts 2.15                                |
| Icons      | Lucide React                                 |
| Language   | TypeScript 5                                 |

## Quick start

Requirements: Node.js 18+ and pnpm (or npm).

```bash
pnpm install        # or: npm install --legacy-peer-deps
pnpm dev            # or: npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

```bash
pnpm build          # static export to out/
pnpm start
```

## Project structure

```
app/
├── page.tsx            # Landing page (all sections)
├── ui-library/page.tsx # Component library showcase
├── layout.tsx          # Root layout + theme provider
└── globals.css         # Global styles
components/
├── sections/           # hero, features, testimonials, pricing, blog, faq, cta
├── ui/                 # shadcn/ui components
├── ui-library/         # Reusable effects & blocks (mouse-glow, …)
├── site-header.tsx     # Navbar
├── site-footer.tsx     # Footer
├── mode-toggle.tsx     # Dark/light toggle
├── scroll-reveal.tsx   # Scroll animation wrapper
└── page-transition.tsx  # Page transition wrapper
hooks/
└── use-scroll-position.tsx
lib/utils.ts            # cn() helper
public/                 # Static assets
next.config.mjs         # Next config (static export + basePath for GitHub Pages)
tailwind.config.ts      # Tailwind theme
components.json         # shadcn/ui config
```

## Environment variables

None required — fully client-side, no backend or API keys.

## Deployment

- **GitHub Pages (this repo):** statically exported (`output: 'export'`) with
  `basePath: '/next-js-boilerplate'` for the project subpath.
  Live at https://girishlade111.github.io/next-js-boilerplate/
  > For domain-root deploys (e.g. Vercel), **remove `basePath`** from
  > `next.config.mjs`.
- **Vercel:** import the repo and deploy as-is.
- Build output goes to `out/` (git-ignored).

## License

Free to use. Built by Girish Lade — https://ladestack.in

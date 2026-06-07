# 🏕️ Scouts BSA Troop 251 — Eastvale, CA

  A modern, fully responsive public website for **Scouts BSA Troop 251** in Eastvale, California. Built with React, Vite, and Tailwind CSS — featuring dark/light mode, animated sections, an interactive calendar, and complete SEO support.

  ---

  ## ✨ Features

  - **9 full pages** — Home, About, Join, Calendar, Gallery, Eagle Scouts, Leadership, Resources, Contact
  - **Dark & Light mode** with system-preference detection
  - **Animated stat counters** on the homepage (rAF + IntersectionObserver)
  - **Framer Motion** scroll animations throughout
  - **Interactive monthly calendar** with color-coded event types
  - **Masonry gallery** with category filter tabs
  - **Eagle Scout honor roll** with a zigzag timeline layout
  - **Contact form** with meeting info, Google Maps embed, and social links
  - **Back-to-top button** with smooth scroll
  - **Full SEO suite** — per-page `<title>`, description, Open Graph, Twitter cards, JSON-LD structured data, `sitemap.xml`, `robots.txt`
  - **100% TypeScript** — zero type errors

  ---

  ## 🖥️ Tech Stack

  | Layer | Technology |
  |---|---|
  | Framework | [React 18](https://react.dev) + [Vite](https://vitejs.dev) |
  | Language | TypeScript |
  | Styling | [Tailwind CSS v4](https://tailwindcss.com) |
  | Animations | [Framer Motion](https://www.framer.com/motion/) |
  | Routing | [Wouter](https://github.com/molefrog/wouter) |
  | UI Components | [shadcn/ui](https://ui.shadcn.com) + [Radix UI](https://www.radix-ui.com) |
  | Icons | [Lucide React](https://lucide.dev) |
  | Dark Mode | [next-themes](https://github.com/pacocoursey/next-themes) |
  | SEO | [react-helmet-async](https://github.com/staylor/react-helmet-async) |

  ---

  ## 🚀 Getting Started

  ### Prerequisites

  - [Node.js](https://nodejs.org/) v18+
  - [pnpm](https://pnpm.io/) v9+

  ### Installation

  ```bash
  # Clone the repository
  git clone https://github.com/ayyappanadithiyakrishna-oss/troop-251b-website.git
  cd troop-251b-website

  # Install dependencies
  pnpm install
  ```

  ### Development

  ```bash
  # Start the dev server
  PORT=5173 BASE_PATH=/ pnpm --filter @workspace/troop-251 run dev
  ```

  Open [http://localhost:5173](http://localhost:5173) in your browser.

  ### Build for Production

  ```bash
  PORT=5173 BASE_PATH=/ pnpm --filter @workspace/troop-251 run build
  ```

  Output is written to `artifacts/troop-251/dist/public/`.

  ### Type Check

  ```bash
  pnpm --filter @workspace/troop-251 run typecheck
  ```

  ---

  ## 📁 Project Structure

  ```
  artifacts/troop-251/
  ├── public/
  │   ├── favicon.svg
  │   ├── opengraph.jpg        # Social share image (replace with real photo)
  │   ├── robots.txt
  │   └── sitemap.xml
  ├── src/
  │   ├── components/
  │   │   ├── layout/
  │   │   │   ├── Navbar.tsx   # Sticky nav with mobile menu + dark mode toggle
  │   │   │   └── Footer.tsx
  │   │   ├── ui/              # shadcn/ui primitives
  │   │   ├── BackToTop.tsx
  │   │   └── SEO.tsx          # Per-page meta + JSON-LD injection
  │   ├── pages/
  │   │   ├── home.tsx         # Hero, animated stats, events preview, Eagle teaser
  │   │   ├── about.tsx        # Mission, patrol method, charter org
  │   │   ├── join.tsx         # Steps to join, meeting info, FAQ, contact form
  │   │   ├── calendar.tsx     # Monthly grid calendar + upcoming event list
  │   │   ├── gallery.tsx      # Masonry photo gallery with category filters
  │   │   ├── eagle-scouts.tsx # Eagle Scout honor roll (timeline layout)
  │   │   ├── leadership.tsx   # Youth PLC + adult volunteer roster
  │   │   ├── resources.tsx    # Downloadable forms + external links
  │   │   ├── contact.tsx      # Contact form, map, social links
  │   │   └── not-found.tsx    # Branded 404 page
  │   ├── App.tsx              # Router + providers
  │   ├── main.tsx
  │   └── index.css            # Theme tokens (navy / forest green / gold)
  ├── index.html
  ├── vite.config.ts
  ├── tsconfig.json
  └── package.json
  ```

  ---

  ## 📄 Pages

  | Route | Page | Description |
  |---|---|---|
  | `/` | Home | Hero, animated stats, upcoming events, Eagle highlight, leadership teaser, CTA |
  | `/about` | About | Troop history, mission, patrol method, why families choose us |
  | `/join` | Join | 4-step process, meeting info, FAQ accordion, interest form |
  | `/calendar` | Calendar | Monthly grid view + upcoming events list (color-coded by type) |
  | `/gallery` | Gallery | Masonry photo grid with All / Camping / Hiking / Service / Summer Camp filters |
  | `/eagle-scouts` | Eagle Scouts | Honor roll with scout names, years, and project descriptions |
  | `/leadership` | Leadership | Youth Patrol Leaders Council + adult volunteer cards |
  | `/resources` | Resources | Packing lists, BSA forms, advancement links |
  | `/contact` | Contact | Message form, meeting address, Google Maps, social media links |

  ---

  ## 🎨 Theme & Colors

  The color palette is defined in `src/index.css` using CSS custom properties:

  | Token | Color | Usage |
  |---|---|---|
  | `--primary` | Navy `#0a1628` | Navbar, buttons, headings |
  | `--secondary` | Forest Green `#1a4731` | Accents, Eagle Scout highlights |
  | `--accent` | Warm Gold `#c9980a` | Stat numbers, badges |

  Both **light** and **dark** variants are fully defined and switch via the `dark` class on `<html>`.

  ---

  ## ✏️ Customizing Content

  All placeholder content is marked with `// TODO:` comments in the source files. Here's a quick reference:

  | What to update | File |
  |---|---|
  | Eagle Scout honor roll | `src/pages/eagle-scouts.tsx` → `EAGLES` array |
  | Youth & adult leadership names | `src/pages/leadership.tsx` → `YOUTH_LEADERS` / `ADULT_LEADERS` |
  | Upcoming events | `src/pages/calendar.tsx` → `EVENTS` array |
  | Resource file links | `src/pages/resources.tsx` → `RESOURCES` array |
  | Social media URLs | `src/pages/contact.tsx` → social `<a>` href values |
  | Meeting address / phone | `src/pages/contact.tsx` and `src/pages/join.tsx` |
  | Photos | Replace all `picsum.photos` `src` URLs with real troop photos |
  | OG share image | Replace `public/opengraph.jpg` with a real 1200×630 troop photo |
  | Favicon | Replace `public/favicon.svg` with your troop logo |

  ---

  ## 🔍 SEO

  Every page includes:

  - Unique `<title>` and `<meta name="description">`
  - Correct `<link rel="canonical">` per route
  - Open Graph (`og:title`, `og:description`, `og:image`, `og:url`)
  - Twitter card meta tags
  - Page-specific **JSON-LD** structured data (Organization, EventSeries, ContactPage, etc.)
  - `public/sitemap.xml` listing all 9 routes
  - `public/robots.txt` with `Sitemap:` declaration

  Update the domain from `https://troop251.com` to your real domain in `src/components/SEO.tsx` (the `url` default) and in `public/sitemap.xml` / `public/robots.txt`.

  ---

  ## 🚢 Deployment

  The site is a standard static Vite build. It can be deployed to any static host:

  - **Netlify** — drag and drop the `dist/public` folder, or connect the repo
  - **Vercel** — set build command to `pnpm build` and output directory to `dist/public`
  - **GitHub Pages** — use the `gh-pages` action with `dist/public` as the publish directory
  - **Firebase Hosting** — point `public` to `dist/public` in `firebase.json`

  ---

  ## 📜 License

  This project is released under the [MIT License](LICENSE). Feel free to fork it for your own troop's website.

  ---

  ## 🙏 Acknowledgments

  - [Scouts BSA](https://www.scouting.org/) for the program that inspired this site
  - [shadcn/ui](https://ui.shadcn.com) for the accessible component library
  - [Framer Motion](https://www.framer.com/motion/) for the animation primitives
  - Built with ❤️ for the scouts and families of Troop 251, Eastvale, CA
  
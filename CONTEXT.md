# Project Context — Atlantic AI Hackathon Participant Waitlist Page

> This file provides full context for any new session working on this project.
> Always read this file at the start of a new or compacted session.

## Project Overview
- **What:** Participant waitlist landing page for "The Atlantic AI Hackathon" in Halifax, NS (2026)
- **Who:** Organized by Jitakshi (Event Lead & Tech Partnerships) and Bethany Wilkie (Business Strategy)
- **Purpose:** Excite non-technical SMB owners about the event and capture their email for the waitlist. Tone is energetic, inclusive, empowering — "the invite to the party everyone will be talking about."
- **Target audience:** Small and medium business owners, operations managers, marketing leads, team members — NON-TECHNICAL people who may feel intimidated by tech
- **Previous event:** Lovable Halifax Women's AI Hackathon, Dec 2025 — 70 participants, 5 sponsors, 7 winners, 3 judges, 100% sold out, participants built working prototypes in 2 hours with zero coding experience
- **New event targets:** 100-150 participants, 10-15 sponsors, full day (9am-6pm), premier Halifax venue, documentary coverage

## Related Project — Sponsor Page (SEPARATE REPO)
- The sponsor landing page lives in a separate repo: https://github.com/JitakshiS/sme-halifax-hackathon.git
- Deployed at: https://sme-halifax-hackathon.vercel.app/
- That page targets potential sponsors (Google, Shopify, Apple, etc.) — it's a "good to read and watch" evidence piece
- The sponsor page uses lemon-green accent (#CBEF43), this page uses coral/warm orange (#F97316)
- Both pages cross-link to each other in their footers

## Tech Stack
- Single self-contained HTML file (`index.html`) — no build tools, no frameworks
- Pure CSS + vanilla JS (no Tailwind)
- Google Fonts: Jost (geometric sans, Futura-like) + JetBrains Mono (monospace labels)
- Colors: near-black (#09090B), off-white (#FAFAF9), **coral/warm orange accent (#F97316)**
- Deployed via GitHub Pages from: https://github.com/JitakshiS/sme-halifax-hackathon-participants.git
- Every `git push` to main auto-deploys via GitHub Actions workflow
- Waitlist form backend: Formspree (email notification)

## Design Preferences (User-confirmed)
- Same base design as sponsor page: dark theme, Jost + JetBrains Mono fonts
- Different accent color: Coral/warm orange (#F97316) to distinguish from sponsor page
- Style: Minimal, modern, 2026-level design — NOT basic or corporate
- Must feel energetic, inclusive, empowering — NOT intimidating for non-tech people
- Mobile-first: most SMB owners will see this on their phones first
- All text must be readable — no tiny gray-on-dark-gray text
- Photos should be high quality, not pixelated/blurry
- Key UX principle: answer "what is this?", "is it for me?", and "what do I get?" within 10 seconds

## Current Page Structure (index.html)
1. **Hero** (dark) — "Build a Real Tool for Your Business in One Day" + Save My Spot CTA + cursor-following spotlight
2. **01 — The Pitch** (light) — Hook copy about duct tape & spreadsheets + 4 pill badges (No Coding Required, Full Day, Free AI Credits, Real Outcomes)
3. **02 — How It Works** (dark) — 4-step timeline cards (Choose Track → Learn Tools → Build 6hrs → Demo & Win)
4. **03 — Build Tracks** (light) — 5 track cards (Automate, Customer Experience, Dashboards, Sell Smarter, Wildcard)
5. **04 — Who This Is For** (dark) — 4 persona cards (restaurant owner, contractor, retailer, agency owner)
6. **05 — What You Get** (light) — 6 benefit cards with icons (prototype, credits, mentors, networking, content, prizes)
7. **06 — From Our Last Event** (dark) — Stats (70 participants, 7 winners, 2hr prototypes, 100% sold out), 4 photos, callout quote, polaroid wall link
8. **07 — Event Details** (light) — 5-card grid (When, Where, Duration, Team Size, Cost)
9. **08 — Waitlist Form** (dark) — Name, email, business name, role dropdown, challenge textarea → Formspree
10. **09 — FAQ** (dark) — 6 collapsible accordion items
11. **Footer** — Links + "Interested in sponsoring?" link to sponsor page

## Key Files
- `index.html` — main page (~1400 lines, fully self-contained HTML/CSS/JS)
- `images/wl-networking.jpeg` — Women networking at high-rise with skyline
- `images/wl-volta.jpeg` — Two women at Volta venue sign
- `images/wl-winner.jpeg` — Winner holding Shopify prize certificate
- `images/wl-judges.jpeg` — Awards ceremony with judges and winners
- `.github/workflows/deploy.yml` — GitHub Pages deployment via Actions
- `.gitignore` — excludes .DS_Store

## Form Setup
- Form action is currently set to: `https://formspree.io/f/PLACEHOLDER`
- **NEEDS:** User must create a Formspree account, create a form, and replace PLACEHOLDER with the real form ID
- On successful submit, the form hides and shows a "You're on the list!" confirmation message
- Form fields: Full Name (required), Email (required), Business Name (required), Role (dropdown), Challenge (textarea)

## Blueprint Reference
- The full strategy document lives in the sponsor repo: `Atlantic-AI-Hackathon-Complete-Blueprint.md`
- This waitlist page implements Part 4 of that blueprint
- Build tracks, personas, FAQ copy, and event format all come from the blueprint

## CSS Architecture
- CSS variables in `:root` for theming (accent overrides from sponsor page)
- Glass morphism: `var(--glass)` background + `var(--glass-border)` borders
- Scroll reveal animations: `.reveal` (fade up) + `.reveal-stagger` (staggered children)
- Counter animation on `[data-count]` elements via IntersectionObserver
- FAQ accordion: JS toggle on `.faq-item.open` with CSS `max-height` transition
- Responsive breakpoints: 900px (2-col), 768px (nav hides), 600px (single-col), 500px/480px (mobile)

## Session Log
- **Session 1 (current):** Built complete waitlist page from blueprint. User confirmed: same base design, coral accent (#F97316), Formspree for form, full page with all sections. Created separate repo, pushed, enabled GitHub Pages. Created this context file.

## Pending Items
- Replace Formspree PLACEHOLDER with real form ID
- User setting up separate Vercel deployment for this repo
- May need to update the sponsor page footer link once Vercel URL is known
- Potential future additions: countdown timer (once date is set), confetti on form submit, social sharing meta image

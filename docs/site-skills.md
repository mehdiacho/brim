# Skills used for the site revamp (2026-10-28)

The revamp of `index.html` used these skills from the set listed in
`X:\ai.tools\docs\capability-index.md` (row "Design/UI, motion ... skill packs").

## Used

| Skill | What it decided |
|---|---|
| `landing-page-design` | The page order: hero with one download action, a tagline section, benefits, coming soon, add-ons, FAQ, then the same download again at the bottom. The spacing scale (4, 8, 12, 16, 24, 32, 40, 48, 64, 80, 96 px), type sizes on Tailwind's steps, the grey gradient on the hero heading only, the floating nav with a blur, sections that rise in once with an IntersectionObserver, and the tagline whose words light up one by one. Sentence case everywhere. |
| `emil-design-eng` | Motion rules: transitions on `transform` and `opacity` only, one ease-out curve (`cubic-bezier(.22,1,.36,1)`), `scale(.97)` on press, hover effects only behind `(hover: hover) and (pointer: fine)`, no `transition: all`. Reduced motion keeps fades and drops movement. |
| `humanizer` | A pass over the copy: removed a repeated "gets out of the way", turned clipped fragments ("No account, no ads.") into a sentence, dropped a claim I couldn't back (that quitting puts everything back), and kept headings plain. No em dashes. |

Accessibility and performance came from the same two design skills plus WCAG basics: a skip link,
visible focus rings, `aria-pressed` on the demo's pause button, a pause control because the demo
moves for more than five seconds, the demo pausing itself when it's off screen or the tab is hidden,
real text for the tagline's screen-reader label, and contrast tokens for both themes.

## Skipped, and why

| Skill | Why not |
|---|---|
| `writing-guidelines`, `web-design-guidelines` | Both fetch their rules from GitHub at run time. That's a download, and downloads need Mehdi's OK, so I used `humanizer` and the rules above instead. Worth running before it goes live. |
| `landing-page-design`'s font rule (Geist, Manrope) and icon rule (Phosphor) | Brim itself draws in Segoe UI Variable with its own line icons, so the site keeps them. Using the app's own font is part of its identity, and it costs no download. |
| `landing-page-design`'s "no background gradients" | The mock screens behind the notch keep a soft wallpaper gradient. They stand in for a desktop, not a page background. |
| `taste-skill`, `hallmark`, `ui-ux-pro-max`, `interfaces:*` | They overlap with the two design skills above; loading all of them would have pulled the page in several directions. The revamp is an extension of the existing look, not a new style. |
| `animate`, `design-to-motion`, `apple-design` | The demo already has its own spring-like motion from Brim's real sizes; I kept it and only added pause and reduced-motion handling. |
| `web-perf` | No build step and no framework: one HTML file, no new requests except the existing GitHub release lookup. Nothing to profile yet. |

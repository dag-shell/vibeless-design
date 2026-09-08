---
name: vibeless-design
description: Use when building, styling, or reviewing a website or UI component and the goal is a clean, premium, intentional look rather than a "vibe coded" one. Triggers on requests like "make this look less AI-generated", "make it feel premium/polished", "review my site's design", "why does this look cheap", or any landing page / hero section / component build where visual quality matters. Also use proactively before shipping any generated UI — check it against references/checklist.md.
---

# Vibeless

Ship UI that reads as intentional, not generated. This skill encodes the recurring
tells of "vibe coded" design (rushed, AI-default, no system behind it) and the
concrete fixes for each one.

## Core principle

Every "vibe coded" tell traces back to the same root cause: a missing system.
Random spacing, random radiuses, random fonts, random animation — none of it is
wrong in isolation, it's wrong because nothing else on the page agrees with it.
Fixing this skill is not about banning purple or sparkles specifically; it's
about picking a small number of systemic decisions up front and applying them
without exception.

## 30 Reasons Your Site Looks Vibe-Coded (Rules & Checklist for AI)

As an AI generating or reviewing UI, you must strictly avoid these 30 recurring vibe-coded anti-patterns. Treat every item below as an actionable rule and audit checklist—any checked item is a violation that must be resolved:

### Visual & Styling
- [ ] **1. Harsh gradients** — **AI Rule:** Never use harsh, multi-stop, or high-contrast decorative gradients. Use subtle monochromatic tints or flat surfaces with calibrated contrast.
- [ ] **2. Lucide icons spam** — **AI Rule:** Do not scatter generic Lucide outline icons as decorative filler across every card and bullet. Use icons with clear purpose, scale them consistently, or omit them.
- [ ] **3. Pure white background** — **AI Rule:** Avoid stark `#FFFFFF` canvas paired with arbitrary gray borders. Use intentional, calibrated background and surface color tokens.
- [ ] **4. Rainbow coloring** — **AI Rule:** Never assign random multi-colored badges, cards, or borders. Enforce a disciplined palette with at most 1–2 brand-derived accent colors.
- [ ] **5. Drop shadows** — **AI Rule:** Ban muddy, heavy, default CSS drop shadows. Use subtle, multi-layered diffuse elevation or clean 1px borders (`border-border`).
- [ ] **6. Soft corner radius mismatch** — **AI Rule:** Standardize on a single, intentional border-radius scale (e.g., 4px, 6px, or 8px). Never mix arbitrary pill shapes with rounded rectangles.
- [ ] **7. Purple and black cliché** — **AI Rule:** Do not default to the generic AI/SaaS dark-mode purple-and-black glow palette unless explicitly requested by brand guidelines.
- [ ] **8. Radial orbs** — **AI Rule:** Ban decorative glowing radial blur orbs (`radial-gradient` circles) floating aimlessly in background corners.
- [ ] **9. Dot grids** — **AI Rule:** Avoid cliché SVG dot matrix or blueprint graph-paper backgrounds used as landing page filler.
- [ ] **10. Sparkle icons** — **AI Rule:** Never use sparkle or magic wand icons (✨) to signal AI, "smart" features, or quality.
- [ ] **11. Liquid glass (Glassmorphism)** — **AI Rule:** Avoid blurry glassmorphism and frosted backdrop filters that compromise readability. Use solid, readable background surfaces.
- [ ] **12. Neon colors** — **AI Rule:** Avoid eye-straining neon glows and cyber accents. Maintain strict WCAG contrast with grounded color palettes.
- [ ] **13. Basic pastel colors** — **AI Rule:** Avoid washed-out, generic pastel pill badges and cards that lack contrast and visual hierarchy.

### Content & Typography
- [ ] **14. Inter / Geist / Space Grotesk defaults** — **AI Rule:** Do not default mindlessly to Inter, Geist, or Space Grotesk without brand rationale. Establish an intentional type ramp with consistent sizing and line-heights.
- [ ] **15. Emojis as UI elements** — **AI Rule:** Never use emojis in headings, feature titles, button labels, or bullet points.
- [ ] **16. Em dashes** — **AI Rule:** Stop writing AI-telltale copy littered with em dashes (—). Write crisp, human, direct sentences.
- [ ] **17. "It's not X, it's Y" copy** — **AI Rule:** Ban cliché antithetical marketing tropes ("It’s not just a tool, it’s a superpower"). State plainly what the product does and why it matters.
- [ ] **18. Checkmark bullets** — **AI Rule:** Eliminate generic green checkmark icon lists. Structure feature benefits with descriptive headings and specs.
- [ ] **19. Fake testimonials** — **AI Rule:** Never generate placeholder testimonials with fake titles ("Sarah P., Growth Lead") or AI stock avatars. Either display authentic, verifiable proof or omit testimonials entirely.

### Layout & Composition
- [ ] **20. 3 feature cards in a row** — **AI Rule:** Break out of the clichéd 3-equal-card grid template. Structure layouts based on the actual hierarchy and content needs of the product.
- [ ] **21. Bento grids** — **AI Rule:** Do not force unrelated features into an arbitrary bento-box puzzle grid just because it's trendy. Use layouts that serve comprehension.
- [ ] **22. Terminal window** — **AI Rule:** Never slap a faux macOS terminal window with traffic-light buttons on a landing page unless the product is strictly a developer CLI.
- [ ] **23. Colored left stripe** — **AI Rule:** Avoid the dated 3px/4px colored left border on cards, callouts, or quote blocks.
- [ ] **24. 3 pricing tiers** — **AI Rule:** Do not generate arbitrary 3-tier pricing tables with a highlighted "Most Popular" card unless reflecting an actual business model.

### Interaction & Polish
- [ ] **25. Hover animations** — **AI Rule:** Remove decorative hover lift, scale, tilt, or bounce on static content cards. Transitions must only indicate functional interactive states.
- [ ] **26. Animated arrows** — **AI Rule:** Never use bouncing or animating SVG arrows nudging the user to click a CTA.
- [ ] **27. No skeleton loaders** — **AI Rule:** Mandatory loading states: every asynchronous data fetch, button submit, or page transition must have a skeleton loader or spinner.
- [ ] **28. No real product demos** — **AI Rule:** Always showcase actual, working product UI, live interactive components, or authentic screen captures—never abstract placeholder art.

### Trust & Legal Fundamentals
- [ ] **29. No TOS** — **AI Rule:** Always include accessible, legitimate Terms of Service links/pages.
- [ ] **30. No privacy policy** — **AI Rule:** Always include accessible, legitimate Privacy Policy links/pages.

## Before generating or reviewing any UI, lock these decisions

1. **Spacing scale** — pick 4pt or 8pt, use only multiples of it for margin,
   padding, gap. Never an arbitrary pixel value.
2. **Type system** — one heading font, one body font, a fixed type ramp
   (sizes + line-heights). No ad hoc font-weight or size choices mid-build.
3. **Color palette** — small and disciplined. No gradient, glow, or neon
   accent unless it's part of an actual brand identity. High contrast is
   mandatory, not optional.
4. **Component language** — one border-radius value, one shadow/elevation
   style, one padding logic, reused across every button/card/input/modal.
5. **Motion policy** — animations only on state change a user needs to
   notice (loading, success, error, focus). No hover lift/rotate/bounce for
   decoration. Easing and timing should feel physical, not overshot.

If any of these five aren't decided yet, decide them before writing markup —
don't let them emerge accidentally component by component.

## While building

- Every async action (button click, data fetch, page nav) gets a loading
  state — spinner-in-button, skeleton, or progress indicator. Never a silent
  gap.
- Every interactive element must actually work: tabs switch, accordions
  open/close, carousels slide, modals close, dark-mode toggles toggle, social
  icons link to real URLs (or get removed). A non-functional element is worse
  than no element.
- Test responsiveness before polishing desktop further. Broken mobile layout
  is a bigger tell than any visual choice.
- Fill in real technical fundamentals: page title (not "Home"), meta
  description, OG image, favicon. These are cheap and their absence is loud.
- Write copy that names the actual thing the product does. Ban filler like
  "build your dreams" / "launch faster" / "where ideas become reality" — say
  what it is and why it matters instead. If you're tempted to add a
  testimonial, make it specific and attributable, or skip it — a generic
  "Sarah P., Helped me so much" with a stock avatar is a bigger red flag than
  having no testimonials at all.

## Before shipping

Run the build against `references/checklist.md`. If 5+ items are checked,
it reads as vibe coded — revise before presenting it as done. Don't just
scan the list mentally; go section by section (visual, structural, copy,
technical) since the categories catch different things.

## Tone

Be direct about tells when reviewing someone's site — vague praise doesn't
help them ship something better. Point at the specific element and the
specific fix ("that hover-lift on every card is fighting your grid — drop it
to a 1px border-color change on hover instead"), not just "this looks vibe
coded."
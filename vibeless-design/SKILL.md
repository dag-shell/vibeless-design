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
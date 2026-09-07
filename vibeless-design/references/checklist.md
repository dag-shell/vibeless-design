# Vibe-Coded Red Flag Checklist

Check the build against every section. 5+ checked items across the whole
list means it reads as vibe coded — revise before shipping.

## Visual

- [ ] Purple gradient / neon-purple glow used without brand justification
- [ ] Sparkle icon or emoji used more than once as a design accent
- [ ] Hover animation that lifts, rotates, or bounces a card/button
- [ ] Emoji used as a UI element (in headings, buttons, bullets, footer)
- [ ] Testimonial with a generic name, no title, no link, or an
      AI-generated-looking avatar
- [ ] Social icon that links to "#", a bare domain, or a 404
- [ ] Icon dramatically oversized relative to its accompanying text
- [ ] Font is fine (Inter/Poppins/Montserrat/etc.) but weights, sizes, and
      line-heights are inconsistent across the page
- [ ] Semi-transparent / blurred header with low-contrast text over
      scrolling content
- [ ] Any animation with no easing, mistimed trigger, or visible stutter

## Structural

- [ ] Any async action with no loading state (button, page, data fetch)
- [ ] Component sizing/padding/alignment shifts between pages
- [ ] Noticeably slow or laggy interactions
- [ ] Misaligned grid, uneven spacing, or drifting sticky elements
- [ ] More than one or two distinct border-radius values in use

## Copy

- [ ] Copyright line has a typo or leftover placeholder ("All right
      reversed", "YourSiteName", "Made by Me")
- [ ] Tagline is generic filler ("Build your dreams", "Launch faster",
      "The future of X")
- [ ] Hero section stacks too many elements at once (sparkle + emoji +
      gradient + two buttons + animated card + Lottie + microcopy)

## Technical

- [ ] Missing OG image, generic/blank page title, or no meta description
- [ ] Text overflow, weird stacking, or oversized buttons on mobile
- [ ] Any interactive element that doesn't actually work (dead carousel,
      inert tabs, accordion that won't open, modal that won't close, no-op
      dark mode toggle)

## The fix, in priority order

1. Establish a 4pt or 8pt spacing system and apply it everywhere.
2. Pick one heading font + one body font, define a type ramp, stop
   improvising sizes.
3. Standardize on one border-radius and one shadow style.
4. Remove decorative animation; keep only state-change motion.
5. Fix responsiveness before further desktop polish.
6. Add loading states to every async action.
7. Rewrite copy down to one clear, specific promise.
8. Click every button, link, and icon — fix or remove anything dead.
# ÉLAN Living — Motion & UI update (v1.1)

## Fixed

- Removed the Hero's **endless CSS zoom loop** (`hero-zoom`) that could cause jitter, especially on mobile.
- Hero now renders a real image (`object-fit: cover`) with `fetchPriority="high"`, a preload hint, and a short GSAP entrance (once, not a repeating animation).
- GSAP page animations are isolated within `gsap.context()`, and cleaned up on navigation. The previous global `ScrollTrigger.getAll().forEach(kill)` approach is removed.
- Support for `prefers-reduced-motion`, including disabling scrolling animations for visitors who request reduced motion.

## UI/UX improvements

- Completely custom language dropdown: native language names, compact two-letter badges, selection checkmark, subtle open animation, soft rounded borders/shadows.
- Five languages: Vietnamese, English, Russian, Korean, Chinese. Changing language uses client-side navigation rather than a page reload and retains the current URL path.
- Language popover closes when clicking outside, pressing Escape, or navigating. Arrow Up/Down and Home/End work between options.
- More polish: staggered property card reveals, image reveal in editorial section, section fade-in, top scroll progress bar, refined navigation underlines and hover interactions.

## Run locally

```bash
npm install
npm run dev
```

Open http://localhost:5173/vi

## Notes

This remains a **frontend demo**. Property content and leads are saved to localStorage. The admin login (`demo123`) is only illustrative — do **not** deploy it as real authentication. Sample images load from Unsplash and need internet access.

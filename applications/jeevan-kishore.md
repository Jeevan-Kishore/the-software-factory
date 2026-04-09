# Jeevan Kishore

## Why this role

As a Lead Engineer who has spearheaded frontend architectures for startups and managed cross-functional deliveries for platforms serving 10M+ users, the "own everything" philosophy is exactly how I operate. I thrive in environments where engineering excellence is coupled with product ownership, from conceptualizing market-ready solutions to optimizing cloud infrastructure for 30% cost reductions.

## Proof of work

- **Personal Portfolio:** [jeevan.vercel.app](https://jeevan.vercel.app)
- **AI-First Application Architecture:** Designed a tech stack for a consumer-facing AI astrology platform using Claude Code, Aider, LiteLLM, and Ollama.
- **Market Data Visualization Extension:** Built a custom Chrome extension using Google Apps Script to visualize intraday Indian stock market data directly in Google Sheets.

## Resume

**Resume:** [jeevan-kishore.pdf](resumes/jeevan-kishore.pdf)
**LinkedIn:** [linkedin.com/in/jeevan-kishore](https://www.linkedin.com/in/jeevan-kishore) *(Inferred from typical naming, please verify)*

## One thing you'd change about this repo

The accessibility (a11y) standards of the terminal interface were previously suboptimal, and we have been systematically remediating them to achieve WCAG 2.1 Level AA compliance. Here is a detailed breakdown of the changes we've implemented:

1. **Color Contrast Optimization:** 
   - Remediated 10+ utility classes where contrast ratios were as low as 1.54:1 (e.g., `#333` on `#0d0d0d`).
   - Standardized secondary and muted text to `#7a7a7a` and `#7c7c7c` to ensure a minimum 4.5:1 ratio while preserving the terminal aesthetic.

2. **Semantic Structure & Landmarks:**
   - Swapped generic `<div>` wrappers for semantic HTML5 elements like `<main>` and `<header>`.
   - Added ARIA landmarks (`role="main"`, `role="banner"`, `role="log"`) to allow screen reader users to navigate the application by region.
   - Converted decorative text spans into proper heading levels (`<h1>`, `role="heading"`) for better document hierarchy.

3. **Interactive Element Compliance:**
   - Replaced non-semantic `<a>` tags (used as buttons) with proper `<button>` elements, ensuring they are keyboard-focusable and correctly identified by assistive technology.
   - Added programmatic associations between form labels and inputs using the `for` attribute (e.g., visitor capture form).
   - Added `aria-label` to the terminal input and search fields, as placeholders alone are insufficient for accessibility.

4. **Focus Management & Navigation:**
   - Implemented a **Skip to Content** link as the first focusable element to allow keyboard users to bypass the terminal title bar.
   - Configured the visitor modal with `role="dialog"` and `aria-modal="true"`, including focus trapping to ensure keyboard navigation remains within the active overlay.

5. **Assisted Technology Refinements:**
   - Marked all decorative Unicode characters (box-drawing chars `│`, `┌─`, scanlines, and title bar dots) with `aria-hidden="true"` to reduce screen reader noise.
   - Added descriptive `<meta name="description">` tags for better SEO and screen reader context.

These changes ensure that the "Software Factory" is not just visually stunning but also inclusive and usable for developers across all ability levels.

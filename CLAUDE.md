# CLAUDE.md - AI Assistant Guide for Reign Globe Website

## Project Overview

**Project:** Reign Globe Automations Landing Page
**Type:** Static HTML/CSS/JavaScript Single-Page Application
**Purpose:** Professional marketing landing page for an AI automation agency

This is a zero-dependency, single-file static website optimized for performance, SEO, and accessibility.

## Quick Start

```bash
# Open directly in browser
open index.html

# Or use a local server
python -m http.server 8000
npx http-server -p 8000
```

No build process, package managers, or dependencies required.

## Project Structure

```
/reignglobe-website/
├── index.html                     # Main landing page (all HTML/CSS/JS)
├── README.md                      # Project documentation
├── HEADER_STRUCTURE_REPORT.md     # SEO optimization report
├── SEO_KEYWORDS_MAP.txt           # Keyword strategy mapping
├── CLAUDE.md                      # This file
└── .gitignore                     # Git configuration
```

## Architecture

The entire application is contained in `index.html`:
- **Lines 1-11:** DOCTYPE, meta tags, font preconnects
- **Lines 11-1436:** Embedded CSS (`<style>` block)
- **Lines 1437-1901:** HTML markup
- **Lines 1902-2036:** JavaScript (`<script>` block)

## Technology Stack

- **HTML5** - Semantic markup with proper heading hierarchy
- **CSS3** - Flexbox, CSS Grid, custom properties, animations
- **Vanilla JavaScript** - No frameworks or libraries
- **Google Fonts** - Syne (headings), Manrope (body)

## Key Conventions

### CSS Organization

CSS follows this section order:
1. CSS Variables (`:root`)
2. Reset & Base Styles
3. Navigation
4. Hero Section
5. Problem Section
6. Solution Section
7. Services Section
8. How-It-Works Section
9. Proof/Case Studies Section
10. Pricing Section
11. FAQ Section
12. Final CTA Section
13. Footer
14. Responsive Design (`@media`)
15. Accessibility
16. Utility Classes
17. Motion Preferences

### CSS Variables (Design Tokens)

```css
--electric-blue: #00AEEF         /* Primary brand color */
--charcoal: #1A1A1A              /* Dark backgrounds */
--dark-gray: #2A2A2A             /* Alternate dark */
--light-gray: #F5F5F5            /* Light backgrounds */
--white: #FFFFFF                 /* Text & accents */
--blue-glow: rgba(0, 174, 239, 0.3) /* Glow effects */
```

### JavaScript Patterns

- **Scroll Effects** - Navbar state changes on scroll
- **Intersection Observer** - Scroll-triggered animations
- **Accordion Pattern** - Service and FAQ expandable items
- **Mobile Menu** - Hamburger toggle with class management
- **Smooth Scroll** - Native `scrollIntoView()` for navigation

## Section IDs (Navigation Targets)

```
#navbar         - Main navigation bar
#navLinks       - Navigation menu
#hamburger      - Mobile menu toggle
#problem        - Problem section
#solution       - Solution section
#services       - Services section
#how-it-works   - Implementation guide
#results        - Case studies section
#pricing        - Pricing plans
#faq            - FAQ section
#final-cta      - Final call-to-action
```

## Responsive Breakpoints

- **Mobile:** `max-width: 768px` - Single column, hamburger menu
- **Tablet:** `769px - 1439px` - Adjusted spacing
- **Desktop:** `1440px+` - Full multi-column layouts

## Accessibility Standards

This project follows **WCAG 2.1 Level AA**:

- Proper heading hierarchy (H1 → H2 → H3 → H4)
- Semantic HTML elements (`<section>`, `<nav>`, `<footer>`)
- ARIA labels on interactive elements
- Focus indicators (3px solid outline)
- Reduced motion support via `prefers-reduced-motion`

## Development Guidelines

### When Modifying CSS

1. Maintain the section organization order
2. Use existing CSS variables for colors/spacing
3. Follow BEM-like naming (e.g., `.pricing-card`, `.pricing-card.popular`)
4. Add responsive styles within existing `@media` queries

### When Modifying JavaScript

1. Use vanilla JS only - no frameworks
2. Maintain event delegation patterns for accordions
3. Use Intersection Observer for scroll animations
4. Keep animations hardware-accelerated (`transform`, `opacity`)

### When Adding Content

1. Follow existing heading hierarchy
2. Maintain semantic HTML structure
3. Add appropriate `id` attributes for navigation targets
4. Consider SEO keyword placement (see `SEO_KEYWORDS_MAP.txt`)

## Animation Keyframes

Available animations:
- `barGrow` - Logo bar entrance
- `gridPulse` - Hero background pulse
- `waveFloat` - Floating wave animation
- `vizPulse` - Logo visualization pulse
- `float` - General floating elements
- `nodePulse` - Network nodes pulsing
- `connectionFlow` - Connection line animation
- `waveSlide` - CTA wave background

## Testing Checklist

### Manual Testing

- [ ] Heading hierarchy in browser outline
- [ ] Screen reader compatibility
- [ ] Mobile responsiveness across viewports
- [ ] Keyboard navigation
- [ ] Color contrast validation

### SEO Validation

- [ ] Google Rich Results Test
- [ ] Lighthouse performance audit
- [ ] Heading structure analysis
- [ ] Keyword density check

## Common Tasks

### Adding a New Section

1. Create HTML section with unique `id`
2. Add corresponding CSS in appropriate section order
3. Update navigation links if needed
4. Add Intersection Observer entry for animations
5. Test responsive behavior at all breakpoints

### Modifying Color Scheme

1. Update CSS variables in `:root`
2. Check all hover states and glows
3. Verify color contrast for accessibility
4. Test reduced motion preferences

### Adding Interactive Elements

1. Use existing patterns (accordion, hover effects)
2. Maintain consistent transitions (0.3s ease)
3. Add appropriate focus states
4. Consider mobile touch interactions

## Performance Targets

- First Contentful Paint: < 1.5s
- Time to Interactive: < 3s
- Lighthouse Score: 95+
- Single HTTP request (no external deps)

## SEO Keywords Focus

Primary: AI automation agency, business automation services
Secondary: Enterprise automation, custom AI automation
Service-specific: AI chatbot, process automation, marketing automation

See `SEO_KEYWORDS_MAP.txt` for complete keyword strategy.

## Contact Information (Customizable)

- Email: hello@reignglobe.com
- Phone: +1 (555) 123-4567

## Deployment

Supported platforms:
- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Traditional web hosting (file upload)

Simply deploy the `index.html` file - no build step required.

## Git Workflow

- Main branch contains production code
- Feature branches for development
- Clean commits with descriptive messages

## Important Notes for AI Assistants

1. **Single-file architecture** - All code is in `index.html`
2. **No build process** - Changes are immediately reflected
3. **Vanilla only** - Do not introduce frameworks or bundlers
4. **Maintain structure** - Follow existing CSS/JS organization
5. **Preserve accessibility** - Always maintain WCAG compliance
6. **SEO awareness** - Consider keyword placement in changes
7. **Test responsively** - Verify all three breakpoints
8. **Use design tokens** - Reference CSS variables, not hard-coded values

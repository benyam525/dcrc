# Claude Code Prompt: DCRC Branding & Visual Language Update

## Objective

Update the DCRC website's visual identity to a refined earthy color palette that feels warm, grounded, professional, and culturally resonant.

---

## New Color Palette

Replace the current CSS `:root` variables with this palette:

```css
:root {
    /* Primary Colors */
    --color-dark: #181417;           /* Deep navy/black - text, headers, nav background */
    --color-teal: #142535;           /* Dark teal - accents, footer, depth */

    /* Warm Earth Tones */
    --color-brown-dark: #6E4436;     /* Rich brown - primary buttons, CTAs */
    --color-brown-medium: #96634E;   /* Medium brown - secondary accents, hover states */
    --color-taupe: #C8AEA4;          /* Warm taupe/beige - backgrounds, cards */

    /* Supporting Colors */
    --color-cream: #F5F0ED;          /* Light cream - page background */
    --color-white: #FFFFFF;          /* White - text on dark, cards */

    /* Legacy mappings (for compatibility) */
    --color-navy: #181417;
    --color-navy-light: #142535;
    --color-gold: #6E4436;
    --color-gold-light: #96634E;
}
```

---

## Color Application Guide

| Element | Old Color | New Color | Variable |
|---------|-----------|-----------|----------|
| Navigation background | Navy #0a1628 | Deep dark #181417 | `--color-dark` |
| Primary buttons | Gold #c9a227 | Rich brown #6E4436 | `--color-brown-dark` |
| Button hover states | Gold light #e8c547 | Medium brown #96634E | `--color-brown-medium` |
| Page background | Cream #faf8f5 | Light cream #F5F0ED | `--color-cream` |
| Section accents | Gold | Rich brown #6E4436 | `--color-brown-dark` |
| Footer background | Navy | Dark teal #142535 | `--color-teal` |
| Card backgrounds | White/Gray | Warm taupe #C8AEA4 | `--color-taupe` |
| Section labels | Gold | Rich brown #6E4436 | `--color-brown-dark` |
| Links | Gold | Rich brown #6E4436 | `--color-brown-dark` |
| Stat numbers | Gold | Rich brown #6E4436 | `--color-brown-dark` |

---

## Files to Update

1. **index.html** — Main site styles in `<style>` block
2. **team.html** — Team page styles
3. **history.html** — History page styles
4. **testimonials.html** — Testimonials page styles

---

## Specific CSS Updates

### Navigation
```css
nav {
    background: rgba(24, 20, 23, 0.95);  /* --color-dark with transparency */
}
```

### Buttons
```css
.btn-primary {
    background: var(--color-brown-dark);
    color: var(--color-white);
}

.btn-primary:hover {
    background: var(--color-brown-medium);
    box-shadow: 0 4px 20px rgba(110, 68, 54, 0.4);
}
```

### Section Labels & Accents
```css
.section-label {
    color: var(--color-brown-dark);
}

.hero-eyebrow {
    background: rgba(110, 68, 54, 0.15);
    border: 1px solid rgba(110, 68, 54, 0.3);
    color: var(--color-brown-dark);
}
```

### Stats & Highlights
```css
.stat-number {
    color: var(--color-brown-dark);
}
```

### Footer
```css
footer {
    background: var(--color-teal);
}
```

### Cards & Alternating Sections
```css
/* Light sections */
.section-light {
    background: var(--color-cream);
}

/* Accent sections */
.section-accent {
    background: var(--color-taupe);
}
```

---

## Design Philosophy

> "Refined earthy tones that are reminiscent of truth, durags, brown skin, and gold chains."

The palette should feel:
- **Warm** — Earth tones create approachability
- **Grounded** — Brown and taupe convey stability and trust
- **Professional** — Deep darks maintain sophistication
- **Culturally resonant** — Colors connect to the community DCRC serves

---

## Checklist

- [ ] Update `:root` CSS variables in all HTML files
- [ ] Replace all gold (#c9a227) references with rich brown (#6E4436)
- [ ] Update navigation background color
- [ ] Update button colors and hover states
- [ ] Update footer background to dark teal
- [ ] Update section labels and accent colors
- [ ] Update stat numbers and highlights
- [ ] Test contrast ratios for accessibility (especially text on taupe backgrounds)
- [ ] Verify hover states feel smooth and intentional
- [ ] Check mobile responsiveness with new colors

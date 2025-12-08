# 🎨 Shoonya Holistics - Style Guide & Customization

## Color Palette

### Primary Colors
```css
--primary-pink: #ff6b9d    /* Main brand color - Warm, inviting */
--secondary-pink: #ffa7c4  /* Accents and soft highlights */
--tertiary-pink: #ffb8d4   /* Light background tints */
```

### Secondary Colors
```css
--soft-purple: #9b7ebd     /* Secondary brand color */
--deep-purple: #6c5b7b     /* Dark accents and text */
```

### Accent Colors
```css
--soft-blue: #4d96ff       /* Cool tone complement */
--light-blue: #6cb4ff      /* Lighter blue variant */
--soft-green: #6bcf7f      /* Growth and wellness */
--warm-peach: #ff9b54      /* Warm accent color */
--light-peach: #ffc17a     /* Light variant */
```

### Neutral Colors
```css
--light-cream: #fff5f0     /* Soft background */
--cream: #faf6f3           /* Primary background */
--white: #ffffff           /* Pure white */
--dark-text: #3d3d3d       /* Main text color */
--light-gray: #f0e8e8      /* Borders and dividers */
```

---

## Typography

### Font Family
```css
font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
```

### Font Sizes
- **Display (Hero)**: 4rem (desktop), 2.5rem (tablet), 2rem (mobile)
- **Heading 1 (Section titles)**: 3rem (desktop), 2rem (mobile)
- **Heading 2**: 2.5rem
- **Heading 3**: 1.8rem
- **Body text**: 1rem
- **Small text**: 0.9rem
- **Tiny text**: 0.85rem

### Font Weights
- **Regular**: 400
- **Medium**: 500
- **Bold**: 700

---

## Spacing System

```css
/* Padding/Margin Scale */
4px, 8px, 12px, 15px, 20px, 25px, 30px, 40px, 50px, 60px, 80px, 100px
```

### Section Padding
```css
padding: 100px 20px;  /* Vertical-Horizontal */
```

### Container Width
```css
max-width: 1200px;
margin: 0 auto;
padding: 0 20px;
```

---

## Shadows

### Soft Shadow
```css
--soft-shadow: 0 10px 30px rgba(155, 126, 189, 0.15);
```

### Medium Shadow
```css
--medium-shadow: 0 15px 40px rgba(155, 126, 189, 0.2);
```

### Custom Shadows
```css
/* Hover effect */
box-shadow: 0 10px 30px rgba(255, 107, 157, 0.3);

/* Button hover */
box-shadow: 0 15px 40px rgba(255, 107, 157, 0.4);
```

---

## Border Radius

- **Buttons**: `50px` (fully rounded)
- **Cards**: `20px` (rounded corners)
- **Form inputs**: `8px` (subtle rounding)
- **Avatars**: `50%` (perfect circle)

---

## Animations

### Duration Scale
- **Quick**: `0.3s`
- **Standard**: `0.6s`
- **Slow**: `0.8s - 1.0s`
- **Looping**: `2s - 20s`

### Easing Functions
```css
ease-out           /* Bounce out effect */
ease-in-out        /* Smooth both ways */
cubic-bezier()     /* Custom curves */
linear             /* Constant speed */
```

### Common Animations

**Fade In Up**
```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(40px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
animation: fadeInUp 0.8s ease-out;
```

**Slide Down**
```css
@keyframes slideDown {
    from {
        transform: translateY(-100%);
        opacity: 0;
    }
    to {
        transform: translateY(0);
        opacity: 1;
    }
}
animation: slideDown 0.6s ease-out;
```

**Float**
```css
@keyframes float {
    0%, 100% { transform: translateY(0px); }
    50% { transform: translateY(-40px); }
}
animation: float 6s ease-in-out infinite;
```

**Bounce**
```css
@keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-15px); }
}
animation: bounce 2s ease-in-out infinite;
```

**Rotate**
```css
@keyframes rotateLogo {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
}
animation: rotateLogo 20s linear infinite;
```

---

## Component Styles

### Buttons

**Primary CTA Button**
```css
.cta-button {
    background: linear-gradient(135deg, var(--primary-pink), var(--soft-purple));
    color: white;
    border: none;
    padding: 16px 40px;
    font-size: 1.1rem;
    border-radius: 50px;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 10px 30px rgba(255, 107, 157, 0.3);
}

.cta-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 15px 40px rgba(255, 107, 157, 0.4);
}
```

### Service Cards

**Base Style**
```css
.service-card {
    background: white;
    padding: 40px;
    border-radius: 20px;
    box-shadow: var(--soft-shadow);
    transition: all 0.3s ease;
    border-left: 4px solid;
    position: relative;
    overflow: hidden;
}

.service-card:hover {
    transform: translateY(-10px);
    box-shadow: var(--medium-shadow);
}
```

**Color Variants**
```css
.service-card.astrological::before {
    background: linear-gradient(90deg, #ffa7c4, #c06c84);
}

.service-card.psychological::before {
    background: linear-gradient(90deg, #4d96ff, #6cb4ff);
}

.service-card.blended::before {
    background: linear-gradient(90deg, #ff9b54, #6bcf7f);
}
```

### Testimonial Cards

```css
.testimonial-card {
    background: white;
    padding: 30px;
    border-radius: 15px;
    box-shadow: var(--soft-shadow);
    border-left: 4px solid;
    transition: all 0.3s ease;
}

.testimonial-card:hover {
    transform: translateY(-8px);
    box-shadow: var(--medium-shadow);
}

.testimonial-card.astro-testimonial {
    border-left-color: #ffa7c4;
}

.testimonial-card.psych-testimonial {
    border-left-color: #4d96ff;
}

.testimonial-card.blended-testimonial {
    border-left-color: #ff9b54;
}
```

### Form Elements

**Input Styling**
```css
input, select, textarea {
    width: 100%;
    padding: 12px 15px;
    border: 2px solid var(--light-gray);
    border-radius: 8px;
    font-size: 1rem;
    transition: all 0.3s ease;
}

input:focus, select:focus, textarea:focus {
    outline: none;
    border-color: var(--primary-pink);
    box-shadow: 0 0 0 3px rgba(255, 107, 157, 0.1);
}
```

---

## Gradient Definitions

### Logo Gradients
```css
<linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="100%">
    <stop offset="0%" style="stop-color:#ff6b9d;stop-opacity:1" />
    <stop offset="50%" style="stop-color:#c06c84;stop-opacity:1" />
    <stop offset="100%" style="stop-color:#6c5b7b;stop-opacity:1" />
</linearGradient>
```

### Text Gradients
```css
background: linear-gradient(135deg, var(--primary-pink), var(--soft-purple));
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
```

---

## Responsive Breakpoints

```css
/* Desktop (Default) */
1200px+

/* Tablet */
@media (max-width: 768px) {
    /* Adjust layouts, hide certain elements */
}

/* Mobile */
@media (max-width: 600px) {
    /* Single column, smaller fonts */
}
```

### Common Adjustments
```css
/* Hero */
.hero-title {
    font-size: 2.5rem;    /* tablet */
    font-size: 2rem;      /* mobile */
}

/* Grid Layout */
.services-grid {
    grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));  /* desktop */
    grid-template-columns: 1fr;  /* mobile */
}

/* Navigation */
.nav-menu {
    display: flex;  /* desktop */
    display: none;  /* mobile - hidden by default */
}

.nav-menu.active {
    display: flex;  /* mobile - shown when toggled */
}
```

---

## How to Customize

### Change Primary Brand Color
1. Open `styles.css`
2. Find `:root` section
3. Update `--primary-pink` to your desired color
4. Update `--secondary-pink` for consistency
5. Save file - changes apply instantly

### Change Logo Colors
1. Open `index.html`
2. Find `<svg class="logo">`
3. Modify the color values in `<linearGradient>` elements
4. Save and refresh browser

### Modify Section Backgrounds
```css
.hero {
    background: linear-gradient(135deg, var(--cream) 0%, var(--light-cream) 100%);
    /* Change to: */
    background: linear-gradient(135deg, #your-color-1 0%, #your-color-2 100%);
}
```

### Adjust Animation Speed
```css
/* Slow down all animations */
@keyframes float {
    animation: float 10s ease-in-out infinite; /* was 6s */
}

/* Speed up logo rotation */
.logo {
    animation: rotateLogo 10s linear infinite; /* was 20s */
}
```

### Change Font
```css
body {
    font-family: 'Your Font Name', fallback, sans-serif;
}
```

### Modify Spacing
```css
.services {
    padding: 150px 20px;  /* was 100px */
}

.service-card {
    padding: 50px;  /* was 40px */
}
```

---

## Color Usage Guidelines

### Primary Pink (#ff6b9d)
- Main headlines
- Primary buttons
- Brand logo
- Active states
- Important accents

### Soft Purple (#9b7ebd)
- Secondary headings
- Subtle text
- Background accents
- Secondary buttons

### Soft Blue (#4d96ff)
- Links
- Icons
- Accents
- Focus states

### Soft Green (#6bcf7f)
- Success messages
- Growth indicators
- Positive actions
- Wellness accents

### Warm Peach (#ff9b54)
- Warm accents
- Alternative CTA
- Blended service branding
- Energetic elements

---

## Accessibility Tips

### Color Contrast
- Ensure text on backgrounds has sufficient contrast
- Test with contrast checker tools
- Minimum 4.5:1 for normal text
- Minimum 3:1 for large text

### Font Sizes
- Never go below 0.85rem for body text
- Maintain 1.5+ line-height for readability
- Use 1.8+ line-height for longer text

### Focus States
```css
*:focus {
    outline: 2px solid var(--primary-pink);
    outline-offset: 2px;
}
```

---

## Performance Optimization

### Reduce Motion
```css
@media (prefers-reduced-motion: reduce) {
    * {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
    }
}
```

### Optimize Images
- Use SVG for icons and logo (scalable)
- Use WebP for photos (when needed)
- Lazy load images with `loading="lazy"`

### CSS Best Practices
- Use CSS variables for easy maintenance
- Group related styles together
- Use shorthand properties
- Minimize specificity conflicts
- Avoid !important unless necessary

---

## Browser-Specific Styles

### Webkit (Chrome, Safari)
```css
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
```

### Firefox
```css
/* Slightly different box-shadow rendering */
filter: drop-shadow(0 5px 15px rgba());
```

### IE/Edge Legacy
- Gradients: Use -ms- prefix
- Some animations may not work perfectly
- Fallback colors recommended

---

## Testing Checklist

- [ ] All colors match brand palette
- [ ] Text contrast is sufficient (WCAG AA)
- [ ] Animations are smooth at 60fps
- [ ] Responsive layout works on all breakpoints
- [ ] Form validation works properly
- [ ] Links and buttons have hover states
- [ ] Mobile touch targets are 44px minimum
- [ ] Page loads in under 3 seconds
- [ ] No console errors
- [ ] Works in all major browsers

---

## Resources

### Color Tools
- Color Palette Generator: coolors.co
- Contrast Checker: webaim.org/resources/contrastchecker
- Gradient Generator: cssgradient.io

### Font Tools
- Google Fonts: fonts.google.com
- Typography Scale: typescale.com

### Animation Tools
- Easing Functions: easings.net
- Animation Inspector: Firefox DevTools

### Performance
- Lighthouse: Google Chrome DevTools
- WebPageTest: webpagetest.org

---

*This style guide ensures consistency and makes future customization easy!*

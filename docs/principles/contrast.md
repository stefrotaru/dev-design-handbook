# Contrast

**Core concept:** Make things extremely different to draw attention and guide user focus.

## What It Does

Contrast creates visual hierarchy and directs users' eyes to the most important elements. Without contrast, everything has equal weight and nothing stands out.

## Types of Contrast

### Color Contrast
High contrast between foreground and background improves readability and accessibility.

```css
/* High contrast - Good */
.text-on-dark {
  color: #ffffff;
  background: #1a1a1a;
}

/* Low contrast - Bad for readability */
.text-low-contrast {
  color: #cccccc;
  background: #dddddd;
}
```

### Size Contrast
Larger elements naturally draw more attention.

```css
/* Create hierarchy with size */
h1 { font-size: 3rem; }    /* Largest - most important */
h2 { font-size: 2rem; }    /* Second level */
p  { font-size: 1rem; }    /* Body - smallest */
```

### Weight Contrast
Font weight creates emphasis without changing size.

```css
h1 { font-weight: 700; }   /* Bold headlines */
p  { font-weight: 400; }   /* Regular body text */
.caption { font-weight: 300; } /* Light captions */
```

### Shape Contrast
Mixing geometric and organic shapes, or different geometric shapes, creates visual interest.

```css
.card { border-radius: 0.5rem; }  /* Rounded cards */
.button { border-radius: 2rem; }  /* Pill-shaped buttons */
.image { border-radius: 50%; }    /* Circular images */
```

## Color Contrast Guidelines

### WCAG Requirements
- **Normal text:** Minimum 4.5:1 contrast ratio
- **Large text:** Minimum 3:1 contrast ratio
- **UI components:** Minimum 3:1 against adjacent colors

### Practical Tips

For the best contrast, you’ll want to use high-contrasting colors for text on your site to
ensure readability, but high-contrasting colors can also have other design purposes.
High-contrasting colors—opposite each other on the color wheel, like green and
red—can be used to create a very intense focus area. But we don’t want to overwhelm
your website’s users, so contrast should be used to focus on bringing attention to the
most important parts of your website. Too much contrasting color can lead to a design
that is overwhelming and hard to scan, which is the opposite of what we want. 

### Primary CTAs
Use high contrast for primary call-to-action buttons:

```css
.cta-primary {
  background: #ff6b35;  /* Bright, attention-grabbing */
  color: #ffffff;       /* High contrast text */
  font-weight: 600;     /* Bold weight */
  font-size: 1.125rem;  /* Slightly larger */
}
```

## Size Contrast

### Don't Be Afraid of Large Typography
Small differences aren't enough. The larger the element, the more it will draw focus compared to the smaller items on the page.

```css
/* Not enough contrast */
h1 { font-size: 18px; }
p  { font-size: 16px; }

/* Strong contrast */
h1 { font-size: 48px; }
p  { font-size: 16px; }
```

### Whitespace Amplifies Size
Large type with generous whitespace creates maximum impact:

```css
.hero-title {
  font-size: 4rem;
  line-height: 1.1;
  margin-bottom: 2rem; /* Ample space */
}
```

## When to Use Contrast

### Create Focus
Guide users to the most important actions:
- Primary buttons vs. secondary buttons
- Headlines vs. body text
- Active navigation items vs. inactive

### Establish Hierarchy
```
Hero headline (largest, boldest)
  ↓
Section headings (large, bold)
  ↓
Subheadings (medium, semi-bold)
  ↓
Body text (regular size and weight)
  ↓
Captions (smallest, lightest)
```

### Signal Importance
- Error messages: red, bold
- Success messages: green, bold
- Warnings: orange, bold
- Info: blue, regular

## Don't Overdo It

Too much contrast is overwhelming:
- Not everything can be large and bold
- Limit bright colors to accents
- Reserve maximum contrast for most important elements

Think of contrast like exclamation marks — if everything is emphasized, nothing is!

## Practical Examples

### Button Hierarchy
```css
/* Primary - highest contrast */
.btn-primary {
  background: #007bff;
  color: white;
  font-weight: 600;
}

/* Secondary - medium contrast */
.btn-secondary {
  background: transparent;
  border: 2px solid #007bff;
  color: #007bff;
  font-weight: 500;
}

/* Tertiary - lowest contrast */
.btn-tertiary {
  background: transparent;
  color: #6c757d;
  font-weight: 400;
  text-decoration: underline;
}
```

### Text Hierarchy
```css
.article-title {
  font-size: 3rem;
  font-weight: 700;
  color: #1a1a1a;
}

.article-subtitle {
  font-size: 1.5rem;
  font-weight: 400;
  color: #666666;
}

.article-body {
  font-size: 1.125rem;
  font-weight: 400;
  color: #333333;
  line-height: 1.7;
}
```

## Testing Contrast

Use tools to verify your color contrast meets accessibility standards:
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
- Browser DevTools accessibility audit
- Color contrast browser extensions

## Key Takeaway

Contrast is the most effective way to bring visual interest to a web page and is
the easiest way to establish hierarchy. We want to draw our user’s attention
immediately, so contrast should be used boldly. It can be created via shape,
color, or size. 

If too many elements are sized the same, the page can become cluttered and
difficult to scan.

---

[← Previous: Repetition](./repetition) | [Back to Principles](./index) | [Next: Balance →](./balance)

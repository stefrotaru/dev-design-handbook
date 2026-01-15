# Repetition

**Core concept:** Reuse styles, elements, and patterns to create unity and consistency.

## What It Does

Repetition creates a cohesive visual experience. When users see repeated patterns, they learn to recognize and predict interface behavior, reducing cognitive load and building trust.

## Benefits

### For Users
- **Reduces cognitive load** — Familiar patterns are easy to process
- **Builds trust** — Consistency signals professionalism
- **Speeds up learning** — Users quickly understand how things work
- **Creates brand recognition** — Consistent style becomes memorable

### For Developers
- **More maintainable code** — Reusable components mean fewer places to update
- **Better performance** — Shared CSS rules are more efficient
- **Faster development** — Component libraries accelerate building
- **Fewer bugs** — One source of truth reduces inconsistencies

## What to Repeat

### Typography Styles
```css
/* Define once, use everywhere */
h1, .heading-1 { font-size: 2.5rem; font-weight: 700; }
h2, .heading-2 { font-size: 2rem; font-weight: 600; }
h3, .heading-3 { font-size: 1.5rem; font-weight: 600; }
body, .body-text { font-size: 1rem; line-height: 1.5; }
.caption { font-size: 0.875rem; color: #666; }
```

### Button Styles
```css
.btn {
  padding: 0.75rem 1.5rem;
  border-radius: 0.25rem;
  font-weight: 600;
  /* Base button styles */
}

.btn-primary { background: #007bff; color: white; }
.btn-secondary { background: #6c757d; color: white; }
.btn-danger { background: #dc3545; color: white; }
```

### Component Layouts
Repeat card layouts, form patterns, navigation structures, and other UI components throughout your application.

### Page Templates
Similar content types should use similar layouts (blog posts, product pages, etc.).

## Functional Consistency

This is critical: **Be consistent with function**.

### Good Example
```
All orange buttons = "Add to Cart"
All blue buttons = "Learn More"
All red buttons = "Delete"
```

### Bad Example
```
Orange button = "Add to Cart" on one page
Orange button = "Sign Up" on another page
Orange button = "Download" on a third page
```

When colors/styles have different meanings in different contexts, users get confused.

## Practical Implementation

### Design System Approach
```css
/* 1. Define design tokens */
:root {
  --color-primary: #007bff;
  --color-secondary: #6c757d;
  --spacing-sm: 0.5rem;
  --spacing-md: 1rem;
  --spacing-lg: 2rem;
  --border-radius: 0.25rem;
}

/* 2. Create reusable components */
.card {
  border: 1px solid #ddd;
  border-radius: var(--border-radius);
  padding: var(--spacing-lg);
  margin-bottom: var(--spacing-md);
}

/* 3. Use consistently throughout */
```

### Component-Based Architecture
```javascript
// React example
function PrimaryButton({ children, onClick }) {
  return (
    <button className="btn btn-primary" onClick={onClick}>
      {children}
    </button>
  );
}

// Use the same component everywhere
<PrimaryButton onClick={handleAdd}>Add to Cart</PrimaryButton>
<PrimaryButton onClick={handleSubmit}>Submit</PrimaryButton>
```

## Breaking Repetition Intentionally

Sometimes you *want* to break repetition to draw attention. This is okay when:
- You want to emphasize a special element
- You're creating visual hierarchy
- You're signaling a different section/context

But break patterns intentionally, not accidentally.

## Common Mistakes

### Inconsistent Spacing
```css
/* Bad: arbitrary spacing */
.section-1 { margin-bottom: 23px; }
.section-2 { margin-bottom: 18px; }
.section-3 { margin-bottom: 31px; }

/* Good: consistent spacing scale */
.section { margin-bottom: var(--spacing-lg); }
```

### Multiple Button Styles
Don't create a new button style for every page. Define a clear set and stick to it.

### Varying Component Behavior
If cards are clickable in one section, they should be clickable everywhere (or clearly different).

## Key Takeaway

Repetition establishes consistency and, on the web, can help orient users. Repetition of elements and styles creates a unified experience that can extend
beyond the website and tie a brand together.

Consistency builds trust. Define your patterns once, then repeat them religiously throughout your application.

---

[← Previous: Alignment](./alignment) | [Back to Principles](./index) | [Next: Contrast →](./contrast)

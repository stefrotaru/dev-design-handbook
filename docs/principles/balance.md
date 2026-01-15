# Balance

**Core concept:** Visual weight should feel evenly distributed across a design.

## What It Does

Balance creates stability and harmony. When a design is balanced, it feels intentional and complete. When unbalanced, it feels awkward or incomplete — like something is missing.

## Types of Balance

### Symmetrical Balance

Equal weight on both sides of a central axis. Creates a predictable, stable, formal feeling.

```
Columns width: 50% 50%
┌─────────────────────┐
│                     │
│  [Image]  [Text]    │
│                     │
│  [Text]   [Image]   │
│                     │
└─────────────────────┘
```

**Characteristics:**
- Traditional and formal
- Easy to achieve
- Predictable and safe
- Less dynamic

### Asymmetrical Balance
Unequal elements that still feel balanced. Creates a more dynamic, interesting, modern feeling.

```
Columns width: 50% 25% 25%
┌─────────────────────────────────────────────────┐
│                                                 │
│ [Large Image]    [Small image]    [Small text]  │
│                  [Link]           [Link]        │
│ [Text Block]     [Text Block]     [Small text]  │
│                                   [Link]        │
│                                   ...           │
└─────────────────────────────────────────────────┘
```

**Characteristics:**
- Modern and dynamic
- More visually interesting
- Harder to achieve
- Feels intentional when done well

Often with asymmetry, one larger element will be balanced by several smaller elements.

## Checking Your Balance

Ask yourself:
1. Does one side feel "heavier" than the other?
2. Does the design feel stable or awkward?
3. Is there a visual focal point?
4. Does whitespace balance the content?

## Responsive Considerations

Balance changes on different screen sizes:

```css
/* Desktop: Asymmetrical balance */
@media (min-width: 768px) {
  .layout {
    grid-template-columns: 2fr 1fr;
  }
}

/* Mobile: Stack for symmetrical balance */
@media (max-width: 767px) {
  .layout {
    grid-template-columns: 1fr;
  }
}
```

## Key Takeaway

Balance is the fundamental that measures the weight of visual elements and
helps make a piece feel complete or evenly weighted. Balance on the web can
be achieved through symmetrical or asymmetrical layouts. A well-balanced
design will draw the user’s eye throughout the layout; otherwise, a user may get
stuck on a focal point.

---

[← Previous: Contrast](./contrast) | [Back to Principles](./index)

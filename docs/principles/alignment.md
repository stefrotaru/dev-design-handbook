# Alignment

**Core concept:** Align elements along invisible lines to establish structure and order.

## What It Does

Alignment creates visual connections between elements that might not be near each other. It establishes an underlying structure that makes designs feel organized and intentional.

## Types of Alignment

### Edge Alignment
- **Top** — Elements align at their top edge
- **Bottom** — Elements align at their bottom edge
- **Left** — Elements align at their left edge (most common for text)
- **Right** — Elements align at their right edge

### Center Alignment
- **Horizontal** — Elements centered on a vertical axis
- **Vertical** — Elements centered on a horizontal axis

### Text Alignment
- **Left** — Most readable for body text (recommended)
- **Right** — Rarely used, special cases only
- **Center** — Headlines, short blocks only
- **Justified** — Avoid! Creates uneven gaps in text

## Best Practices

### Establish Strong Invisible Lines

We want our content on the web to be easily scannable and consumable. Establish a
strong line and use that to align elements on the page. This alignment will establish a
visible connection between pieces of content on the site and further help users understand the relationship between elements. 


### Don't Mix Alignment Within Components
```css
/* Bad: mixing alignment creates chaos */
.card {
  text-align: center;
}
.card h2 {
  text-align: left; /* Don't do this! */
}
```

```css
/* Good: consistent alignment */
.card {
  text-align: left;
}
.card h2 {
  text-align: left; /* Stays consistent */
}
```

### DO Mix Alignment Between Sections
Don’t be afraid to choose different alignments on your website, but look at those
decisions on a larger scale instead of mixing the alignment of different pieces of the
same smaller component. Mixing the alignment between sections can help distinguish sections on a website more effectively and keep the user engaged by creating a
more dynamic layout that moves their eye through the content. 

## Practical Examples

### Navigation Bar
```css
.nav {
  display: flex;
  align-items: center; /* Vertical alignment */
}

.nav-logo {
  margin-right: auto; /* Align left */
}

.nav-links {
  /* Align right */
}
```

### Card Grid
```css
.card-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  align-items: start; /* All cards align at top */
}

.card-content {
  text-align: left; /* All text left-aligned */
}
```

### Form Layout
```html
<form class="form-aligned">
  <div class="form-row">
    <label>Name</label>
    <input type="text">
  </div>
  <div class="form-row">
    <label>Email</label>
    <input type="email">
  </div>
</form>
```

```css
.form-row {
  display: flex;
  align-items: center; /* Label and input align vertically */
}

.form-row label {
  width: 100px;
  text-align: right; /* All labels align right */
  margin-right: 1rem;
}
```

## Common Mistakes

### Centered Body Text
Centered paragraphs are hard to read. Reserve center alignment for headlines and short text blocks only.

### Justified Text on Web
Justified text creates uneven spacing between words, especially on narrow screens. Stick with left alignment for readability.

### No Clear Alignment
When elements don't align to anything, designs feel chaotic and unprofessional.

## Key Takeaway

Alignment is the principle that establishes structure within a design. When
applied, it creates an invisible line between elements and brings a feeling of
order. It also makes connections between elements via that invisible line.

---

[← Previous: Proximity](./proximity) | [Back to Principles](./index) | [Next: Repetition →](./repetition)

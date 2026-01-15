# Proximity

**Core concept:** Items placed close together are perceived as related or grouped.

## What It Does

Proximity creates visual relationships between elements. When elements are near each other, users automatically assume they're connected. When elements are far apart, users see them as separate.

## How to Apply

- **Group related content together** — Form fields, related text, associated images
- **Use whitespace to separate unrelated groups** — Create clear visual boundaries
- **Create "chunks" of scannable content** — Break up text into digestible sections
- **Keep form fields in logical groups** — Use section headings to organize

## The Power of Whitespace

Don't fear whitespace — it's essential for:

- **Reducing cognitive load** — Less overwhelming, easier to process
- **Making content scannable** — Users can quickly find what they need
- **Creating visual hierarchy** — Emphasize important content through space

## Examples

### Bad Proximity
```
What the heck is an Origin Trial?
In this blog post I’ll explain what an origin trial is and how it’s vital...
Browser font rendering inconsistencies
Let’s take a look at what’s happening across different browsers when...
How to use the CSS “appearance” property properly
The “appearance” property has been used by developers to hack their...
Diving into building apps for dual screen devices
Dual screen devices have finally hit the market, but how can we start...
```

### Good Proximity
```
What the heck is an Origin Trial?
In this blog post I’ll explain what an origin trial is and how it’s vital...

Browser font rendering inconsistencies
Let’s take a look at what’s happening across different browsers when...

How to use the CSS “appearance” property properly
The “appearance” property has been used by developers to hack their...

Diving into building apps for dual screen devices
Dual screen devices have finally hit the market, but how can we start...
```

## Practical Application

### Form Design
```html
<!-- Group related fields -->
<fieldset>
  <legend>Personal Information</legend>
  <label>First Name</label>
  <input type="text">

  <label>Last Name</label>
  <input type="text">
</fieldset>

<!-- Separate unrelated section with space -->

<fieldset>
  <legend>Contact Information</legend>
  <label>Email</label>
  <input type="email">

  <label>Phone</label>
  <input type="tel">
</fieldset>
```

### CSS Implementation
```css
/* Create groupings with margin */
.content-group {
  margin-bottom: 2rem; /* Separate groups */
}

.content-group > * + * {
  margin-top: 0.5rem; /* Items within group stay close */
}
```

## Key Takeaway

Proximity is the rule of relationships and is fundamental to organizing information. The closer items are grouped together, the more likely they are to be
related, and the further apart, the less likely.

Mastering proximity will make your designs feel more organized and professional.

---

[← Back to Principles](./index) | [Next: Alignment →](./alignment)

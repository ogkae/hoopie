<div align="center">
<img height="330" src="https://github.com/user-attachments/assets/8ce7693b-a232-4beb-a6a4-5b289ae1da73" />

![Version](https://img.shields.io/badge/v2.3.0-stable-5d5d5d?style=flat-square)  [![Give a star](https://img.shields.io/badge/Give%20a%20⭐-%20-5d5d5d?style=flat-square&logo=github)](https://github.com/ogkae/hoopie/stargazers)

*Built with attention to detail by [ogkae](https://github.com/ogkae)*

</div>

---

**Hoopie** is a modular css framework that brings sophisticated design patterns, smooth animations, advanced visual effects, and production-ready components to your projects. crafted with performance, accessibility, and developer experience in mind.

---

## > table of contents

- [Features](#Features)
- [Quick start](#Quick-start)
- [Components](#Components)
- [Visual effects](#Visual-effects)
- [Animations](#Animations)
- [Responsive utilities](#Responsive-utilities)
- [Typography](#Typography)
- [Theming](#Theming)
- [Browser support](#Browser-support)
- [Performance](#Performance)
- [Accessibility](#Accessibility)
- [Migration guide](#Migration-guide)
- [Contributing](#Contributing)

---

## Quick start

### Installation

```html
<!-- cdn (recommended for quick prototyping) -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ogkae/hoopie@latest/dist/hoopie.min.css">

<!-- or download and serve locally -->
<link rel="stylesheet" href="./hoopie/index.css">
```

### Basic usage

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="./hoopie/index.css">
  <title>hoopie demo</title>
</head>
<body>
  <div class="hp-container">
    <h1 class="hp-h1">welcome to hoopie</h1>
    <button class="hp-btn hp-btn--primary">get started</button>
    
    <div class="hp-card hp-card-elevated hp-depth-lg">
      <h3 class="hp-h3">elegant container</h3>
      <p class="hp-body">with smooth shadows and glassmorphic effects</p>
    </div>
  </div>
</body>
</html>
```

---

## Components

### Buttons

comprehensive button system with multiple variants and states.

```html
<!-- variants -->
<button class="hp-btn hp-btn--primary">primary</button>
<button class="hp-btn hp-btn--secondary">secondary</button>
<button class="hp-btn hp-btn--outline">outline</button>
<button class="hp-btn hp-btn--ghost">ghost</button>
<button class="hp-btn hp-btn--glass">glass</button>

<!-- sizes -->
<button class="hp-btn hp-btn--sm">small</button>
<button class="hp-btn">default</button>
<button class="hp-btn hp-btn--lg">large</button>

<!-- states -->
<button class="hp-btn hp-btn--primary" disabled>disabled</button>
<button class="hp-btn hp-btn--block">full width</button>
```

### Cards

flexible card components for content organization.

```html
<!-- variants -->
<div class="hp-card">default card</div>
<div class="hp-card hp-card-elevated">elevated card</div>
<div class="hp-card hp-card-flat">flat card</div>
<div class="hp-card hp-card-glass hp-glass">glass card</div>

<!-- structured card -->
<div class="hp-card hp-card-elevated">
  <div class="hp-card__header">
    <h3>card title</h3>
  </div>
  <div class="hp-card__body">
    <p>card content goes here</p>
  </div>
  <div class="hp-card__footer">
    <button class="hp-btn hp-btn--primary">action</button>
    <button class="hp-btn hp-btn--outline">cancel</button>
  </div>
</div>
```

### Navbar

responsive navigation component with glass effect support.

```html
<nav class="hp-navbar hp-navbar--glass">
  <a href="#" class="hp-navbar__brand">
    <img src="logo.svg" alt="logo">
  </a>
  <ul class="hp-navbar__menu">
    <li class="hp-navbar__item"><a href="#home">home</a></li>
    <li class="hp-navbar__item"><a href="#about">about</a></li>
    <li class="hp-navbar__item"><a href="#services">services</a></li>
    <li class="hp-navbar__item"><a href="#contact">contact</a></li>
  </ul>
</nav>
```

### Tabs

interactive tab component for content switching.

```html
<div class="hp-tabs">
  <div class="hp-tabs__list">
    <button class="hp-tabs__trigger hp-active">overview</button>
    <button class="hp-tabs__trigger">features</button>
    <button class="hp-tabs__trigger">pricing</button>
  </div>
  <div class="hp-tabs__content">
    <p>tab content appears here</p>
  </div>
</div>
```

### Forms

comprehensive form components with validation states.

```html
<!-- input group -->
<div class="hp-form-group">
  <label class="hp-label required">email address</label>
  <input type="email" class="hp-input" placeholder="your@email.com">
  <span class="hp-form-hint">we never share your email</span>
</div>

<!-- textarea -->
<div class="hp-form-group">
  <label class="hp-label">message</label>
  <textarea class="hp-textarea" rows="4" placeholder="your message"></textarea>
</div>

<!-- select -->
<div class="hp-form-group">
  <label class="hp-label">country</label>
  <select class="hp-select">
    <option>choose a country</option>
    <option>united states</option>
    <option>united kingdom</option>
    <option>canada</option>
  </select>
</div>
```

### Badges

status indicators and labels.

```html
<span class="hp-badge hp-badge--primary">primary</span>
<span class="hp-badge hp-badge--success">success</span>
<span class="hp-badge hp-badge--warning">warning</span>
<span class="hp-badge hp-badge--error">error</span>
<span class="hp-badge hp-badge--info">info</span>
```

### Alerts

notification and message components.

```html
<div class="hp-alert hp-alert--primary">
  <div class="hp-alert__title">information</div>
  <div class="hp-alert__description">this is an informational message</div>
</div>

<div class="hp-alert hp-alert--success">
  <div class="hp-alert__title">success</div>
  <div class="hp-alert__description">operation completed successfully</div>
</div>

<div class="hp-alert hp-alert--warning">
  <div class="hp-alert__title">warning</div>
  <div class="hp-alert__description">please review this information</div>
</div>

<div class="hp-alert hp-alert--error">
  <div class="hp-alert__title">error</div>
  <div class="hp-alert__description">something went wrong</div>
</div>
```

### Tooltips

contextual hover information.

```html
<div class="hp-tooltip">
  hover over me
  <div class="hp-tooltip__content hp-tooltip__content--top">
    tooltip text appears here
  </div>
</div>

<!-- positioning variants -->
<div class="hp-tooltip__content hp-tooltip__content--right">right tooltip</div>
<div class="hp-tooltip__content hp-tooltip__content--bottom">bottom tooltip</div>
<div class="hp-tooltip__content hp-tooltip__content--left">left tooltip</div>
```

### Skeletons

loading state placeholders.

```html
<div class="hp-skeleton hp-skeleton--card"></div>
<div class="hp-skeleton hp-skeleton--text"></div>
<div class="hp-skeleton hp-skeleton--avatar"></div>
<div class="hp-skeleton hp-skeleton--button"></div>
```

### Icons

icon wrapper with sizing and animation utilities.

```html
<div class="hp-icon hp-icon--sm">
  <svg><!-- icon content --></svg>
</div>

<div class="hp-icon hp-icon--md hp-icon--brand">
  <svg><!-- icon content --></svg>
</div>

<div class="hp-icon hp-icon--lg hp-icon--spin">
  <svg><!-- spinner icon --></svg>
</div>
```

---

## Visual effects

### Glassmorphism

modern frosted glass effects with backdrop blur.

```html
<div class="hp-glass">
  <h3>glass effect card</h3>
  <p>with beautiful backdrop blur</p>
</div>

<div class="hp-card hp-card-glass hp-glass">
  <p>glass card variant</p>
</div>
```

### Gradients

pre-built gradient utilities.

```html
<div class="hp-gradient-primary">primary gradient background</div>
<div class="hp-gradient-accent">accent gradient background</div>
<div class="hp-gradient-animated">animated gradient background</div>
```

### Depth and elevation

shadow depth system for layering.

```html
<div class="hp-depth-sm">subtle shadow</div>
<div class="hp-depth-md">medium shadow</div>
<div class="hp-depth-lg">large shadow</div>
<div class="hp-depth-xl">maximum shadow</div>
```

### Glow effects

luminous glow effects for emphasis.

```html
<button class="hp-btn hp-btn--primary hp-glow">
  glowing button
</button>

<div class="hp-card hp-glow-lg">
  card with large glow
</div>

<div class="hp-animate-glow">
  animated pulsing glow
</div>
```

---

## Animations

### Entrance animations

smooth content reveal animations.

```html
<div class="hp-animate-fade-in">fades in smoothly</div>
<div class="hp-animate-slide-up">slides up from bottom</div>
<div class="hp-animate-slide-down">slides down from top</div>
<div class="hp-animate-scale-in">scales from center</div>
<div class="hp-animate-blur-in">blur in effect</div>
```

### Continuous animations

looping animations for dynamic elements.

```html
<div class="hp-animate-pulse">subtle pulsing</div>
<div class="hp-animate-spin">spinning element</div>
<div class="hp-animate-parallax-float">floating parallax</div>
<div class="hp-animate-gradient">animated gradient</div>
```

### Interactive animations

hover and interaction effects.

```html
<div class="hp-animate-hover-lift">lifts on hover</div>
<div class="hp-animate-hover-rotate-3d">3d rotation on hover</div>
<div class="hp-animate-press">press animation on click</div>
<div class="hp-animate-hover-scale">scales on hover</div>
```

---

## Responsive utilities

### Grid system

flexible grid with auto-responsive behavior.

```html
<!-- auto-responsive grid -->
<div class="hp-grid hp-grid--auto">
  <div>item 1</div>
  <div>item 2</div>
  <div>item 3</div>
</div>

<!-- fixed column grids -->
<div class="hp-grid hp-grid--2">2 columns</div>
<div class="hp-grid hp-grid--3">3 columns</div>
<div class="hp-grid hp-grid--4">4 columns</div>
```

### Spacing utilities

consistent spacing system.

```html
<!-- gaps -->
<div class="hp-gap-1">extra small gap (0.25rem)</div>
<div class="hp-gap-2">small gap (0.5rem)</div>
<div class="hp-gap-3">medium gap (1rem)</div>
<div class="hp-gap-4">large gap (1.5rem)</div>

<!-- padding -->
<div class="hp-p-1">padding xs</div>
<div class="hp-p-2">padding sm</div>
<div class="hp-p-3">padding md</div>
<div class="hp-p-4">padding lg</div>

<!-- margin -->
<div class="hp-m-2">margin small</div>
<div class="hp-m-3">margin medium</div>
```

### Visibility controls

responsive visibility utilities.

```html
<div class="hp-hidden-sm">hidden on small screens</div>
<div class="hp-hidden-md">hidden on medium screens</div>
<div class="hp-hidden-lg">hidden on large screens</div>
```

---

## Typography

### Heading system

responsive heading scales.

```html
<h1 class="hp-h1">heading level 1</h1>
<h2 class="hp-h2">heading level 2</h2>
<h3 class="hp-h3">heading level 3</h3>
<h4 class="hp-h4">heading level 4</h4>
```

### Text utilities

body text and modifiers.

```html
<p class="hp-body">default body text</p>
<p class="hp-body-sm">small body text</p>
<p class="hp-body-lg">large body text</p>

<p class="hp-text-balance">balanced line breaks for better readability</p>
<p class="hp-font-bold">bold text weight</p>
<p class="hp-tracking-wide">wide letter spacing</p>
<p class="hp-tracking-tight">tight letter spacing</p>
```

---

## Theming

### Built-in themes

```html
<!-- light theme (default) -->
<html data-theme="default">

<!-- neon theme -->
<html data-theme="neon">

<!-- forest theme -->
<html data-theme="forest">

<!-- sunset theme -->
<html data-theme="sunset">
```

### Custom themes

create custom themes by overriding css custom properties. see [customization.md](./CUSTOMIZATION.md) for complete theming guide.

```css
:root {
  --hp-primary: #your-color;
  --hp-secondary: #your-color;
  --hp-radius: 12px;
  /* override any design token */
}
```

---

## Browser support

hoopie supports all modern browsers with graceful degradation:

| browser | minimum version |
|---------|----------------|
| chrome / edge | 88+ |
| firefox | 87+ |
| safari | 15+ |
| opera | 74+ |

**features with fallbacks:**
- container queries → standard media queries
- backdrop-filter → solid backgrounds
- scroll-linked animations → standard animations
- css `clamp()` → fixed sizes

---

## Performance

### Optimization features

```css
/* respects user preferences */
@media (prefers-reduced-motion: reduce) {
  * {
    animation-duration: 0.01ms !important;
    transition-duration: 0.01ms !important;
  }
}

/* gpu-accelerated transforms */
.hp-animate-hover-lift {
  transform: translateZ(0); /* force gpu acceleration */
}
```

---

## Accessibility

hoopie is built with accessibility in mind:

- ✅ **wcag 2.1 aa** color contrast ratios
- ✅ **semantic html** throughout components
- ✅ **keyboard navigation** support
- ✅ **screen reader friendly** with proper aria labels
- ✅ **reduced motion** support via `prefers-reduced-motion`
- ✅ **focus indicators** on all interactive elements

### Accessibility checklist

when using hoopie components:

```html
<!-- ✅ good: semantic html with proper labels -->
<button class="hp-btn hp-btn--primary" aria-label="submit form">
  submit
</button>

<!-- ✅ good: proper form labels -->
<label class="hp-label" for="email">email</label>
<input type="email" id="email" class="hp-input">

<!-- ✅ good: meaningful alt text -->
<img src="hero.jpg" alt="team collaboration in modern office">
```

---

## Migration guide

### From bootstrap

```html
<!-- bootstrap -->
<button class="btn btn-primary btn-lg">click</button>

<!-- hoopie -->
<button class="hp-btn hp-btn--primary hp-btn--lg">click</button>
```

### From tailwind

```html
<!-- tailwind -->
<div class="bg-blue-500 text-white p-4 rounded-lg shadow-xl">

<!-- hoopie -->
<div class="hp-card hp-card-elevated hp-depth-lg">
```

---

## Contributing

we welcome contributions! please read [Contributing.md](./contributing.md) for guidelines.

**priority areas:**
- [ ] additional component variants
- [ ] enhanced animation library
- [ ] expanded theme collection
- [ ] comprehensive examples
- [ ] performance benchmarks

---

## > contributors

<a href="https://github.com/ogkae/hoopie/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ogkae/hoopie" />
</a>

---

## License

hoopie is released under the [MIT License](./license)

---

<div align="center">

made by [ogkae](https://github.com/ogkae)

[Documentation](./docs) · [Examples](./examples) · [Customization](./customization.md) · [Changelog](./changelog.md)

<code> ⭐ star this repo if hoopie powers your project </code>

</div>

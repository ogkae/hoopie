# Customization guide

*adapt hoopie to your brand and design system.*

## Design tokens

```css
:root {
  --hp-brand: #3b82f6;
  --hp-accent: #8b5cf6;
  --hp-text-primary: #0f172a;
  --hp-bg-primary: #ffffff;
}
```

## Color system

### Primary palette

```css
:root {
  --hp-primary: #0f172a;
  --hp-accent: #3b82f6;
  --hp-secondary: #8b5cf6;
  --hp-brand-50: #eff6ff;
  --hp-brand-100: #dbeafe;
  --hp-brand-500: #3b82f6;
  --hp-brand-900: #1e3a8a;
}
```

### Semantic colors

```css
:root {
  --hp-success: #10b981;
  --hp-warning: #f59e0b;
  --hp-error: #ef4444;
  --hp-info: #06b6d4;
}
```

## Dark mode

customize dark theme automatically detected by prefers-color-scheme:

```css
@media (prefers-color-scheme: dark) {
  :root {
    --hp-bg-primary: #0f172a;
    --hp-bg-secondary: #1e293b;
    --hp-text-primary: #f8fafc;
    --hp-text-secondary: #cbd5e1;
    --hp-border: #334155;
  }
}
```

## Typography

### Font families

```css
:root {
  --hp-font-display: "Inter Tight", system-ui;
  --hp-font-ui: "Inter", system-ui;
  --hp-font-mono: "Fira Code", monospace;
}
```

### Responsive scales

```css
:root {
  --hp-text-xs: clamp(0.75rem, 1vw, 0.875rem);
  --hp-text-sm: clamp(0.875rem, 1.2vw, 1rem);
  --hp-text-base: clamp(1rem, 1.5vw, 1.125rem);
  --hp-text-lg: clamp(1.125rem, 1.8vw, 1.25rem);
  --hp-text-3xl: clamp(1.875rem, 3vw, 2.25rem);
}
```

### Letter spacing

```css
:root {
  --hp-tracking-tight: -0.025em;
  --hp-tracking-normal: 0em;
  --hp-tracking-wide: 0.025em;
  --hp-tracking-wider: 0.05em;
}
```

## Spacing scale

customize spacing increments:

```css
:root {
  --hp-spacing-xs: 0.25rem;
  --hp-spacing-sm: 0.5rem;
  --hp-spacing-md: 1rem;
  --hp-spacing-lg: 1.5rem;
  --hp-spacing-xl: 2rem;
  --hp-spacing-2xl: 3rem;
  --hp-spacing-3xl: 4rem;
}
```

## Border radius

customize rounding:

```css
:root {
  --hp-radius-sm: 0.375rem;
  --hp-radius-md: 0.5rem;
  --hp-radius-lg: 0.75rem;
  --hp-radius-xl: 1rem;
  --hp-radius-2xl: 1.5rem;
  --hp-radius-full: 9999px;
}
```

## Shadow system

customize elevation shadows:

```css
:root {
  --hp-shadow-elevation-1: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  --hp-shadow-elevation-2: 0 1px 3px 0 rgba(0, 0, 0, 0.1);
  --hp-shadow-elevation-3: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
  --hp-shadow-elevation-4: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
  --hp-shadow-elevation-5: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
  --hp-shadow-glass: 0 8px 32px rgba(31, 38, 135, 0.37);
}
```

## Transitions

customize animation timing:

```css
:root {
  --hp-transition-fast: 150ms cubic-bezier(0.4, 0, 0.2, 1);
  --hp-transition-base: 250ms cubic-bezier(0.4, 0, 0.2, 1);
  --hp-transition-slow: 350ms cubic-bezier(0.4, 0, 0.2, 1);
}
```

## Theme variants

create named theme variants:

```css
[data-theme="neon"] {
  --hp-brand: #d400ff;
  --hp-accent: #ff006e;
}

[data-theme="forest"] {
  --hp-brand: #00a15f;
  --hp-accent: #05d9c4;
}

[data-theme="sunset"] {
  --hp-brand: #ff6b35;
  --hp-accent: #ffc93b;
}
```

switch themes:

```javascript
document.documentElement.dataset.theme = "neon";
```

## Component extensions

extend components with custom variants:

```css
/* custom button variant */
.hp-btn--neon {
  background: linear-gradient(135deg, #d400ff, #ff006e);
  color: #fff;
  box-shadow: 0 0 20px rgba(212, 0, 255, 0.5);
}

.hp-btn--neon:hover {
  box-shadow: 0 0 40px rgba(212, 0, 255, 0.8);
}

/* custom card variant */
.hp-card--featured {
  border: 2px solid var(--hp-accent);
  background: linear-gradient(135deg, 
    rgba(59, 130, 246, 0.05), 
    rgba(139, 92, 246, 0.05)
  );
}
```

## Animation customization

modify animation behavior:

```css
/* slower animations for preference */
:root {
  --hp-transition-base: 400ms cubic-bezier(0.4, 0, 0.2, 1);
}

/* custom animation */
@keyframes hp-custom-bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-1rem); }
}

.hp-animate-custom {
  animation: hp-custom-bounce 2s ease-in-out infinite;
}
```

## Responsive breakpoints

customize responsive utilities:

```css
@media (max-width: 640px) {
  .hp-grid--4 {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 1024px) {
  .hp-grid--3 {
    grid-template-columns: repeat(2, 1fr);
  }
}
```
# Contributing to hoopie

guidelines for contributing to the framework.

## Development setup

clone and install:

```bash
git clone https://github.com/ogkae/hoopie.git
cd hoopie
```

## Code standards

### Naming conventions

- use lowercase prefixed classes: `.hp-{component}`
- variants: `.hp-{component}--{variant}`
- element modifiers: `.hp-{component}__{element}`
- states: `.hp-{state}` (e.g., `.hp-active`)
- utilities: `.hp-{property}-{value}`

### CSS guidelines

- use css custom properties (variables) for all values
- write lowercase comments in english
- follow modular component structure
- keep selectors simple and performant
- ensure gpu-accelerated animations
- support dark mode automatically
- respect prefers-reduced-motion

### File structure

components belong in \`src/hoopie/components/\`

core utilities in \`src/hoopie/core/\`

each file focuses on single responsibility

## Component development

when creating new components:

1. create file in \`src/hoopie/components/component-name.css\`
2. use bem naming structure consistently
3. include all variant states
4. support dark mode with automatic detection
5. add animation and transition support
6. ensure keyboard navigation ready
7. test screen reader compatibility
8. update \`src/hoopie/index.css\` imports

example component:

```css
/* component-name.css */
/* hoopie component - description */

.hp-component {
  /* base styles */
}

.hp-component--variant {
  /* variant styles */
}

/* dark mode support */
@media (prefers-color-scheme: dark) {
  .hp-component {
    /* dark mode overrides */
  }
}

/* reduced motion support */
@media (prefers-reduced-motion: reduce) {
  .hp-component {
    animation: none;
    transition: none;
  }
}
```

## Documentation

update documentation when adding features:

- `README.md\` - component usage and examples
- `CUSTOMIZATION.md\` - theming and variable changes
- `CONTRIBUTING.md\` - development guidelines
- inline css comments for complex logic

## Testing requirements

before submitting:

- test in chrome, firefox, safari
- verify dark mode support
- check mobile/tablet responsiveness
- test keyboard navigation
- validate with screen readers
- ensure animation performance
- test with prefers-reduced-motion

## Performance requirements

- keep component css minimal
- use gpu-accelerated transforms
- avoid complex selectors
- maintain fast animation performance
- minimal performance impact on page load

## Submitting changes

1. fork the repository
2. create descriptive feature branch
3. commit with clear messages
4. verify all tests pass
5. open pull request with details

pull request should include:

- clear description of changes
- before/after behavior if applicable
- browser testing results
- accessibility considerations

## Reporting issues

create issue with:

- descriptive title
- clear reproduction steps
- affected browsers and versions
- screenshot if visual issue
- performance impact if applicable

## References

web standards and best practices:

[W3C CSS SPECS](https://www.w3.org/style/css)

[MDN CSS GUIDE](https://developer.mozilla.org/en-us/docs/web/css)

[WCAG ACCESS](https://www.w3.org/wai)

[CSS PERFORMANCE](https://developer.mozilla.org/en-us/docs/web/performance/css_animations_performance)

---

**thank you for contributing to hoopie <3**

# Directives

This directory contains custom Vue directives.

## Usage

- Custom Vue directives for DOM manipulation
- Reusable DOM behavior across components
- Specialized UI interactions

## Example Structure

```
directives/
├── clickOutside.ts       # Click outside directive
├── focus.ts              # Auto-focus directive
├── tooltip.ts            # Tooltip directive
├── lazyLoad.ts           # Lazy loading directive
└── index.ts              # Directive exports
```

## Best Practices

- Use descriptive names for directives
- Keep directives focused on DOM manipulation
- Handle cleanup in directive unbind hooks
- Use TypeScript for type safety
- Document directive usage and options 
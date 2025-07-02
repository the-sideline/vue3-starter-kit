# Layouts

This directory contains layout components that wrap pages.

## Usage

- Page layout components
- Common page structure (header, footer, sidebar)
- Layout variations for different page types
- Responsive layout components

## Example Structure

```
layouts/
├── DefaultLayout.vue      # Default page layout
├── AuthLayout.vue         # Authentication pages layout
├── DashboardLayout.vue    # Dashboard pages layout
├── AdminLayout.vue        # Admin pages layout
└── index.ts               # Layout exports
```

## Best Practices

- Use descriptive names ending with "Layout"
- Keep layouts focused on structure and composition
- Use slots for flexible content areas
- Make layouts responsive by default
- Use CSS Grid or Flexbox for layout structure 
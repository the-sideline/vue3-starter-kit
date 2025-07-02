# Views

This directory contains route-level components (page components).

## Usage

- Place route components here that represent full pages
- These components are typically used in the router configuration
- Each view should be self-contained and represent a complete page

## Example Structure

```
views/
├── HomeView.vue          # Home page component
├── AboutView.vue         # About page component
├── UserProfileView.vue   # User profile page
└── DashboardView.vue     # Dashboard page
```

## Best Practices

- Use descriptive names ending with "View"
- Keep views focused on layout and composition
- Delegate complex logic to composables or stores
- Use layouts for consistent page structure 
# Composables

This directory contains reusable composition functions (Vue 3 Composition API).

## Usage

- Reusable logic that can be shared across components
- State management that doesn't belong in stores
- Side effects and lifecycle management
- Custom hooks for common functionality

## Example Structure

```
composables/
├── useLocalStorage.ts     # LocalStorage management
├── useTheme.ts            # Theme management
├── useApi.ts              # API call management
├── useForm.ts             # Form handling
├── useModal.ts            # Modal state management
└── useDebounce.ts         # Debounce utility
```

## Best Practices

- Use "use" prefix for composable names
- Keep composables focused on a single concern
- Return reactive data and functions
- Handle cleanup in onUnmounted if needed
- Use TypeScript for better type safety
- Test composables independently 
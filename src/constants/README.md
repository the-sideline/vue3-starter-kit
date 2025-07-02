# Constants

This directory contains application-wide constants and configuration values.

## Usage

- Application configuration constants
- API endpoints and URLs
- Validation rules and patterns
- Feature flags and settings

## Example Structure

```
constants/
├── api.ts                 # API endpoints and URLs
├── validation.ts          # Validation rules and patterns
├── config.ts              # Application configuration
├── routes.ts              # Route names and paths
└── index.ts               # Constant exports
```

## Best Practices

- Use UPPER_SNAKE_CASE for constant names
- Group related constants together
- Export constants from index.ts for easy imports
- Use TypeScript const assertions when possible
- Document complex constants with comments 
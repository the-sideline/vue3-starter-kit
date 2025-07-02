# Services

This directory contains API calls, external service integrations, and business logic.

## Usage

- Place API service functions here
- External service integrations (payment, analytics, etc.)
- Business logic that doesn't belong in components or stores

## Example Structure

```
services/
├── api/
│   ├── auth.ts           # Authentication API calls
│   ├── users.ts          # User-related API calls
│   └── posts.ts          # Post-related API calls
├── external/
│   ├── analytics.ts      # Analytics service integration
│   └── payment.ts        # Payment service integration
└── utils/
    ├── http.ts           # HTTP client configuration
    └── validation.ts     # Validation utilities
```

## Best Practices

- Use descriptive names for service files
- Group related API calls together
- Handle errors consistently
- Use TypeScript interfaces for API responses
- Keep services pure and testable 
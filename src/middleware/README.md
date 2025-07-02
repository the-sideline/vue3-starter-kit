# Middleware

This directory contains route guards, navigation guards, and middleware functions.

## Usage

- Route guards for authentication/authorization
- Navigation guards for route protection
- Middleware functions for request/response processing
- Permission checks and access control

## Example Structure

```
middleware/
├── auth.ts               # Authentication guard
├── guest.ts              # Guest-only route guard
├── admin.ts              # Admin-only route guard
├── permissions.ts        # Permission checking middleware
└── index.ts              # Middleware exports
```

## Best Practices

- Use descriptive names for middleware functions
- Keep middleware focused on a single responsibility
- Handle errors gracefully
- Use TypeScript for type safety
- Test middleware functions thoroughly 
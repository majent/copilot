---
applyTo: "**/*.ts,**/*.tsx"
---

Apply the [general coding guidelines](./general-coding.instructions.md) to all code.

# Project coding standards for React

## React Guidelines

- Use functional components with hooks
- Follow the React hooks rules (no conditional hooks)
- Use React.FC type for components with children
- Keep components small and focused
- Use prop-types for runtime type checking
- Use custom hooks for reusable logic (/src/hooks)
- Manage utility functions for reusable logic (in /src/utils)

## GraphQL Guidelines

- Use snake_case for data transfer objects (such as GraphQL fields)

## Performance

- Use React.memo and useCallback to prevent unnecessary re-renders

## Accessibility

- Follow WCAG guidelines for accessibility
- Use semantic HTML elements
- Ensure keyboard navigability
- Use ARIA attributes where necessary

## SEO

- Use correct keywords in title and meta description and headings
- Use heading tags (h1, h2, etc.) appropriately
- Use alt attributes for images
- Use srcSet for appropriate image sizes
- Use lazy loading for images outside the first view
- Fix height and width for images to prevent layout shifts
- Use S3 and CDN for static assets (https://static.nearme.jp)
- Test SEO performance with tools like Lighthouse

## Security

- Sanitize user inputs to prevent XSS attacks
- Avoid exposing sensitive information in the frontend code

---
trigger: always_on
---

# Next.js Best Practices

## Directory Structure

```
src/
├── app/         # Routing & Pages
├── components/  # React Components
│   ├── ui/      # ShadCn UI Components
│   └── layouts/ # Layouts
├── hooks/       # Custom Hooks
└── lib/         # Utilities
    ├── constants/
    ├── types/
    └── utils/
```

## Naming Conventions

- Pages: `page.tsx`
- Layouts: `layout.tsx`
- Loading: `loading.tsx`
- Error: `error.tsx`
- API: `route.ts`

## Component Design

### Server Components (Default)

- Data Fetching
- SEO Support

### Client Components (When Needed)

- Browser APIs
- Event Listeners
- React Hooks
- Client State

```typescript
"use client"; // Client Component
```

## API Design

- **No GET APIs** – fetch data in Server Components
- **Only POST/PATCH/PUT/DELETE**
- Prefer Server Actions

## Optimization

- Optimize images with `next/image`
- Load scripts with `next/script`
- Cache strategy: `{ next: { revalidate: 3600 } }`
- Enable TypeScript strict mode

## Error Handling

- Catch errors with `error.tsx`
- Handle loading states with `loading.tsx`
- Use try-catch where needed
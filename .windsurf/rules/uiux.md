---
trigger: glob
globs: *.tsx
---

# UI/UX Design & Implementation Rules

## Key Constraints

- **No UI changes without approval**
- Get approval before modifications
- Be extra careful with layout/colors/fonts/spacing

## Design System

- **Shadcn/ui** based
- Minimal customization
- Reuse existing components first

## Styling

- **Tailwind CSS** utility classes first
- Use `@layer` for custom classes
- Naming: `kebab-case`

## Responsive & Accessibility

- Mobile-first approach
- Follow WAI-ARIA guidelines
- Keyboard navigation support
- Sufficient color contrast

## Animations & Forms

- Use `tailwindcss/animation`
- Avoid excessive animations
- Use Shadcn/ui form components
- Clear validation messages

## Icons & Error Handling

- Standard: **Lucide Icons**
- Optimize images with `next/image`
- Use `@/components/ui/sonner` for toasts
- Clear, specific error messages

## Dark Mode

- Use `dark:` prefix
- Sync with system preferences
- Maintain contrast ratios
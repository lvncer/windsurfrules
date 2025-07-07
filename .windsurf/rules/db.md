---
trigger: manual
---

# Database Design Rules


## Naming

- Models: Singular PascalCase (`User`, `Project`)
- Fields: camelCase (`firstName`, `createdAt`)
- Primary keys: `id`
- Foreign keys: `[referencedTable]Id`
- Timestamps: `createdAt`, `updatedAt`

## Data Types

- Strings: `String`
- Numbers: `Int`, `Float`
- Boolean: `Boolean`
- DateTime: `DateTime`
- Arrays: `String[]`, `Int[]`
- JSON: `Json`

## Relations

- One-to-many: `@relation`
- Many-to-many: junction table
- One-to-one: `@relation` + `@unique`
- Cascade delete: `onDelete: Cascade`

## Indexes & Validation

- Index frequently queried fields
- Always index foreign keys
- Required fields: no `?`
- Optional fields: include `?`

## File Locations

- **SQL files**: `/public/sql/` directory
- Migrations: `prisma/migrations/`

## Security

- Encrypt sensitive data
- Validate all inputs
- Set proper access permissions
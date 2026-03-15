# Zod Data Validation

Zod is a TypeScript-first schema declaration and validation library.

## Basic Schemas
```typescript
import { z } from "zod";

const UserSchema = z.object({
  username: z.string().min(3).max(20),
  email: z.string().email(),
  age: z.number().positive().optional(),
  isAdmin: z.boolean().default(false),
});

// Infer TypeScript type from schema
type User = z.infer<typeof UserSchema>;
```

## Validation
```typescript
const result = UserSchema.safeParse(data);

if (result.success) {
  const user = result.data; // Fully typed
} else {
  console.log(result.error.format()); // Friendly error messages
}
```

## Useful Features
- `.optional()`: Makes a field optional.
- `.nullable()`: Allows null values.
- `.default(value)`: Sets a default value.
- `.array()`: `z.array(z.string())`.
- `.enum()`: `z.enum(["Admin", "User"])`.
- `.refine()`: Custom validation logic.

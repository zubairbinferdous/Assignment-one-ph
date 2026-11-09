## Introduction

In TypeScript, both `type` and `interface` are used to set the structure of data. They help us define what properties should have.

They look similar, but they have some differences.

## Differences and Usage

The main difference is that an `interface` can be declared more than once. This is called **declaration merging**.

A `type` alias cannot be declared again with the same name.

### Example:

```typescript
// Interface can declared more than once
interface UserProfile {
    name: string;
}

interface UserProfile {
    age: number;
}

// Both properties are combined
// name: string
// age: number


// Type alias can define unions and tuples
type Status = "pending" | "success" | "failed";

type Coordinate = readonly [number, number];
```

Another difference is that `type` can work with more kinds of data, such as:
- Strings and numbers
- Union types
- Tuples
- Objects

An `interface` is mainly used to describe the structure of objects and classes.

Both can also be extended:
- An `interface` uses the `extends` keyword.

## Conclusion

Use `interface` when you want to describe objects, classes, or when you need to add more properties later.

Use `type` when you want to create union types, primitive types, tuples, or combine different types.

Both are useful in TypeScript. Choosing the right one helps make your code simple, clean, and easy to understand.
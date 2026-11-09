## Introduction

In TypeScript, both `type` and `interface` are used to define the structure of data. They help us describe what properties an object should have. They look similar, but they have some important differences. Understanding these differences helps us write better TypeScript code.

## Differences and Usage

The main difference is that an `interface` can be declared more than once with the same name. This feature is called **declaration merging**. TypeScript combines all the properties into one interface. However, a `type` alias cannot be declared again with the same name.

### Example:

```typescript
// Interface can be declared more than once
interface UserProfile {
    name: string;
}

interface UserProfile {
    age: number;
}

// Both properties are combined

// Type alias can define unions and tuples
type Status = "pending" | "success" | "failed";

type Coordinate = readonly [number, number];
```

Another difference is that `type` can represent strings, numbers, unions, tuples, and objects. An `interface` is mainly used to describe the structure of objects and classes. Both can also be extended using the `extends` keyword.

## Conclusion

Use `interface` when describing objects, classes, or when you need declaration merging. Use `type` when creating union types, primitive types, tuples, or combining different types. Both are useful in TypeScript. Choosing the right one makes your code cleaner, simpler, and easier to maintain.
```
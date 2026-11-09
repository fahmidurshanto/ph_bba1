# Difference Between Type Alias and Interface in TypeScript

## Introduction
When I started learning TypeScript, I saw both `type` and `interface` are used to define the shape of data. At first, they looked almost the same to me. But when we build real projects, we see some clear differences between them.

## Key Differences

### 1. Declaration Merging
We can write the same interface name multiple times, and TypeScript will join them together automatically. But if we try to do this with a type alias, TypeScript gives an error.

```typescript
// Interface merges automatically
interface User {
  name: string;
}
interface User {
  age: number;
}
// Now User has both name and age
```

### 2. Working with Primitives and Unions
With `type`, we can easily make union types, primitive types, or tuples. An `interface` cannot do this because it is only made to describe objects.

```typescript
// Allowed with type alias
type ID = string | number;
type Coordinates = [number, number];
```

### 3. Extending
An interface extends another interface using the `extends` keyword. A type alias uses the `&` (intersection) symbol to join types together.

```typescript
interface Animal {
  name: string;
}
interface Dog extends Animal {
  breed: string;
}
```

## When to Choose Which?
I use `interface` when I am working with object shapes, classes, or when writing APIs because it is easy to extend. On the other hand, I choose `type` whenever I need union types, tuples, or simple primitive aliases.

## Conclusion
Both type and interface are very important in TypeScript. For regular object models and OOP code, interface is the best choice. For unions and complex type combinations, type alias is better.

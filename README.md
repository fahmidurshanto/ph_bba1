# Assignment 1: Problem Solving with TypeScript & OOP

This repository contains solutions for Assignment 1 (Batch 8) covering TypeScript fundamentals, advanced types, generics, asynchronous operations, and OOP concepts.

## Project Structure
```text
├── src/
│   ├── solutions.ts
│   ├── type-vs-interface.md
│   └── type-narrowing.md
├── tsconfig.json
└── README.md
```

## Problem Solving (`src/solutions.ts`)
The `src/solutions.ts` file contains implementations for 8 problems:
1. `multiplyValue`: Handles multiplication with default parameter and proper `0` check.
2. `processInput`: Type narrowing with `typeof` for string, number, and boolean unions.
3. `formatCoordinate`: Working with readonly tuples `[latitude, longitude, locationName]`.
4. `concatenateArrays`: Generic function combining multiple arrays using rest parameters without `any`.
5. `getPopularCourses`: Interface definition and filtering published courses by student count.
6. `pluckValues`: Generic key extraction using `keyof` constraint (`<T, K extends keyof T>`).
7. `Employee` & `Manager`: OOP class inheritance with `protected` and `private` access modifiers.
8. `validateAgeAsync`: Async age validation returning `Promise<string>` with timer delay and Error rejection.

## Blog Posts
- [Blog 1: Difference Between Type Alias and Interface in TypeScript](./type-vs-interface.md)
- [Blog 2: What is Type Narrowing in TypeScript?](type-narrowing.md)

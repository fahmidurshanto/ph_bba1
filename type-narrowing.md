# What is Type Narrowing in TypeScript?

## Introduction
In TypeScript, we often use union types like `string | number`. But when a variable can hold more than one type, TypeScript does not let us use type-specific methods directly. Type narrowing is how we check the type at runtime so TypeScript knows the exact type inside our code block.

## Practical Examples of Type Narrowing

### 1. Using `typeof`
The `typeof` guard is very useful for checking basic types like `string`, `number`, or `boolean`.

```typescript
function printLength(value: string | number) {
  if (typeof value === "string") {
    // TypeScript knows value is string here
    console.log(value.length);
  } else {
    // TypeScript knows value is number here
    console.log(value * 2);
  }
}
```

### 2. Using `instanceof`
When we work with classes or built-in objects, we can use `instanceof` to check if an object was created from a specific class constructor.

```typescript
class Car {
  drive() {
    console.log("Driving a car");
  }
}

function startVehicle(vehicle: Car | string) {
  if (vehicle instanceof Car) {
    vehicle.drive();
  }
}
```

### 3. Using the `in` Operator
If we have different object types in a union, we can check if a property exists inside the object using the `in` keyword.

```typescript
type Fish = { swim: () => void };
type Bird = { fly: () => void };

function move(animal: Fish | Bird) {
  if ("swim" in animal) {
    animal.swim();
  } else {
    animal.fly();
  }
}
```

## Conclusion
Type narrowing makes our TypeScript code safer and prevents runtime errors. By using simple guards like `typeof`, `instanceof`, and `in`, we help TypeScript understand our data types and write bug-free applications.

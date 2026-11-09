# Type Aliases vs Interfaces

TypeScript helps us write safer code by giving names to data types. Two common ways to do this are `type` aliases and `interface`. Both help us describe the shape of data, but they have some differences.

## What Is a Type Alias?

A type alias gives a name to a type. We use the `type` keyword to create it. It can describe objects, numbers, strings, unions, and more.

```typescript
type User = {
    name: string;
    age: number;
};

const user: User = {
    name: "Uttam",
    age: 38
};
```

Here, `User` is a name for an object type.

## What Is an Interface?

An interface also describe the shape of an object. We use the `interface` keyword.

```typescript
interface Student {
    name: string;
    age: number;
}

const student: Student = {
    name: "Shilpo",
    age: 5
};
```

Here, `Student` tells us which properties an object must have.

## Main Differences

Both can describe objects and support `extends`. However, a type alias can also create union and intersection types. An interface cannot directly create a union type.

Another difference is that interfaces support declaration merging. This means we can write the same interface name more than once, and TypeScript joins them together. Type aliases do not support this feature.

## When to Choose Which

Use an interface for objects and classes, because it is clear and easy to extend. Use a type when you need a union, a tuple, or any special type that an interface cannot describe.


Type aliases and interfaces are both useful. Choose the one that makes your code easier to read and understand.
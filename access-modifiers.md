# Access Modifiers in TypeScript OOP

Object-Oriented Programming (OOP) acts like a design or blueprint for creating classes and objects. Often, we may want to control who can access the properties and methods of a class. TypeScript provides 'access modifiers' to help us manage this. The four key keywords for this purpose are `public`, `private`, `protected`, and `readonly`.

## 1. Public

The `public` keyword means everyone can access a property or method. It is the default access level in TypeScript.

```typescript
class Student {
    public name: string = "Shilpo";
}

const student = new Student();
console.log(student.name);
```

Here, we can access `name` from outside the class.

## 2. Private

The `private` keyword means a property or method can only be used inside its own class.

```typescript
class BankAccount{
    private balance: number = 500;
}
```

We cannot access `balance` directly from outside the class.

## 3. Protected

The `protected` keyword allows access inside the class and its child classes. However, we cannot access it directly from outside.

```typescript
class Animal {
    protected name: string = "Dog";
}

class Dog extends Animal {
    showName(): string {
        return this.name;
    }
}
```

The `Dog` class can use the `name` property because it extend `Animal`.

## 4. Readonly

The `readonly` keyword means a property can be given a value when it is created, but it cannot be changing later.

```typescript
class Product {
    readonly price: number = 100;
}
```

We cannot change `price` after it has been initialized.


Access modifiers help us protect data and organize our code. Use `public` for open access, `private` for class-only access, `protected` for parent and child classes, and `readonly` for values that should not change after initialization.
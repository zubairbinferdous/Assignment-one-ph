## Introduction

Object-Oriented Programming (OOP) uses access modifiers to protect data on classes. TypeScript provides four modifiers: `public`, `private`, `protected`, and `readonly`. These modifiers control how class properties can be accessed.

## How Access Modifiers Work

In TypeScript, class properties are `public` by default. This means they can be accessed and changed from anytime.

- **Public:** Anyone can access or change the property.
- **Private:** Only the same class can access the property.
- **Protected:** The same class and its child classes can access the property.
- **Readonly:** The property can only be assigned a value once, can't modify this .

### Example:

```typescript
class Vehicle {
    public brand: string;
    private vinNumber: string;
    protected speed: number = 0;
    readonly wheels: number;

    constructor(brand: string, vin: string, wheels: number) {
        this.brand = brand;
        this.vinNumber = vin;
        this.wheels = wheels;
    }
}

class Car extends Vehicle {
    accelerate() {
        this.speed += 10;
    }
}
```

In this example:
- `brand` is public, so anyone can access it.
- `vinNumber` is private, so only the Vehicle class can use it.
- `speed` is protected, so the Car class can also use it.
- `wheels` is readonly, so its value cannot be changed after set.

## Conclusion

Access modifiers help us protect data and keep our code organized. They make our applications safer and easy to maintain. We use `private` to hide data, `protected` to share data with child classes, `readonly` to prevent changes, and `public` when everyone needs access. Choosing the correct modifier helps us write better and cleaner  code.
```
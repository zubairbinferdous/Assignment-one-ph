## Introduction

Object-Oriented Programming (OOP) uses access modifiers to protect data in class. TypeScript provides four modifiers: `public`, `private`, `protected`,`readonly`. 

## How Access Modifiers Work

In TypeScript, class properties `public` by default. This means they can be accessed and changed from anywhere.

- **Public:** Anyone can access or change the property.
- **Private:** Only the same class can access the property. Other classes cannot use it .
- **Protected:** The same class and its child classes can access the property. Outside code cannot access it.
- **Readonly:** The property can only be set once. After that it value cannot be changed.

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
- `wheels` is readonly, so its value cannot be changed .

## Conclusion

Access modifiers help us protect data and keep our code organized. We use `private` to hide data, `protected` to share data with child classes, `readonly` to stop changes, and `public` when everyone needs access.


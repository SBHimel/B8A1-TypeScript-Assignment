# Access Modifiers in TypeScript OOP

## Introduction

In TypeScript, classes help us create objects with properties and methods. But sometimes we do not want every property to be accessible from everywhere. Access Modifiers help us control where a property or method can be used. TypeScript has three main access modifiers: public, private, and protected. We can also use readonly to prevent a property from being changed.

## Types of Access Modifiers

### 1. Public

Public properties and methods can be accessed from anywhere. It is the default access modifier in TypeScript.

### 2. Private

Private properties can only be accessed inside their own class. We cannot directly access them from outside the class or from a child class.

### 3. Protected

Protected properties can be accessed inside their own class and its child classes. This is useful when one class extends another class.

### 4. Readonly

Readonly properties can be assigned a value when they are declared or inside the constructor. After that, we cannot change their values.

## Practical Example

```ts
class Employee {
  public name: string;
  private salary: number;
  protected department: string;
  readonly id: number;

  constructor(
    name: string,
    salary: number,
    department: string,
    id: number
  ) {
    this.name = name;
    this.salary = salary;
    this.department = department;
    this.id = id;
  }
}
```

Here, name is public, salary is private, and department is protected. The id property is readonly, so its value cannot be changed after initialization.

## Conclusion

Access Modifiers help us control access to class properties and methods. They make our code more organized and help protect important data. Understanding these modifiers is important when working with TypeScript OOP.
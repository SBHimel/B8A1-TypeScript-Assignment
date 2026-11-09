# Type Narrowing in TypeScript

## Introduction

TypeScript helps us write safer code by checking data types. Sometimes a variable can have more than one type. For example, a value can be a string or a number. In this situation, we need to check its actual type before using it. This process is called Type Narrowing.

## What is Type Narrowing?

Type Narrowing means making a variable's possible type more specific through conditions. It helps TypeScript understand which type we are working with. There are different ways to do this.

### 1. Using typeof

We can use the `typeof` operator to check basic types like string, number, and boolean.

```ts
function processInput(value: string | number): void {
  if (typeof value === "string") {
    console.log(value.toLowerCase());
  } else {
    console.log(value * 10);
  }
}
```

Here, TypeScript understands that value is a string inside the first condition and a number inside the else block.

### 2. Using instanceof

We can use `instanceof` to check whether an object belongs to a particular class.

```ts
class Student {}

const student = new Student();

if (student instanceof Student) {
  console.log("This is a Student");
}
```

### 3. Using the in Operator

The `in` operator checks whether a property exists inside an object.

```ts
type Admin = {
  name: string;
  permissions: string[];
};

type Subscriber = {
  name: string;
  subscription: string;
};

function showUserInfo(user: Admin | Subscriber): void {
  if ("permissions" in user) {
    console.log(user.permissions);
  } else {
    console.log(user.subscription);
  }
}
```

Here, TypeScript checks whether the object has a name property.

## Conclusion

Type Narrowing is useful when we work with different types in one variable. It helps us avoid type-related errors and write safer code. By using `typeof`, `instanceof`, and `in`, we can check values and work with the correct type. It is an important concept for writing TypeScript programs.




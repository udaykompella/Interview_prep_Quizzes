## 1. What is the difference between type inference for let and const declarations in TypeScript?

For let declarations, TypeScript infers a general type (like number) because the variable can be reassigned to other values of that type. For const declarations with immutable value types (numbers, strings), TypeScript infers a literal type (like 79) because the variable cannot be reassigned and the value itself cannot be mutated, so TypeScript knows it will always hold that exact value.

---

## 2. What does the term 'literal type' mean in TypeScript?

A literal type is a type that represents a single, specific value. For example, a const declaration of const humidity = 79 creates a type that only allows the value 79, not any other number.

---

## 3. What is an 'implicit any' type in TypeScript?

An implicit any occurs when a variable is declared without a type annotation and TypeScript cannot infer its type from context. This typically happens when a variable is declared but not initialized. The variable effectively loses type safety and can accept any value, behaving like a regular JavaScript variable. This behavior depends on TypeScript compiler configuration.

---

## 4. How do you provide a type annotation in TypeScript?

To provide a type annotation, use a colon followed by the type name after a variable declaration. For example: let endTime: Date; specifies that endTime must be a Date instance.

---

## 5. What happens when you try to assign a value of a different type to a variable with a specific type in TypeScript?

TypeScript will raise a type checking error. For example, if a variable is inferred to be of type number, trying to assign a string like 'warm' will fail with an error 'string is not assignable to type number'. Similarly, if a variable has a literal type (like 79), you cannot assign it a different value of the same general type (like 78) because the literal type only accepts that exact value.
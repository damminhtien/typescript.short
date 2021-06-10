# Typescript Fundamentals
These tutorials are designed for beginners and professionals who want to learn TypeScript and how to use it in web application.
# Introduction
+ Typescript is the typed superset of Javascript that compiles (transpiles) to Javascript
+ Why typescript rather writing in js:
  + Ts as its name adds type(s) enforcement which js wont
  + Ts has much neat easy to maintain
  + Ts is cross platform
+ Hi world program:
```typescript
function sayHi(name: string): string { 
    return 'Hi ' + name; 
} 

console.log(sayHi('world'));
```
# Types
+ Primitive types:
  + number
  + string
  + boolean
  + any
  + void
  + null
+ Enums and Arrays
  + Enums:
   ```typescript
   enum greeting = { hello, hi, xinchao }
   ```
# Interfaces
```typescript
interface person {
  name: string,
  age: number
}
```

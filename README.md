# Typescript Fundamentals
Short and simple bullet points about Typescript
## 1. Introduction
+ Typescript is the typed superset of Javascript that compiles (transpiles) to Javascript
+ Why Typescript rather writing in Javascript:
  + Typescript as its name adds type(s) enforcement which Javascript wont
  + Typescript has much neat easy to maintain
  + Typescript is cross platform
+ Hi world program:
```typescript
function sayHi(name: string): string { 
    return 'Hi ' + name;
} 
console.log(sayHi('world'))
```
## 2. Types
+ Primitive types:
  + number
  ```typescript
  const n: number = 100
  ```
  + string
  ```typescript
  const s: string = 'Hi world'
  ```
  + boolean
  ```typescript
  const b: boolean = true
  ```
  + any
  ```typescript
  const a: any = 💟
  ```
  + void
  ```typescript
  const v = (): void => {}
  ```
  + null
  ```typescript
  const a: null = null
  ```
+ Enums and Arrays
  + Enums:
   ```typescript
   enum greeting = { hello, hi, xinchao }
   ```
  + Arrays:
  ```typescript
   const greeting Array<string> = [ 'hello', 'hi', 'xinchao' ]
   const fruit string[] = [ 🍏, 🍉,  🥝,  🍇,  🥑,  🥥 ]
   ```
## 3. Interfaces
```typescript
interface Person {
  name: string,
  age: number
}

const ps: Person = { name: 'damminhtien', age: 18 } 

interface SaySmt {
  (name: string): string
}

function sayHi(name: string): string {
  return 'Hi ' + name
}

const sayHiWorld: SaySmt = sayHi
```

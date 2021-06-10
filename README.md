Short and simple bullet points about Typescript 💛

## 1. Introduction

+ Typescript is the typed superset of Javascript that compiles (transpiles) to Javascript
+ Why Typescript rather writing in Javascript:
  + Typescript as its name adds type(s) enforcement which Javascript wont
  + Typescript has much neat easy to maintain
  + Typescript is cross platform
+ Hi world program:
```typescript
function sayHi(name?: string = 'world'): string { 
    return 'Hi ' + name;
} 
console.log(sayHi('world'))
```

## 2. Types

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
+ enums
```typescript
enum greeting = { hello, hi, xinchao }
```
+ Array
```typescript
const greeting Array<string> = [ 'hello', 'hi', 'xinchao' ]
const fruit string[] = [ 🍏, 🍉,  🥝,  🍇,  🥑,  🥥 ]
```

## 3. Function

+ Rest parameters
```typescript
function sayHiEveryOne(...names: Array<string>): string {
    return 'Hi ' + names.join(', ')
}
sayHiEveryOne('Hi ', 'Type', "Script"); // returns 'Hi Type Script'
```

## 4. Interfaces

```typescript
interface Person {
  name: string
  age?: number
  getAge: () => number // arrow function
  getName(): string
}

const ps: Person = { 
  name: 'damminhtien'
  age: 18
  getAge: () => 18
  getName() {
    return 'damminhtien'
  }
} 

interface SaySmt {
  (name: string): string
}

function sayHi(name: string): string {
  return 'Hi ' + name
}

const sayHiWorld: SaySmt = sayHi
```

### 5. Class

+ Simple class
```typescript
class Person {
  readonly name: string
  age?: number

  constructor(name: string, age?: number) {
    this.name = name
    this.age = age
  }

  getAge(): number {
    return this.age
  }
}
```
+ Abstract class

> Note: The class which implements an abstract class must call super() in the constructor

```typescript
class Person {
  abstract name: number
  age: string

  abstract getAge(): number
}

class Lover extends Person {
  name: string
  age: number
  
  constructor() {
  }
}
```

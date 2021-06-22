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
}

const ps: Person = { 
  name: 'damminhtien'
  age: 18
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
+ Data modifiers
  + public
  
  By default, all members of a class in TypeScript are public. All the public members can be accessed anywhere without any restrictions.
  
  ```typescript
  class Dog {
    name: string
    public color: string
  }
  let dog = new Dog()
  dog.name = 'Ki'
  dog.color = 'white'
  ```
  + private
  
  The private access modifier ensures that class members are visible only to that class and are not accessible outside the containing class.
  
  ```typescript
  class Dog {
    name: string
    private color: string
  }
  let dog = new Dog()
  dog.name = 'Ki'
  dog.color = 'white' // error 
  ```
  + protected
  
  The protected access modifier is similar to the private access modifier, except that protected members can be accessed using their deriving classes.
  
  ```typescript
  class Animal {
    protected name: string
    constructor(name: string) {
      this.name = name
    }
  }
  class Dog extends Animal{
    public color: string
    constructor(name: string, color: string) {
      super(name)
      this.color = color
    }
  }
  let dog = new Dog()
  dog.name = 'Ki' // error
  dog.color = 'white'
  ```
+ static

```typescript
class Color {
  static BLUE: number = '#0000FF'
  
  static getBlue(): string {
    return '#0000FF'
  }
}
let blue = Color.BLUE // '#0000FF'
let getBlue = Color.getBlue() // '#0000FF'
```

+ generic classes

```typescript
class Mac<Type> {
  version: Type;
  constructor(v: Type) {
    this.version = v;
  }
}

const b: Mac<string> = new Mac("hello!"); // 
```

### 6. [Decorator](https://saul-mirone.github.io/a-complete-guide-to-typescript-decorator/)

+ Class Decorators

+ Property Decorators

+ Method Decorators

+ Accessor Decorators

+ Parameter Decorators

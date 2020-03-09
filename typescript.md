# XYZ in under 10 minutes

#### Contents

- [Python](index.md)
- [Typescript](#typescript)

## Typescript

### Print

```typescript
console.log('Hello world');
console.table({foo, bar});
console.group();
console.groupEnd();
console.warn();
console.error();
console.time();
```

### Variables

```typescript
let x: number = 4;
const x: number = 2;
let x = `Hello ${firstName} ${lastName}`; // template string
let x = (condition) ? valueIfTrue:valueIfFalse; // conditional operator
```

### Data types

```typescript
// Basic types
let x: number;
let x: string;
let x: boolean;
let x: any;
let x: void;
let x: null;
let x: undefined;

// Array
let arr: string[];
let arr: Array<string>;
arr[0]

// Tuple
let tup: [string, number] = ['hello', 4]

// Enum
enum Color { Red, Green, Blue };
let green: Color = Color.Green
```

### Control flow

```typescript
// while loop
while (condition) { }

// if-else
if (a < b) {
    // statement
} else if (a == b) {
    // statement
} else {
    // statement
}

// switch
switch (variable_expression) {
    case constant_expr1: {
        //statement
        break;
    }
    case constant_expr2: {
        //statement
        break;
    }
    default: {
        //statement 
        break;
    }
}
```

### Functions

```typescript
function myFunction(arg: number): number {
    return arg;
}

// Fat arrow function
let evens = [2, 4, 6, 8];
let odds = evens.map(v => v + 1);
```

### Classes

```typescript
class Person {
    first_name: string;
    last_name: string;

    constructor() {}

    greet(): void {
        console.log('Hello', this.first_name);
    }
}

// Instantiation
let person = new Person();
```

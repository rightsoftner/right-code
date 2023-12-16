[Index](./index.md)

# Return from constructors

Можно примитивные значения возвращать из конструкторов, их нужно оборачивать в классы, но работают они так же, как и примитивы.

```javascript
class Int {
  constructor(value) {
    if (!Number.isInteger(value)) {
      throw new Error("Not an integer");
    }
    return new Number(value);
  }
}

const i = new Int(100);
console.log(i);

const n = new Int(100.5);
console.log(n);
```

# String Concatenation
```js
let x=10, y=20, z="30";
let result1 = x + y + z; // 3030
let result2 = x + y - z; // 0
```

# Special Number
`NaN`: Not a number
`Infinity` (or `-Infinity`): Infinity

# Methods
```js
let x = 12.3;  
let text = x.toString(2); // 1100.010011001100110011001100110011001100110011001101

let num1 = x.toExponential(4) // 1.2300e+1
let num2 = x.toFixed(0) // 12
let num3 = x.toPrecision(4) // 12.30

parseInt("10.33");  // 10
parseInt("10 20 30");  // 10
parseInt("years 10"); // 10
parseFloat("10.33");  // 10.33

Number.isInteger(10); // true
Number.isFinite(Infinity); // false
Number.isNaN(NaN) // true
Number.isSafeInteger(12345678901234567890) // false

Number.parseFloat()
Number.parseInt()
```

# Properties
```js
let x = Number.EPSILON; // The difference between the smallest floating point number greater than 1 and 1

let x = Number.MAX_VALUE;
let x = Number.MIN_VALUE;
let x = Number.MIN_SAFE_INTEGER;
let x = Number.MAX_SAFE_INTEGER;

let x = Number.POSITIVE_INFINITY;
let x = Number.NEGATIVE_INFINITY;
let x = Number.NaN;
```

# BigInt
JS integers are only accurate up to 15 digits:

```js
let x = 1234567890123456789012345n;  
let y = BigInt(1234567890123456789012345)
```

- Operators that can be used on a JS `Number` can also be used on a `BigInt`.
- Can not have decimals.
- Can also be written in hexadecimal, octal, or binary notation.
- Rounding can compromise program security.

# Bitwise

| Operator | Name                  | Description                                                                                              |
| -------- | --------------------- | -------------------------------------------------------------------------------------------------------- |
| &        | AND                   | Sets each bit to 1 if both bits are 1                                                                    |
| \|       | OR                    | Sets each bit to 1 if one of two bits is 1                                                               |
| ^        | XOR                   | Sets each bit to 1 if only one of two bits is 1                                                          |
| ~        | NOT                   | Inverts all the bits                                                                                     |
| <<       | Zero fill left shift  | Shifts left by pushing zeros in from the right and let the leftmost bits fall off                        |
| >>       | Signed right shift    | Shifts right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |
| >>>      | Zero fill right shift | Shifts right by pushing zeros in from the left, and let the rightmost bits fall off                      |

| Operator | Example  | Same As     |
| -------- | -------- | ----------- |
| <<=      | x <<= y  | x = x << y  |
| >>=      | x >>= y  | x = x >> y  |
| >>>=     | x >>>= y | x = x >>> y |

| Operator | Example | Same As    |
| -------- | ------- | ---------- |
| &=       | x &= y  | x = x & y  |
| ^=       | x ^= y  | x = x ^ y  |
| \|=      | x \|= y | x = x \| y |
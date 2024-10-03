# JavaScript

---

## **JavaScript Data Types & Variables**

JavaScript supports various data types that are essential for effective programming. These data types are mainly divided into two categories: **Primitive** and **Non-Primitive** (or Reference) types.

### **Primitive Data Types**
Primitive data types are the simplest forms of data in JavaScript. They are **immutable**, meaning that their values cannot be changed after they are created.

JavaScript defines seven primitive types:

1. **String**: Represents textual data.
   - Example: `"Hello World"`
   
2. **Number**: Represents numeric values (both integers and floating-point numbers).
   - Example: `42`, `3.14`
   
3. **BigInt**: Represents large integers with arbitrary precision.
   - Example: `1234567890123456789012345678901234567890n`
   
4. **Boolean**: Represents logical values: `true` or `false`.
   - Example: `true`, `false`
   
5. **Undefined**: Represents a variable that has been declared but not yet assigned a value.
   - Example: `let x; // x is undefined`
   
6. **Null**: Represents the intentional absence of any object value.
   - Example: `let y = null; // y is null`
   
7. **Symbol**: Represents a unique and immutable identifier.
   - Example: `let sym = Symbol('unique');`

**Characteristics of Primitive Data Types**:
- **Immutable**: Once created, the value cannot be changed.
- **Stored by Value**: When you assign a primitive to another variable, a copy of the value is made.
- **Memory**: Allocated on the **stack**, which is faster and more efficient for smaller data.

---

### **Non-Primitive Data Types (Reference Types)**

Non-primitive types, also known as **reference types**, can hold collections of values or complex data structures. These types are **mutable**, meaning their contents can be changed.

Common non-primitive types include:

1. **Object**: Represents a collection of key-value pairs.
   - Example: `let person = { name: "John", age: 30 };`

2. **Array**: Represents an ordered list of values (can be mixed types).
   - Example: `let arr = [1, "apple", true];`

3. **Function**: Represents a block of code that can be invoked or executed.
   - Example: `function greet() { console.log("Hello!"); }`

4. **Date**: Represents dates and times.
   - Example: `let now = new Date();`

5. **RegExp**: Represents regular expressions used for pattern matching in strings.
   - Example: `let regex = /abc/;`

**Characteristics of Non-Primitive Data Types**:
- **Mutable**: The contents can be modified.
- **Stored by Reference**: When you assign a non-primitive type to another variable, it points to the same reference in memory.
- **Memory**: Allocated on the **heap**, which is used for dynamic memory allocation.

---

### **Key Differences Between Primitive & Non-Primitive Data Types**

| Feature                  | **Primitive**                            | **Non-Primitive**                       |
|--------------------------|------------------------------------------|-----------------------------------------|
| **Mutability**            | Immutable                                | Mutable                                 |
| **Storage**               | Stored by value (directly in the stack)  | Stored by reference (in the heap)       |
| **Copying**               | Creates a new copy                       | Copies a reference to the same object   |
| **Memory Allocation**     | Allocated on the stack                   | Allocated on the heap                   |

---

### **Detailed Comparison: Primitive vs Non-Primitive**

1. **Mutability**:
   - **Primitive**: Values cannot be changed after creation (immutable).
   - **Non-Primitive**: Values can be modified (mutable).

2. **Storage**:
   - **Primitive**: Data is stored by value, meaning each variable holds its own copy of the data.
   - **Non-Primitive**: Data is stored by reference, meaning multiple variables can point to the same object.

3. **Copying**:
   - **Primitive**: Copying a primitive type creates an independent new value.
   - **Non-Primitive**: Copying a reference type creates a new reference to the same object or array, not a separate copy.

4. **Memory Allocation**:
   - **Primitive**: Stored on the stack, which is faster and more efficient for small, fixed-size data.
   - **Non-Primitive**: Stored on the heap, which is suitable for dynamic, variable-size data.

---

### **Summary:**

- **Primitive Data Types**: 
  - Examples: `String`, `Number`, `Boolean`, etc.
  - Characteristics: Immutable, stored by value, allocated on the stack.

- **Non-Primitive Data Types**:
  - Examples: `Object`, `Array`, `Function`, etc.
  - Characteristics: Mutable, stored by reference, allocated on the heap.

---

This guide provides a clear understanding of the different types of data in JavaScript and their respective characteristics. Knowing when to use primitive versus non-primitive types is key to writing efficient and bug-free JavaScript code.

--- 

### Operators and Expressions in JavaScript

In JavaScript, **operators** are symbols that perform operations on values (called operands) to produce a result. An **expression** is a piece of code that combines variables, operators, and values, which can be evaluated to produce a value.

For example, in the expression `5 + 3`, the `+` is an operator, and `5` and `3` are operands. When the expression is evaluated, it produces the result `8`.

Let’s go through different types of operators and how they are used.

---

#### 1. **Arithmetic Operators**
These operators are used to perform basic arithmetic operations like addition, subtraction, multiplication, etc.

| Operator | Name          | Example          | Explanation                                |
|----------|---------------|------------------|--------------------------------------------|
| `+`      | Addition       | `5 + 3`          | Adds two numbers, result is `8`.           |
| `-`      | Subtraction    | `10 - 6`         | Subtracts the second number, result is `4`.|
| `*`      | Multiplication | `4 * 2`          | Multiplies two numbers, result is `8`.     |
| `/`      | Division       | `10 / 2`         | Divides the first number by the second, result is `5`. |
| `%`      | Modulus        | `10 % 3`         | Gives the remainder of division, result is `1` (because `10 ÷ 3` leaves a remainder of `1`).|
| `**`     | Exponentiation | `2 ** 3`         | Raises the first number to the power of the second, result is `8` (because `2^3 = 8`). |

---

#### 2. **Assignment Operators**
These operators assign values to variables.

| Operator | Name           | Example         | Explanation                                |
|----------|----------------|-----------------|--------------------------------------------|
| `=`      | Assignment      | `let x = 10`    | Assigns the value `10` to the variable `x`.|
| `+=`     | Addition Assignment | `x += 5`   | Adds `5` to `x` (equivalent to `x = x + 5`), result is `15` if `x` was `10`. |
| `-=`     | Subtraction Assignment | `x -= 2`| Subtracts `2` from `x` (equivalent to `x = x - 2`), result is `8` if `x` was `10`. |
| `*=`     | Multiplication Assignment | `x *= 2` | Multiplies `x` by `2`, result is `20` if `x` was `10`.|
| `/=`     | Division Assignment | `x /= 2`   | Divides `x` by `2`, result is `5` if `x` was `10`. |
| `%=`     | Modulus Assignment | `x %= 3`    | Stores the remainder of `x ÷ 3`, result is `1` if `x` was `10`. |

---

#### 3. **Comparison Operators**
These operators compare two values and return a boolean (`true` or `false`) based on the comparison.

| Operator | Name            | Example           | Explanation                                |
|----------|-----------------|-------------------|--------------------------------------------|
| `==`     | Equal to         | `5 == '5'`        | Returns `true` if values are equal, even if types differ (loose equality). |
| `===`    | Strict Equal to  | `5 === '5'`       | Returns `false` because values are equal but types differ (strict equality). |
| `!=`     | Not equal to     | `5 != '6'`        | Returns `true` because the values are not equal. |
| `!==`    | Strict Not equal to | `5 !== '5'`    | Returns `true` because values or types are not equal. |
| `>`      | Greater than     | `7 > 5`           | Returns `true` because `7` is greater than `5`. |
| `<`      | Less than        | `3 < 5`           | Returns `true` because `3` is less than `5`. |
| `>=`     | Greater than or equal to | `5 >= 5` | Returns `true` because `5` is equal to `5`. |
| `<=`     | Less than or equal to | `4 <= 5`     | Returns `true` because `4` is less than `5`. |

---

#### 4. **Logical Operators**
These operators combine multiple conditions and return `true` or `false` based on the logic.

| Operator | Name       | Example                 | Explanation                                    |
|----------|------------|-------------------------|------------------------------------------------|
| `&&`     | AND        | `x > 5 && y < 10`       | Returns `true` if both conditions are true. |
| `||`     | OR         | `x > 5 || y < 10`       | Returns `true` if at least one condition is true. |
| `!`      | NOT        | `!(x === 5)`            | Returns `true` if the condition is false (inverts the result). |

---

#### 5. **Unary Operators**
Unary operators work with only one operand.

| Operator | Name        | Example          | Explanation                                       |
|----------|-------------|------------------|---------------------------------------------------|
| `++`     | Increment   | `let x = 5; x++` | Increases the value of `x` by `1`, result is `6`. |
| `--`     | Decrement   | `let y = 5; y--` | Decreases the value of `y` by `1`, result is `4`. |
| `typeof` | Type        | `typeof 42`      | Returns the data type of the operand, result is `'number'`. |
| `delete` | Delete      | `delete obj.prop`| Deletes a property from an object. |

---

#### 6. **Ternary (Conditional) Operator**
The ternary operator is a shorthand way to write conditional statements. It works with three operands.

Syntax:
```javascript
condition ? expressionIfTrue : expressionIfFalse;
```

Example:
```javascript
let age = 18;
let canVote = age >= 18 ? 'Yes' : 'No';
console.log(canVote); // Output: Yes
```

---

#### 7. **Bitwise Operators**
These operators work on binary numbers (bit-level). They are useful in situations where you need to manipulate bits directly.

| Operator | Name       | Example           | Explanation                                      |
|----------|------------|-------------------|--------------------------------------------------|
| `&`      | AND        | `5 & 1`           | Compares each bit of two numbers, result is `1`.  |
| `|`      | OR         | `5 | 1`           | Compares each bit of two numbers, result is `5`.  |
| `^`      | XOR        | `5 ^ 1`           | Compares each bit, result is `4`.                 |
| `~`      | NOT        | `~5`              | Inverts all bits, result is `-6`.                 |
| `<<`     | Left Shift | `5 << 1`          | Shifts bits to the left, result is `10`.          |
| `>>`     | Right Shift| `5 >> 1`          | Shifts bits to the right, result is `2`.          |

---

### Expressions

An **expression** is a valid set of literals, variables, operators, and function calls that JavaScript can evaluate to produce a value.

- **Arithmetic Expression**: Combines arithmetic operators and values to compute a result.
  ```javascript
  let sum = 5 + 3;  // Evaluates to 8
  ```

- **Comparison Expression**: Compares values and produces a boolean (`true` or `false`).
  ```javascript
  let isEqual = (5 === 5);  // Evaluates to true
  ```

- **Logical Expression**: Combines multiple conditions.
  ```javascript
  let isAdult = age > 18 && hasID;  // Both conditions must be true
  ```

- **Function Call Expression**: Calls a function and evaluates its result.
  ```javascript
  let greeting = sayHello();  // Evaluates to the result of the function
  ```

--- 

This is a detailed breakdown of JavaScript operators and expressions. Let me know if you'd like to dive deeper into any specific topic!

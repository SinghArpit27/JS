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

Let me know if you'd like to add more sections or examples!

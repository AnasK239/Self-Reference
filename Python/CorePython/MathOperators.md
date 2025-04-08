## 1. Arithmetic Operators

- **Addition (`+`)**  
  Adds two operands.  
  *Example:* `a + b` adds the value of `b` to `a`.
--
- **Subtraction (`-`)**  
  Subtracts the right operand from the left operand.  
  *Example:* `a - b` gives the difference between `a` and `b`.
--
- **Multiplication (`*`)**  
  Multiplies two operands.  
  *Example:* `a * b` produces the product of `a` and `b`.
--
- **Division (`/`)**  
  Divides the left operand by the right operand and always returns a floating-point result (even if the result is a whole number).  
  *Example:* `a / b` computes the division of `a` by `b`.
--
- **Floor Division (`//`)**  
  Divides and returns the largest whole number less than or equal to the quotient (i.e., it “rounds down”).  
  *Example:* `a // b` calculates the integer quotient of `a` divided by `b`.
--
- **Modulus (`%`)**  
  Returns the remainder of the division between the left and right operands.  
  *Example:* `a % b` yields the remainder when `a` is divided by `b`.
--
- **Exponentiation (`**`)**  
  Raises the left operand to the power of the right operand.  
  *Example:* `a ** b` means *a* raised to the power of *b*.
--
---

## 2. Bitwise Operators

Bitwise operators treat their operands as a sequence of binary bits. They are often used for low-level programming tasks, such as bit manipulation.

- **Bitwise AND (`&`)**  
  Compares each bit of its first operand to the corresponding bit of its second operand. The result in each position is 1 if both bits are 1; otherwise, it is 0.  
  *Example:* `a & b`
--
- **Bitwise OR (`|`)**  
  Compares each bit of its operands and returns 1 if any corresponding bit is 1.  
  *Example:* `a | b`
--
- **Bitwise XOR (`^`)**  
  Compares each bit of its operands. The result in each bit position is 1 if only one of the bits is 1, but not both.  
  *Example:* `a ^ b`
--
- **Bitwise NOT (`~`)**  
  Inverts all the bits of the operand (also known as bitwise complement).  
  *Example:* `~a` produces the complement of `a`.
--
- **Left Shift (`<<`)**  
  Shifts the bits of the first operand to the left by the number of positions specified by the second operand.  
  *Example:* `a << b` shifts `a`’s bits to the left by `b` positions.
--
- **Right Shift (`>>`)**  
  Shifts the bits of the first operand to the right by the number of positions specified by the second operand.  
  *Example:* `a >> b` shifts `a`’s bits to the right by `b` positions.
--
---

## 3. Compound Assignment Operators

These operators combine an arithmetic (or bitwise) operation with assignment. They provide a shorthand for updating the value of a variable.

- **Addition Assignment (`+=`)**  
  Equivalent to `a = a + b`.
--
- **Subtraction Assignment (`-=`)**  
  Equivalent to `a = a - b`.
--
- **Multiplication Assignment (`*=`)**  
  Equivalent to `a = a * b`.
--
- **Division Assignment (`/=`)**  
  Equivalent to `a = a / b`.
--
- **Floor Division Assignment (`//=`)**  
  Equivalent to `a = a // b`.
--
- **Modulus Assignment (`%=`)**  
  Equivalent to `a = a % b`.
--
- **Exponentiation Assignment (`**=`)**  
  Equivalent to `a = a ** b`.
--
- **Bitwise AND Assignment (`&=`)**  
  Equivalent to `a = a & b`.
--
- **Bitwise OR Assignment (`|=`)**  
  Equivalent to `a = a | b`.
--
- **Bitwise XOR Assignment (`^=`)**  
  Equivalent to `a = a ^ b`.
--
- **Left Shift Assignment (`<<=`)**  
  Equivalent to `a = a << b`.
--
- **Right Shift Assignment (`>>=`)**  
  Equivalent to `a = a >> b`.
--
---
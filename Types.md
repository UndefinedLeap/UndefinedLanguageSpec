# Numbers in general

- Operators:
	- Addition, substraction, multiplication, division.
	- power-of, can be built-in function.

# Int

Integer of specific size and signedness
- u8: Unsigned 8-bit integer
- u16: Unsigned 16-bit integer
- u32: Unsigned 32-bit integer
- u64: Unsigned 64-bit integer

- i8: Signed 8-bit integer
- i16: Signed 16-bit integer
- i32: Signed 32-bit integer
- i64: Signed 64-bit integer

- Integers can only be implictly cast, if it doesn't produce bugs like integer over-flow.
	1. Conversion rule for implict casts:
		- Same-signedness integer can be promoted to bigger sized integers.
	2. Conversion rule for explict casts (built-in feature):
		- Integer size demotion:
			a. Truncate: Truncate bits on either size
			b. Max: Get maximum value that new integer size fits. (u16 = 500 -> u8 = 255)
		- Signedness change:
			a. uhhhhhhhh
		- Singedness change and demotion:
			a. uhhhhhhhhhhhhhhhhhhhhh
			
- Bit shift:
	1. Logical left-right shift on unsigned integers.
	2. I don't see any point in bit shifting on signed integers.
		- I don't see any point in arithmetic right shift.
		- Need good example to include bit-shifting on signed integers or arithmetic right shift, until then we exclude it.
		
- Integer division truncates, eg: 5/2 = 2.

# Float

Following IEEE 754 standard.

Two float type:
- float: 32-bit floating point number.
- double: 64-bit floating point number.

- Conversion rules:
	1. Float to integer converstion, both will be in-built functions:
		- Truncate
		- Round-off
	2. Promotion no problem, demotion:
		- uhhhhhhhhhhhhh

# String/Array-of-char

# Array

# Expression evaluation order

- If expression evaluation order is specified, that is, precedence order or bracket grouping, it will be evaluated in left to right order.
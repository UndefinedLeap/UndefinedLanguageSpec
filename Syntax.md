# Syntax

## Variable and constant declaration

```
var x: u8 = 10;
const y: i32 = 122222;
```
- Variable is mutable and can be changed.
- Constant is immutable and can be comptime (Seperate immutable and comptime variable?)

## Array

```
var x: []u8 = {2, 3, 4};
var x: [3]u8 = {};
```
- Array size can be infered if the size is not provided.
- If Array size is provided but it is empty (line 2), it will be filled with undefined value.

## Struct

```
Struct Vec3{
	x: float,
	y: float,
	z: float,
}
```
or
```
var laal: Struct{
	x: float,
	y: u32,
} = .{.x = 3.14, .y = 15555};
```
- First example is struct declared with name `Vec3`, with it fields `x`, `y` and `z`.
- Second example is anonymous struct, with fields `x` and `y`.
- Struct can be accessed with `.` notation, eg: `laal.x`.
- Struct can be assiged with c-like notation, eg: `.{.x = 3.14, .y = 15555}`

## Branchs

```
if a > 5 and !(b < 10){
	// blah blah
}
```
- No need for brackets.
- Boolean operations such as `and`, `or`, `xor`, will be word instead of `&&`, `||`, etc. Except for `not` operation, it will use `!`.

## Functions
```
fn foo(x: float) float {
	return x;
}
```
- Function take x of type float as parameter and return float.
- Can be called with: `foo(0.69);`

## Comments
```
// Single line comment.
```
- Dunno if multi-line comment is necessary, for anything beside documentation.

## Bit shifts
- Nothing special, `>>` for right shift, `<<` for left shift.

## Binary operators
- Left shift and assign: `=<<`
- Right shift and assign: `=>>`
- Add and assign: `+=`
- Sub and assign: `-=`
- Multiply and assign: `*=`
- Division and assign: `/=`

## Trinary operator
- if x, then y else z: `x ? y : z`
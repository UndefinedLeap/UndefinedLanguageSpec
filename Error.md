# Error

Just like zig, we have error set, which is basically enum, but enforced by compiler.

Function can return and error set and a value, though unlike traditional enum, it will be enforced by compiler to handle the function return value.

```
// An error set of name 'SomeError'
Error SomeError{
	IndexOutOfBound, UseAfterFree, DivideByZero
};
```

We would use `!` as binary operator that tell if function return a error or value.
```
fn foo(a: f32) SomeError!f32 {
	if a == 0 {
		return SomeError.DivideByZero;
	}
	return a;
}
```

It can be catched with `catch`
```
foo(0) catch |err| {
// Handle the err.
}
```

Note: Whether to catch error by `catch` or something else is not yet discussed and to use pipe `|` notation is also not discussed.
% Embyr Technologies Go Style Guide
% Matthew Cooper Healy
% 8 April 2018

## Use `gofmt`
Either follow the syle accepted by `gofmt` or run `gofmt` prior to pushing
any code.

## Comments
Comments will follow the Google standard, notably that comments are
primarily used inline, rather than in blocks, and are preceeded by exactly
one space if on the same line as a line of code.

### Example:
```go
main() int {
	fmt.PrintLn("Hello, World") // prints "Hello, World" to the console
	return 0;
}
```

#### Note: this is a living document and should be checked regularly for updates.
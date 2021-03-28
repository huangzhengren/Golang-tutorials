# Output

## Output

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello Golang")
	fmt.Print("Hello Golang")
	fmt.Printf("Hello Golang")

	fmt.Print("a", "b", "c")
	fmt.Println("a", "\n", "b", "c")
	fmt.Printf("a b c")

	var a = 1
	var b = 2
	var c = 3

	fmt.Printf("a=%v, b=%v, c=%v\n", a, b, c)

}

```

## Focus

* Fmt.Println will output a newline, fmt.Printf will format the output, and fmt.Print will not output a newline.

* When outputting multiple values at the same time, fmt.Println will output a space between each value, and finally a newline will be output, while fmt.Print will not output spaces and newlines.

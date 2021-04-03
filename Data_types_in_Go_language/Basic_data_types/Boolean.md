[TOC]



# Boolean

## Boolean

```go
package main

import (
	"fmt"
)

func main() {
	var flag bool = true
	fmt.Printf("%v,%T\n", flag, flag)

	var flag1 = false
	fmt.Printf("%v,%T\n", flag1, flag1)

	var flag2 bool
	fmt.Printf("%v,%T\n", flag2, flag2)

}

```

## Focus

* Boolean default value is false.
* In Go language, Boolean type and other types cannot be converted to each other.
* In Go language, Boolean cannot participate in numerical operations.

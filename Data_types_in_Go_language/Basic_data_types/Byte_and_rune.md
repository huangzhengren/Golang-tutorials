[TOC]



# Byte and rune

## Byte and rune

```go
package main

import (
	"fmt"
)

func main() {

	var a = 'a'
	fmt.Printf("%v,%c,%T\n", a, a, a)

	var b = 'a'
	fmt.Printf("%c,%T\n", b, b)

	c := "This is qiqi"
	fmt.Printf("%v,%c,%T\n", c[1], c[1], c[1]) // 104,h,uint8

	var d string = "hello"
	fmt.Println(len(d))

	e := "琪 琪"
	fmt.Println(len(e))

	var f = '琪'
	fmt.Printf("%v,%T\n", f, f) //Unicode编码十进制：29738,int32

}

```


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

	str := "hello 琪琪"
	for i := 0; i < len(str); i++ {
		fmt.Printf("%v,%c\n", str[i], str[i]) // byte
	}

	for _, v := range str {
		fmt.Printf("%v,%c\n", v, v)
	}

	var str1 = "nihao xiaobudianer"
	var str2 string = "hello 小不点儿"

	strByte := []byte(str1)
	strByte[0] = 'q'
	fmt.Println(string(strByte))

	strRune := []rune(str2)
	strRune[0] = '琪'
	fmt.Println(string(strRune))

}

```


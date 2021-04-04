# String

## Go language escape characters

| escape characters |   description    |
| :---------------: | :--------------: |
|        \t         | 横向制表符(\x09) |
|        \n         |   换行符(\x0A)   |
|        \v         | 纵向制表符(\x0B) |
|        \f         |   换页符(\x0C)   |
|        \r         |   回车符(\x0D)   |
|        \\^        |        ^         |
|        \\$        |        $         |
|        \\.        |        .         |
|        \\*        |        *         |
|        \\+        |        +         |
|        \\?        |        ?         |
|        \\{        |        {         |
|        \\}        |        }         |
|        \\(        |        (         |
|        \\)        |        )         |
|        \\[        |        [         |
|        \\]        |        ]         |
|        \\|        |        \|        |



## String

```go
package main

import (
	"fmt"
	"strings"
)

func main() {
	var str1 string = "你好琪琪"
	var str2 = "你好小不点儿"
	str3 := "你好qiqi"

	fmt.Printf("%v, %T\n", str1, str1)
	fmt.Printf("%v, %T\n", str2, str2)
	fmt.Printf("%v, %T\n", str3, str3)

	// Single-line string
	str4 := "D:\\Golang-turorials\\Golang-tutorials"
	fmt.Printf("%v\n", str4)

	// Multi-line string
	str5 := `
	qiqi
	琪琪
	小不点儿
	`
	fmt.Printf("%v\n", str5)

	var str6 = "琪琪"
	fmt.Println(len(str6))

	var str7 string = "qiqi"
	fmt.Println(len(str7))

	str8 := "你好"
	var str9 = "qiqi"
	var str10 string = str8 + str9
	fmt.Println(str8 + str9)
	fmt.Println(str10)

	str11 := "你好"
	str12 := "小不点儿"
	str13 := fmt.Sprintf("%v %v", str11, str12)
	fmt.Println(str13)

	str14 := "你好" +
		"琪琪"
	fmt.Println(str14)

	// strings.Split return slice
	str15 := "你好-琪琪"
	arr15 := strings.Split(str15, "-") // 返回切片
	fmt.Println(arr15)
	fmt.Println(strings.Join(arr15, "qiqi"))

	// strings.Join return string
	arr16 := []string{"123", "456", "789"}
	str16 := strings.Join(arr16, "qq")
	fmt.Println(str16)

	// strings.Contains return Boolean
	str17 := "this is qiqi"
	str18 := "this"
	str19 := strings.Contains(str17, str18)
	fmt.Printf("%v,%T\n", str19, str19)

	// string.HasPrefix,strings.HasSuffix
	str20 := "this is qiqi"
	str21 := "qiqi"
	res := strings.HasPrefix(str20, str21)
	fmt.Printf("%v,%T\n", res, res)
	res1 := strings.HasSuffix(str20, str21)
	fmt.Printf("%v,%T\n", res1, res1)

	// strings.Index strings.LastIndex
	str22 := "this  is qiqi"
	str23 := "s"
	pos := strings.Index(str22, str23)
	fmt.Printf("%v,%T\n", pos, pos)
	pos1 := strings.LastIndex(str22, str23)
	fmt.Printf("%v,%T\n", pos1, pos1)
	str24 := "ss"
	pos2 := strings.Index(str22, str24) // return -1 if not found
	fmt.Printf("%v,%T\n", pos2, pos2)

}

```



## Common methods of strings package

|                   method                   |                         description                          |
| :----------------------------------------: | :----------------------------------------------------------: |
|    strings.Split(s string, sep string)     | 用去掉s中出现的sep的方式进行分割，会分割到结尾，并返回生成的所有片段组成的切片（每一个sep都会进行一次切割，即使两个sep相邻，也会进行两次切割）。如果sep为空字符，Split会将s切分成每一个unicode码值一个字符串。 |
|  strings.Join(elems []string, sep string)  |       将一系列字符串连接为一个字符串，之间用sep来分隔        |
| strings.Contains(s string, substr string)  |                判断字符串s是否包含子串substr                 |
| strings.HasPrefix(s string, prefix string) |                判断s是否有前缀字符串prefix。                 |
| strings.HasSuffix(s string, suffix string) |                判断s是否有后缀字符串suffix。                 |
|   strings.Index(s string, substr string)   |     子串sep在字符串s中第一次出现的位置，不存在则返回-1。     |
| strings.LastIndex(s string, substr string) |    子串sep在字符串s中最后一次出现的位置，不存在则返回-1。    |


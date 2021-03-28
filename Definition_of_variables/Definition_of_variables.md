[TOC]



# Definition of variables

## Variable

```go
package main

import "fmt"

func main() {

	/*
		var variable_name type
		variable_name = value
	*/
	var qiqi string

	qiqi = "琪琪"

	fmt.Println(qiqi)

	// var variable_name = value
	var dahuang = "大黄"

	fmt.Println(dahuang)

	// var variable_name type = value
	var wsq string = "小不点儿"

	fmt.Println(wsq)

	/*
		var variable_name1, variable_name2, type
		variable_name1 = value1
		variable_name2 = value2
	*/
	var ren, qi string

	ren = "他"
	qi = "她"

	fmt.Println(ren, qi)

	/*
		var (
			variable_name1 type1
			variable_name2 type2
			variable_name3 type3
		)

		variable_name1 = value1
		variable_name2 = value2
		variable_name3 = value3
	*/
	var (
		zheng string
		shu   string
		age   int
	)

	zheng = "政"
	shu = "姝"
	age = 24

	fmt.Println(zheng, shu, age)

	/*
		var (
			variable_name1 = value1
			variable_name2 = value2
		)
	*/
	var (
		zhengren = "huang"
		shuqi    = "wang"
	)

	fmt.Println(zhengren, shuqi, age)

	/*
		var (
				variable_name1 type1 = value1
				variable_name2 type2 = value2
			)
	*/
	var (
		zr string = "zr"
		sq string = "sq"
	)

	fmt.Println(zr, sq)

}

```

## Short variable

```go
package main

import "fmt"

func main() {

	/*
		variable_name1,variable_name2,variable_name3 := value1, value2,value3
	*/
	a, b, c := 1, 2, 3
	fmt.Println(a, b, c)

	/*
		variable_name1,variable_name2,variable_name3 := value1,value2,value3
	*/
	d, e, f := 52, "qiqi", "77"
	fmt.Println(d, e, f)
	fmt.Printf("d的类型是%T,e的类型是%T,f的类型是%T\n", d, e, f)
    
}

```

## Anonymous variable

```go
package main

import "fmt"

func getUserInfo() (string, int, string) {

	return "xiaobudianer", 24, "岁月依稀残梦里"

}

func main() {
    
	/*
		_ Represents anonymous variables
	*/
	var username, _, he = getUserInfo()
	fmt.Println(username, he)

}

```

# Focus

* Variable names in Go language consist of letters, numbers and underscores.
* The first character cannot be a number.
* Go language is case sensitive.
* Keywords and reserved words of Go language cannot be used as variable names.
* Variables cannot be declared repeatedly in the same scope in Go language.
* When the Go language short variable declaration method declares multiple variables and assigns them, the types of the variables can be inconsistent.
* The short variable declaration method of Go language can only be used to declare local variables.
* Anonymous variables do not occupy the namespace and do not allocate memory, so there is no duplicate declaration between anonymous variables.

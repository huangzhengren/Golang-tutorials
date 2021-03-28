[TOC]



# Definition_of_constants

## Constants

```go
package main

import "fmt"

func main() {

	// const constant_name = value
	const QIQI = "琪琪"

	fmt.Println(QIQI)

	/*
		const (
			constant_name1 = value1
			constant_name2 = value2
		)
	*/
	const (
		zrhuang = "zrhuang"
		qiqi    = "qiqi"
	)

	fmt.Println(zrhuang, qiqi)

	/*
		const (
			variable_name1 = value1
			variable_name2
			variable_name3 = value3
			variable_name4
			variable_name5
		)
	*/
	const (
		a = 100
		b
		c = "琪琪"
		d
		e
	)

	fmt.Println(a, b, c, d, e)

	/*
		const (
			variable_name1 type = value1
			variable_name2
			variable_name3 type = value3
			variable_name4
			variable_name5
		)
	*/
	const (
		f int = 100
		g
		h string = "琪琪"
		i
		j
	)

	fmt.Println(f, g, h, i, j)

}

```

## Iota

```
package main

import "fmt"

func main() {

	// const variable_name = iota
	const it = iota
	fmt.Println(it)

	/*
		const (
			variable_name1 = iota
			variable_name2
		)
	*/
	const (
		s = iota
		t
	)

	fmt.Println(s, t)

	/*
		const (
			variable_name1 = iota
			variable_name2 = value2
			variable_name3
			variable_name4 = iota
			_
			variable_name4
		)
	*/
	const (
		m = iota
		n = 100
		o
		p = iota
		_
		r
	)

	fmt.Println(m, n, o, p, r)

	/*
		const (
			variable_name1,variable_name2 = iota + value1, iota + value2
			variable_name3,variable_name4
			variable_name5,variable_name6
		)
	*/
	const (
		u, v = iota + 1, iota + 3
		w, x
		y, z
	)

	fmt.Println(u, v)
	fmt.Println(w, x)
	fmt.Println(y, z)

}

```

# Focus

* Constants must be assigned at the same time as they are defined.
* The value of the constant cannot be changed.
* Iota is a constant counter in the Go language and can only be used in constant expressions.
* Every time const appears, iota will be initialized to 0.
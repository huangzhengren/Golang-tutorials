# Float

## Float comparison table

|  type   |                      range                       | Occupied size |
| :-----: | :----------------------------------------------: | :-----------: |
| float32 |  -3.4028234663852886e+38~3.4028234663852886e+38  |       4       |
| float64 | -1.7976931348623157e+308~1.7976931348623157e+308 |       8       |

## Float

```go
package main

import (
	"fmt"
	"unsafe"

	"github.com/shopspring/decimal"
)

func main() {

	var qiqi float32 = 3.1415926
	fmt.Printf("%v, %f, %T,%.2f,%2f\n", qiqi, qiqi, qiqi, qiqi, qiqi)
	fmt.Println(unsafe.Sizeof(qiqi))

	var xiaobudianer float64 = 3.14e2
	fmt.Printf("%v,%f,%T\n", xiaobudianer, xiaobudianer, xiaobudianer)
	fmt.Println(unsafe.Sizeof(xiaobudianer))

	var qq float32 = 3.14e-2
	fmt.Printf("%v,%f,%T\n", qq, qq, qq)
	fmt.Println(unsafe.Sizeof(qq))

	//Loss of accuracy
	var a1 = 277.1
	fmt.Println(a1 * 100) //27710.000000000004

	a3 := 9.2
	a4 := 3.9
	fmt.Println(a3 - a4) //5.299999999999999

	// Solution
	// Addition
	a5 := 9.2
	a6 := 3.9
	res := decimal.NewFromFloat(a5).Add(decimal.NewFromFloat(a6))
	fmt.Println(res)

	// Subtraction
	a7 := 9.2
	a8 := 3.9
	res2 := decimal.NewFromFloat(a7).Sub(decimal.NewFromFloat(a8))
	fmt.Println(res2)

	// Multiplication
	a9 := 9.2
	a10 := 3.9
	res3 := decimal.NewFromFloat(a9).Mul(decimal.NewFromFloat(a10))
	fmt.Println(res3)

	// Division
	a11 := 9.2
	a12 := 3.9
	res4 := decimal.NewFromFloat(a11).Div(decimal.NewFromFloat(a12))
	fmt.Println(res4)

	var b1 float32 = 23.45
	var b2 int = int(b1)
	fmt.Printf("%v,%T\n", b1, b1)
	fmt.Printf("%v,%T\n", b2, b2)

}

```

## Focus

* The package "github.com/shopspring/decimal" can be used for floating point calculations
* Direct addition, subtraction, multiplication and division of floating-point numbers may cause loss of precision

## Common_Go_commands

```shell
[root@app01 software]# go mod init Go_WorkSpace
```

```shell
[root@app01 software]# go get "github.com/shopspring/decimal"
```
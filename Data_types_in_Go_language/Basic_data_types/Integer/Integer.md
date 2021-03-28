[TOC]



# Integer

## Integer comparison table

|  type  |                            range                             | Occupied size | With or without symbols |
| :----: | :----------------------------------------------------------: | :-----------: | :---------------------: |
|  int8  |               (-128 to 127)     -2^7 to 2^7-1                |    1 byte     |          with           |
| int16  |             (-32768 to 32767)    -2^15 to 2^15-1             |    2 bytes    |          with           |
| int32  |        (-2147483648 to 2147483647)    -2^31 to 2^31-1        |    4 bytes    |          with           |
| int64  | (-9223372036854775808 to 9223372036854775807)    -2^63 to 2^63-1 |    8 bytes    |          with           |
| uint8  |                   (0 to 255)    0 to 2^8-1                   |    1 byte     |         without         |
| uint16 |                 (0 to 65535)    0 to 2^16-1                  |    2 bytes    |         without         |
| uint32 |                (0 to 4294967295) 0 to 2^32-1                 |    4 bytes    |         without         |
| uint64 |          (0 to 18446744073709551615)    0 to 2^64-1          |    8 byte     |         without         |

## Integer

```go
package main

import (
	"fmt"
	"unsafe"
)

func main() {

	// int8
	var num1 int8 = -128
	fmt.Printf("num1=%v, type=%T\n", num1, num1)
	fmt.Println(unsafe.Sizeof(num1))

	// int16
	var num2 int16 = -32768
	fmt.Printf("num2=%v, type=%T\n", num2, num2)
	fmt.Println(unsafe.Sizeof(num2))

	// int32
	var num3 int32 = -2147483648
	fmt.Printf("num3=%v, type=%T\n", num3, num3)
	fmt.Println(unsafe.Sizeof(num3))

	// int64
	var num4 int64 = -9223372036854775808
	fmt.Printf("num4=%v, type=%T\n", num4, num4)
	fmt.Println(unsafe.Sizeof(num4))

	// uint8
	var num5 uint8 = 255
	fmt.Printf("num5=%v, type=%T\n", num5, num5)
	fmt.Println(unsafe.Sizeof(num5))

	// uint16
	var num6 uint16 = 65535
	fmt.Printf("num6=%v, type=%T\n", num6, num6)
	fmt.Println(unsafe.Sizeof(num6))

	// uint32
	var num7 uint32 = 4294967295
	fmt.Printf("num7=%v, type=%T\n", num7, num7)
	fmt.Println(unsafe.Sizeof(num7))

	// uint64
	var num8 uint64 = 18446744073709551615
	fmt.Printf("num8=%v, type=%T\n", num8, num8)
	fmt.Println(unsafe.Sizeof(num8))

}

```

## Special integer

```go
package main

import (
	"fmt"
	"unsafe"
)

func main() {

	// int
	var num9 int = 9223372036854775807
	fmt.Printf("num9=%v, type=%T\n", num9, num9)
	fmt.Println(unsafe.Sizeof(num9))

	// uint
	var num10 uint = 18446744073709551615
	fmt.Printf("num10=%v, type=%T\n", num10, num10)
	fmt.Println(unsafe.Sizeof(num10))
	
	// uintptr
	var num11 uintptr = 18446744073709551615
	fmt.Printf("num11=%v, type=%T\n", num11, num11)
	fmt.Println(unsafe.Sizeof(num11))

}

```

## Focus

```mathematica
1 Byte = 8 bits

1KB = 1024 Bytes

1MB = 1024 KB

1GB = 1024 MB

1TB = 1024 GB

1PB = 1024 TB
```

* On a 32-bit operating system, int is int32. On a 64-bit operating system, int is int64.

* On a 32-bit operating system, uint is uint32. On a 64-bit operating system, uint is uint64.

* Uintptr is used to store a pointer.

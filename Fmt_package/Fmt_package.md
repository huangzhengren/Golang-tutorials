[TOC]



# Fmt package

The fmt package implements formatted I/O similar to the C languages printf and scanf. The formatting action ('verb') comes from C but is simpler.

## general

| Placeholder |            description             |
| :---------: | :--------------------------------: |
|     %v      |          值的默认格式表示          |
|     %+v     | 类似%v，但输出结构体时会添加字段名 |
|     %#v     |           值的Go语法表示           |
|     %T      |        值的类型的Go语法表示        |
|     %%      |               百分号               |

## Boolean value

| Placeholder |   description   |
| :---------: | :-------------: |
|     %t      | 单词true或false |

## Integer

| Placeholder | description                                                  |
| ----------- | ------------------------------------------------------------ |
| %b          | 表示为二进制                                                 |
| %c          | 该值对应的Unicode码值                                        |
| %d          | 表示为十进制                                                 |
| %o          | 表示为八进制                                                 |
| %q          | 该值对应的单引号括起来的Go语法字符字面值，必要时会采用安全的转义表示 |
| %x          | 表示为十六进制，使用a-f                                      |
| %X          | 表示为十六进制，使用A-F                                      |
| %U          | 表示为Unicode格式： U+1234，等价于“U+%4X”                    |

## Floating point numbers and complex numbers

| Placeholder |                         description                          |
| :---------: | :----------------------------------------------------------: |
|     %b      | 无小数部分、二进制指数的科学计数法，如-12345678p-78；参见strconv.FormatFloat |
|     %e      |                 科学计数法，如-1234.456e+78                  |
|     %E      |                 科学计数法，如-1234.456E+78                  |
|     %f      |              有小数部分但无指数部分，如123.456               |
|     %F      |                           等价于%f                           |
|     %g      |    根据实际情况采用%e或%f格式（以获得更简洁、准确的输出）    |
|     %G      |    根据实际情况采用%E或%F格式（以获得更简洁、准确的输出）    |

## String and []byte

| Placeholder |                         description                          |
| :---------: | :----------------------------------------------------------: |
|     %s      |                    直接输出字符串或[]byte                    |
|     %q      | 该值对应的双引号括起来的Go语法字符串字面值，必要时会采用安全的转义表示 |
|     %x      |          每个字节用两字符十六进制数表示（使用a-f）           |
|     %X      |          每个字节用两字符十六进制数表示（使用A-F）           |

## Pointer

| Placeholder |          description           |
| :---------: | :----------------------------: |
|     %p      | 表示为十六进制，并加上前导的0x |

## Focus

| Placeholder |    description     |
| :---------: | :----------------: |
|     %f      | 默认宽度，默认精度 |
|     %9f     |  宽度9，默认精度   |
|    %.2f     |  默认宽度，精度2   |
|    %9.2f    |    宽度9，精度2    |
|    %9.f     |    宽度9，精度0    |


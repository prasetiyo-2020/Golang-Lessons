## Konversi Tipe Int
``` golang
package main

import "fmt"

func main() {
	var nilai32 int32 = 100000
	var nilai64 int64 = int64(nilai32)
	var nilai8 int8 = int8(nilai32)

	fmt.Println(nilai32)
	fmt.Println(nilai64)
	fmt.Println(nilai8)
}
```
```
$ go run main.go
> 100000
> 100000
> -96
```

## Konversi Tipe String
``` golang
package main

import "fmt"

func main() {
	var lastName = "Prasetiyo"
	var e byte = lastName[0]
	var eString string = string(e)

	fmt.Println(lastName)
	fmt.Println(eString)
}
```
```
$ go run main.go
> Prasetiyo
> P
```

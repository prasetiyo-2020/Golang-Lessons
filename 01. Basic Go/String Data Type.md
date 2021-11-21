## String Data Type

``` golang
package main

import "fmt"

func main() {
	// Mencetak string
	fmt.Println("Prasetiyo")
	fmt.Println("Prasetiyo sedang belajar Golang")
	fmt.Println("Prasetiyo sedang belajar Golang Web")

	// Mengambil berapa jumlah karakter string
	fmt.Println(len("Prasetiyo"))
	// Mengambil huruf pada index 0 yaitu huruf P dan ditampilkan dalam bentuk byte
	fmt.Println("Prasetiyo sedang belajar Golang"[0])
	// Mengambil huruf pada index 1 yaitu huruf r dan ditampilkan dalam bentuk byte
	fmt.Println("Prasetiyo sedang belajar Golang Web"[1])
}
```

```
$ go run main.go
Prasetiyo
Prasetiyo sedang belajar Golang    
Prasetiyo sedang belajar Golang Web
9
80
114
```

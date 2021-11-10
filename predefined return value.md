``` golang
package main

import "fmt"

func main() {
	luas, keliling := calculate(10, 4)
	fmt.Println("Luas : ")
	fmt.Println(luas)
	fmt.Println("Keliling : ")
	fmt.Println(keliling)

}

func calculate(panjang int, lebar int) (luas int, keliling int) {
	luas = panjang * lebar
	keliling = 2 * (panjang + lebar)

	return
}

```

```
$ go run .
> Luas : 
> 40
> Keliling : 
> 28
```
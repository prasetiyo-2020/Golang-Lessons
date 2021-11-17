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

### Contoh ke-2
```golang
package main

import "fmt"

func main() {
	scores := []int{10, 5, 9, 8, 7}
	
	total := sum(scores)
	fmt.Println("Total nilai pada array adalah : ")
	fmt.Println(total)

	addition, substraction, multiple, division := calculation(3, 2)
	fmt.Println("Total pertambahan : ")
	fmt.Println(addition)
	fmt.Println("Total perkurangan : ")
	fmt.Println(substraction)
	fmt.Println("Total perkalian : ")
	fmt.Println(multiple)
	fmt.Println("Total pembagian : ")
	fmt.Println(division)
}

// Fungsi mencari total nilai
func sum(numbers []int) int {
	var total int
	for _, number := range numbers {
		total = total + number
	}

	return total
}

func calculation(number1 int, number2 int) (addition int, substraction int, multiple int, division int) {
	addition = number1 + number2
	substraction = number1 - number2
	multiple = number1 * number2
	division = number1 / number2

	return
}

```
```
$ go run .
> Total nilai pada array adalah :
> 39
> Total pertambahan :
> 5
> Total perkurangan :
> 1
> Total perkalian :
> 6
> Total pembagian :
> 1
```

### Contoh ke-3
```golang
package main

import (
	"errors"
	"fmt"
)

func main() {
	result, err := calculate(5, 4, "*")
	if err != nil {
		fmt.Println("Terjadi Kesalahan")
		fmt.Println(err.Error())
	}

	fmt.Println(result)
}

func calculate(number int, numberTwo int, operation string) (int, error) {
	var result int
	var errorResult error

	switch operation {
	case "+":
		result = number + numberTwo
	case "-":
		result = number - numberTwo
	case "*":
		result = number * numberTwo
	case "/":
		result = number / numberTwo
	default:
		errorResult = errors.New("unknown operation")
	}

	return result, errorResult
}
```

#### Output saat argumen tidak sesuai kriteria
```
$ go run .
> Terjadi Kesalahan
> unknown operation
> 0
```

#### Output saat argumen sesuai kriteria
```
$ go run .
> 20
```

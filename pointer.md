## Pointer Basic 1

``` golang
func main() {
	numberA := 15
	numberB := &numberA

	fmt.Println(numberA) // 15
	fmt.Println(numberB) // 0xc00001a088
	fmt.Println(*numberB) // 15

	*numberB = 30
	fmt.Println(*numberB) // 30
	fmt.Println(numberA) // 30
}
```
``` golang
func main() {
	var numberA int = 2
	var numberB *int = &numberA

	fmt.Println(numberA) // 2
	fmt.Println(numberB) // 0xc00001a088
	fmt.Println(*numberB) // 2

	numberA = 100
	fmt.Println(numberA) // 100
	fmt.Println(numberB) // 0xc00001a088
	fmt.Println(*numberB) // 100

}
```
## Pointer Basic 2
``` golang
func main() {
	number := 25
	fmt.Println("Alamat memory : ", &number) // Alamat memory :  0xc0000a8058
	fmt.Println("Nilai Awal : ", number) // Nilai Awal :  25

	change(&number, 100) // Alamat memory di dalam function :  0xc0000cc020
			     // Di dalam function :  100

	fmt.Println("Nilai Akhir : ", number) //Nilai Akhir :  100
}

func change(old *int, new int) {
	*old = new
	fmt.Println("Alamat memory di dalam function : ", &old)
	fmt.Println("Di dalam function : ", *old)
}
```

## Pointer struct sebagai parameter
``` golang
package main

import "fmt"

type Student struct {
	id   int
	name string
	GPA  float64
}

func main() {
	student := Student{1, "Prasetiyo", 3.78}
	fmt.Println("Nama sebelum lulus : " + student.name) // Nama sebelum lulus : Prasetiyo
	graduate(&student)				    // Nama setelah lulus : Prasetiyo S. Kom
}

func graduate(student *Student) {
	student.name = student.name + " S. Kom"
	fmt.Println("Nama setelah lulus : " + student.name)
}

```

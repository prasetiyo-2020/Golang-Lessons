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
## Pointer 

# Variadic Function
- Parameter yang berada di posisi terakhir, memiliki kemampuan dijadikan sebuah varargs.
- Varargs artinya datanya bisa menerima lebih dari satu input, atau angap saja semacam Array.
- Apa bedanya dengan parameter biasa dengan tipe data Array?
  - Jika parameter tipe Array, kita wajib membuat array terlebih dahulu sebelum mengirimkan ke function
  - Jika parameter menggunakan vararghs, kita bisa langsung mengirim datanya, jika lebih dari satu, cukup gunakan tanda koma

## Variadic Function
```golang
func main() {
	total := sumAll(10, 20, 30, 40)
	fmt.Println(total) // 100
}

// "..." adalah varargs
func sumAll(numbers ...int) int {
	total := 0
	for _, number := range numbers {
		total += number
	}

	return total
}
```

## Menggunakan Slice Sebagai Arguments
```golang
func main() {
	sliceNumber := []int{10, 20, 30, 40}

	total := sumAll(sliceNumber...)
	fmt.Println(total) // 100
}

func sumAll(numbers ...int) int {
	total := 0
	for _, number := range numbers {
		total += number
	}

	return total
}
```

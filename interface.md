``` golang
package main

import "fmt"

type BangunDatar interface {
	hitungLuas() int
}

type Persegi struct {
	sisi int
}

func (persegi Persegi) hitungLuas() int {
	return persegi.sisi * persegi.sisi
}

type PersegiPanjang struct {
	panjang int
	lebar   int
}

func (persegiPanjang PersegiPanjang) hitungLuas() int {
	return persegiPanjang.panjang * persegiPanjang.lebar
}

func main() {
	// Persegi
	persegi := Persegi{sisi: 4}
	luasPersegi := seberapaLuas(persegi)
	fmt.Println("Luas Persegi : ", luasPersegi)

	// Persegi Panjang
	persegiPanjang := PersegiPanjang{panjang: 6, lebar: 5}
	luasPersegiPanjang := seberapaLuas(persegiPanjang)
	fmt.Println("Luas Persegi Panjang : ", luasPersegiPanjang)
}

func seberapaLuas(bangunDatar BangunDatar) int {
	return bangunDatar.hitungLuas()
}

```
```
$ go run .
> Luas Persegi :  16
> Luas Persegi Panjang :  30
```

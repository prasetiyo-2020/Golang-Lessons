```golang
package main

import "fmt"

func main() {
	var languages [5]string
	languages[0] = "Go"
	languages[1] = "Javascript"
	languages[2] = "Python"
	languages[3] = "Ruby"
	languages[4] = "C#"

	fmt.Println(languages)
	length := len(languages)
	fmt.Println(length)
}
```

#### OR

```golang
package main

import "fmt"

func main() {
	languages := [5]string{"Go", "Javascript", "Python", "Ruby", "C#"}

	fmt.Println(languages)
	length := len(languages)
	fmt.Println(length)
}

```

#### Jika pengisian array menggunakan cara vertikal maka perlu menambahkan "," jika kurung tutup kurawal terpisah dengan array terakhir
``` golang
package main

import "fmt"

func main() {
	languages := [5]string{
		"Go",
		"Javascript",
		"Python",
		"Ruby",
		"C#",
	}

	fmt.Println(languages)
	length := len(languages)
	fmt.Println(length)
}

```
```
$ go run .
> [Go Javascript Python Ruby C#]
> 5
```

#### Menggunakan simbol "..." agar jumlah array tidak memiliki batasan jumlah

``` golang
package main

import "fmt"

func main() {
	languages := [...]string{
		"Go",
		"Javascript",
		"Python",
		"Ruby",
		"C#",
		"C",
	}

	fmt.Println(languages)
	length := len(languages)
	fmt.Println(length)
}

```
```
$ go run .
> [Go Javascript Python Ruby C# C]
> 6
```


#### Menggunakan forEach pada Array
```golang
package main

import "fmt"

func main() {
	languages := [...]string{
		"Go",
		"Javascript",
		"Python",
		"Ruby",
		"C#",
		"C",
	}

	for index, lang := range languages {
		fmt.Println(" index : ", index, " language : ", lang)
	}
}
```

```
$ go run .
> index :  0  language :  Go
> index :  1  language :  Javascript
> index :  2  language :  Python
> index :  3  language :  Ruby
> index :  4  language :  C#
> index :  5  language :  C
```

## Mencari nilai rata-rata pada array
``` golang
package main

import "fmt"

func main() {
	// hitung rata-rata
	scores := [8]int{100, 80, 75, 92, 70, 93, 88, 67}

	// Penjumlahan isi dari map
	var total int
	for _, score := range scores {
		total = total + score
	}

	// Jumlah dari map
	length := len(scores)

	// Hasil pecahan
	average := float64(total) / float64(length)

	// Hasil bilangan bulat
	averageInt := total / length

	fmt.Println("Menghasilkan bilangan pecahan : ")
	fmt.Println(average)
	fmt.Println("=======================")
	fmt.Println("Menghasilkan bilangan bulat : ")
	fmt.Println(averageInt)
}

```
```
$ go run .
> Menghasilkan bilangan pecahan : 
> 83.125
> =======================
> Menghasilkan bilangan bulat :
> 83
```

## Mencari nilai dengan kondisi tertentu pada array
``` golang
package main

import "fmt"

func main() {
	// Mencari nilai >= 90
	scores := [8]int{100, 80, 75, 92, 70, 93, 88, 67}

	// Membuat variabel kosong untuk menampung nilai array
	var goodScores []int

	// Melakukan perulangan forEach dengan kondisi score >= 90
	for _, score := range scores {
		if score >= 90 {
			goodScores = append(goodScores, score)
		}
	}

	fmt.Println("Isi array goodScores saat ini : ")
	fmt.Println(goodScores)
}
```

```
$ go run .
> Isi array goodScores saat ini : 
> [100 92 93]
```

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

```golang
package main

import "fmt"

func main() {
	var mataKuliahs []string

	mataKuliahs = append(mataKuliahs, "Basis Data")
	mataKuliahs = append(mataKuliahs, "Pemrograman Berorientasi Objek")
	mataKuliahs = append(mataKuliahs, "Pemrograman Web")

	fmt.Println(mataKuliahs)
}
```

#### OR
``` golang
package main

import "fmt"

func main() {
	mataKuliahs := []string{"Basis Data", "Pemrograman Berorientasi Objek", "Pemrograman Web"}
	fmt.Println(mataKuliahs)
}

```

```
$ go run .
> [Basis Data Pemrograman Berorientasi Objek Pemrograman Web]
```

#### forEach pada Slice
```golang
package main

import "fmt"

func main() {
	var mataKuliahs []string

	mataKuliahs = append(mataKuliahs, "Basis Data")
	mataKuliahs = append(mataKuliahs, "Pemrograman Berorientasi Objek")
	mataKuliahs = append(mataKuliahs, "Pemrograman")

	for _, mataKuliah := range mataKuliahs {
		fmt.Println(mataKuliah)
	}
}
```

```
$ go run .
> Basis Data
> Pemrograman Berorientasi Objek
> Pemrograman
```

## Constant

``` golang
func main() {
	const firstName = "Yosho"
	const lastName string = "Prasetiyo"

	fmt.Println(firstName)
	fmt.Println(lastName)
}
```
```
$ go run main.go
> Yosho
> Prasetiyo
```

## Deklarasi Multiple Variable menggunakan Const
``` golang
package main

import "fmt"

func main() {
	const (
		firstName = "Yosho"
		lastName  = "Prasetiyo"
	)

	fmt.Println(firstName)
	fmt.Println(lastName)
}
```
```
$ go run main.go
> Yosho
> Prasetiyo
```


## Jika mengubah isi dari tipe variabel const
``` golang
package main

import "fmt"

func main() {
	const firstName = "Yosho"
	const lastName string = "Prasetiyo"

	// Jika mengubah isi dari tipe variabel const
	firstName = "Diana"
	lastName = "Putri"

	fmt.Println(firstName)
	fmt.Println(lastName)
}
```

```
$ go run main.go
# command-line-arguments
.\main.go:10:12: cannot assign to firstName (declared const)
.\main.go:11:11: cannot assign to lastName (declared const)
```

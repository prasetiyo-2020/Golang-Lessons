File hello1.go
``` golang
package main
import "fmt"

func main() {
	firstName := "Prasetiyo"
	fmt.Println(firstName)

	aboutMe := TestAja()
	fmt.Println(aboutMe)
}
```

File hello2.go
``` golang
package main
import "fmt"

func TestAja() string {
	return fmt.Sprintf("Saya %s, saya suka berbagi setiap tanggal %d", "Prasetiyo", 10)
}
```
#### File hello1.go dan hello2.go saling terhubung karena masing-masing file menggunakan main package
```
$ go run hello1.go hello2.go
> Prasetiyo
> Saya Prasetiyo, saya suka berbagi setiap tanggal 10
```

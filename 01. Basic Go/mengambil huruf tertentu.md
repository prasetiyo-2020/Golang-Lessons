#### Cetak Huruf yang memiliki angka genap menggunakan IF
``` golang
package main
import "fmt"

func main() {
	judul := "Saya sedang belajar fundamental golang"

	for index, letter := range judul {
		letterstring := string(letter)
		if letterstring == "a" || letterstring == "i" || letterstring == "u" || letterstring == "e" || letterstring == "o" {
			fmt.Println("index :", index, "letter : ", string(letter))
		}
	}
}
```

#### Cetak Huruf yang memiliki angka genap menggunakan Switch
```golang
func main() {
	judul := "Saya sedang belajar fundamental golang"

	for index, letter := range judul {
		letterstring := string(letter)
		switch letterstring {
		case "a", "i", "u", "e", "o":
			fmt.Println("index :", index, " letter:", string(letter))
		}
	}
}
```

```
$ go run .
index : 1  letter: a
index : 3  letter: a
index : 6  letter: e
index : 8  letter: a
index : 13  letter: e
index : 15  letter: a
index : 17  letter: a
index : 21  letter: u
index : 24  letter: a
index : 26  letter: e
index : 29  letter: a
index : 33  letter: o
index : 35  letter: a
```

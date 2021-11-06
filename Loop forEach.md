``` golang
package main
import "fmt"

func main() {
	judul := "Saya sedang belajar fundamental golang"

	for index, letter := range judul {
		fmt.Println("index : ", index, " letter : ", string(letter))
	}
}

```

```
$ go run .
index :  0  letter :  S
index :  1  letter :  a
index :  2  letter :  y
index :  3  letter :  a
index :  4  letter :   
index :  5  letter :  s
index :  6  letter :  e
index :  7  letter :  d
index :  8  letter :  a
index :  9  letter :  n
index :  10  letter :  g
index :  11  letter :
index :  12  letter :  b
index :  13  letter :  e
index :  14  letter :  l
index :  15  letter :  a
index :  16  letter :  j
index :  17  letter :  a
index :  18  letter :  r
index :  19  letter :
index :  20  letter :  f
index :  21  letter :  u
index :  22  letter :  n
index :  23  letter :  d
index :  24  letter :  a
index :  25  letter :  m
index :  26  letter :  e
index :  27  letter :  n
index :  28  letter :  t
index :  29  letter :  a
index :  30  letter :  l
index :  31  letter :
index :  32  letter :  g
index :  33  letter :  o
index :  34  letter :  l
index :  35  letter :  a
index :  36  letter :  n
index :  37  letter :  g
```

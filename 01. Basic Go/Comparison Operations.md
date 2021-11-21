## Comparison Operations

| Operator  | Keterangan |
| :-------------: | :-------------: |
| > | Lebih dari  |
| < | Kurang dari  |
| >= | Lebih atau sama dengan  |
| <= | Kurang atau sama dengan  |
| == | Sama dengan  |
| != | Tidak sama dengan  |

``` golang
package main

import "fmt"

func main() {
	var score1 int8 = 10
	var score2 int8 = 10

	var compare1 bool = score1 == score2
	var compare2 bool = score1 > score2
	var compare3 bool = score1 < score2
	var compare4 bool = score1 >= score2
	var compare5 bool = score1 <= score2
	var compare6 bool = score1 != score2
	fmt.Println(compare1)
	fmt.Println(compare2)
	fmt.Println(compare3)
	fmt.Println(compare4)
	fmt.Println(compare5)
	fmt.Println(compare6)
}
```

```
$ go run main.go
> true
> false
> false
> true
> true
> false
```

``` golang
package main

import "fmt"

func main() {
	students := []map[string]string{
		{"Nama": "Prasetiyo", "Score": "B"},
		{"Nama": "Diana", "Score": "A"},
		{"Nama": "Gem", "Score": "C"},
	}

	for _, student := range students {
		fmt.Println(student)
	}
}
```

```
$ go run .
> map[Nama:Prasetiyo Score:B]
> map[Nama:Diana Score:A]
> map[Nama:Gem Score:C] 
```

``` golang
package main

import "fmt"

func main() {
	students := []map[string]string{
		{"Name": "Prasetiyo", "Score": "B"},
		{"Name": "Diana", "Score": "A"},
		{"Name": "Gem", "Score": "C"},
	}

	for _, student := range students {
		fmt.Println(student["Name"], " - ", student["Score"])
	}
}
```

```
$ go run .
> Prasetiyo  -  B
> Diana  -  A
> Gem  -  C
``` 

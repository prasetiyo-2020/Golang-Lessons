```golang
package main

import "fmt"

func main() {
	myMap := map[string]int{}

	myMap["Python"] = 8
	myMap["Ruby"] = 9
	myMap["Javascript"] = 10

	fmt.Println(myMap["Python"])
}
```

```
$ go run .
> 8
```

``` golang
package main

import "fmt"

func main() {
	myMap := map[string]string{
		"Python":     "is Powerfull",
		"Javascript": "is confusing",
		"Go":         "is ....",
	}

	fmt.Println(myMap)
}
```

```
$ go run .
> map[Go:is .... Javascript:is confusing Python:is Powerfull]
```

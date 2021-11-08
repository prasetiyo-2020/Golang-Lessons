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

## ForEach pada Map
``` golang
package main

import "fmt"

func main() {
	myMap := map[string]string{
		"Python":     "is Powerfull",
		"Javascript": "is confusing",
		"Go":         "is ....",
	}

	for key, value := range myMap {
		fmt.Println(" Key : ", key, " Value : ", value)
	}
}
```
```
$ go run .
> Key :  Python  Value :  is Powerfull
> Key :  Javascript  Value :  is confusing
> Key :  Go  Value :  is ....
```

## Menghapus isi Map
```golang
package main

import "fmt"

func main() {
	myMap := map[string]string{
		"Python":     "is Powerfull",
		"Javascript": "is confusing",
		"Go":         "is ....",
	}

	fmt.Println("Sebelum dihapus : ")
	for key, value := range myMap {
		fmt.Println(" Key : ", key, " Value : ", value)
	}

	fmt.Println("==================")

	delete(myMap, "Go")
	fmt.Println("Setelah dihapus : ")

	for key, value := range myMap {
		fmt.Println(" Key : ", key, " Value : ", value)
	}
}
```
```
$ go run .
> Sebelum dihapus : 
> Key :  Python  Value :  is Powerfull    
> Key :  Javascript  Value :  is confusing
> Key :  Go  Value :  is ....
> ==================
> Setelah dihapus :
> Key :  Python  Value :  is Powerfull    
> Key :  Javascript  Value :  is confusing
```

## Pengecekan isi Map
``` golang
package main

import "fmt"

func main() {
	myMap := map[string]string{
		"Python":     "is Powerfull",
		"Javascript": "is confusing",
		"Go":         "is ....",
	}

	fmt.Println("Pengecekan apakah terdapat key tertentu pada Map")
	fmt.Println("-------------------------------------------------")
	fmt.Println("Jika key tersedia : ")
	_, isAvailable2 := myMap["Python"]
	fmt.Println(isAvailable2)

	fmt.Println("=================================================")

	fmt.Println("Jika key tidak tersedia : ")
	_, isAvailable1 := myMap["Java"]
	fmt.Println(isAvailable1)

}
```
```
$ go run .
> Pengecekan apakah terdapat key tertentu pada Map
> -------------------------------------------------
> Jika key tersedia :
> true
> =================================================
> Jika key tidak tersedia :
> false
```

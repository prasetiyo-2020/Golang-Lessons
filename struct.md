``` golang
package main

import "fmt"

type User struct {
	id        int
	firstName string
	lastName  string
	email     string
	isActive  bool
}

func main() {
	user := User{}
	fmt.Println(user)
}
```

#### Menjalankan untuk pertama kali
```
$ go run .
> {0    false}
```

#### Ketika struck dipakai
``` golang
package main

import "fmt"

type User struct {
	id        int
	firstName string
	lastName  string
	email     string
	isActive  bool
}

func main() {
	// Instance cara ke-1
	user := User{}
	user.id = 1
	user.firstName = "Yosho"
	user.lastName = "Prasetiyo"
	user.email = "prasetiyo2020@yahoo.com"
	user.isActive = true

	// Instance cara ke-2
	// Posisi bisa diacak, misalkan id ditelakkan paling terakhir
	user2 := User{id: 2, firstName: "Diana", lastName: "Syafitri", email: "diana2020@yahoo.com", isActive: false}

	user3 := User{
		id:        3,
		firstName: "Rama",
		lastName:  "Ristawan",
		email:     "rama2020@yahoo.com",
		isActive:  true,
	}

	// Instance cara ke-3
	// Dengan cara menghilangkan nama propertinya, namun inputan harus urut atau sesuai
	user4 := User{4, "Azis", "Saputra", "azis2020@yahoo.com", true}

	fmt.Println(user)
	fmt.Println(user2)
	fmt.Println(user3)
	fmt.Println(user4)
}

```

```
$ go run .
> {1 Yosho Prasetiyo prasetiyo2020@yahoo.com true}
> {2 Diana Syafitri diana2020@yahoo.com false}
> {3 Rama Ristawan rama2020@yahoo.com true}   
> {4 Azis Saputra azis2020@yahoo.com true}  
```

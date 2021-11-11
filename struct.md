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

## Struct sebagai parameter
``` golang
type User struct {
	id        int
	firstName string
	lastName  string
	email     string
	isActive  bool
}

func main() {
	user1 := User{1, "Yosho", "Prasetiyo", "prasetiyo2020@yahoo.com", true}
	user2 := User{2, "Diana", "Syafitri", "diana2020@yahoo.com", true}

	displayUser1 := displayUser(user1)
	displayUser2 := displayUser(user2)
	fmt.Println(displayUser1)
	fmt.Println(displayUser2)
}

// "User" sebagai tipe data
func displayUser(user User) string {
	result := fmt.Sprintf("Name : %s %s \nEmail : %s", user.firstName, user.lastName, user.email)
	return result
}
```

```
$ go run .
> Name : Yosho Prasetiyo
> Email : prasetiyo2020@yahoo.com
> Name : Diana Syafitri      
> Email : diana2020@yahoo.com
```

## Embedded struct
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

type Group struct {
	name        string
	admin       User
	users       []User
	isAvaliable bool
}

func main() {
	user1 := User{1, "Yosho", "Prasetiyo", "prasetiyo2020@yahoo.com", true}
	user2 := User{2, "Diana", "Syafitri", "diana2020@yahoo.com", true}

	users := []User{user1, user2}

	group := Group{"Gagak Hitam", user1, users, true}

	displayGroup(group)
}

func displayGroup(group Group) {
	fmt.Printf("Nama Group : %s", group.name)
	fmt.Println("")
	fmt.Printf("Jumlah Anggota : %d", len(group.users))
	fmt.Println("")

	fmt.Println("Nama Anggota : ")
	fmt.Println("================")
	for _, user := range group.users {
		fmt.Println(user.firstName)
	}

	fmt.Println("================")
	fmt.Println("Status Group")
	if group.isAvaliable == true {
		fmt.Println("Tersedia")
	} else {
		fmt.Println("Tidak Tersedia")
	}
}
```

```
$ go run .
> Nama Group : Gagak Hitam
> Jumlah Anggota : 2
> Nama Anggota :
> ================
> Yosho
> Diana
> ================
> Status Group
> Tidak Tersedia
```

## Method
```golang
package main

import "fmt"

type User struct {
	id        int
	firstName string
	lastName  string
	email     string
	isActive  bool
}

func (user User) display() string {
	return fmt.Sprintf("Name : %s %s \nEmail : %s", user.firstName, user.lastName, user.email)
}

func main() {
	user1 := User{1, "Yosho", "Prasetiyo", "prasetiyo2020@yahoo.com", true}
	user2 := User{2, "Diana", "Syafitri", "diana2020@yahoo.com", true}

	result := user1.display()
	fmt.Println(result)
	fmt.Println(user2.display())
}
```

```
$ go run .
> Name : Yosho Prasetiyo
> Email : prasetiyo2020@yahoo.com
```

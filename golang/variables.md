# variables

```go
package main

import "fmt"

var c, python, java bool

func main() {
	var i int
	fmt.Println(i, c, python, java)
}

```

> 0 false false false



Default int is 0

Default bool is false.



## variable with initialise

```go
package main

import "fmt"

var i, j int = 1, 2

func main() {
	var c, python, java = true, false, "no!"
	fmt.Println(i, j, c, python, java)
}

```

> 1 2 true false no!





### Shorthand variable

Inside a function `:=` can be used as a shorthand to assign value to varibale

You don't need type when do this

```go
package main

import "fmt"

func main() {
	var i, j int = 1, 2
	k := 3
	c, python, java := true, false, "no!"

	fmt.Println(i, j, k, c, python, java)
}
```



But outside a function, you need to declare the variable types:

```go
package main

import "fmt"

var i, j int = 1, 2
func main() {
	k := 3
	c, python, java := true, false, "no!"

	fmt.Println(i, j, k, c, python, java)
}
```

## Const

```go
package main

import "fmt"

const Pi = 3.14

func main() {
    fmt.Println("Go rules?")
}
```


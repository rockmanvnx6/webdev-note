## Function

### Function syntax

```go
func main(argc int, argv []string) int
```



Dropping parameters:



```go
func main(int, []string) int
```



**Example**

```go
package main

import "fmt"

func add(x int, y int) int {
    return x+y
}

func main() {
    fmt.Println(add(42,13))
}
```



*If 2 or more parameters have the same type, we can shorten it*

```go
package main

import "fmt"

func add(x,y int) int {
    return x + y
}

func main() {
    fmt.Println(add(42,13))
}
```



### Return multiple result

```go
package main

import "fmt"

func swap(x,y string) (string, string) {
    return y,x
}

func main() {
    a,b := swap("second", "first")
    fmt.Println(a,b)
}
```

```result
first second
```

> `:=` to return to both variables.



### Naked return

```go
func split(sum int) (x,y int) {
    x = sum / 3
    y = sum - x
    return
}

func main() {
    fmt.Println(split(20))
}
```

> Naked return return based on the the variable defined in the top of the function.
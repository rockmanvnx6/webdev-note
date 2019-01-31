# Syntax

Imagine like this

```go
x: int
p: pointer to int
a: array[3] of int
```



Read from left to right

```go
x int
p *int
a [3]int
```



Apparently reading from left to right is easier.



## Function syntax

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



## pointer

```go
var a []int
x = a[1]
```



```go
var p *int
x = *p
```


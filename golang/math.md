# math/rand

```go
package main

import (
	"fmt"
    "math/rand"
)

func main() {
    rand.Seed(0) // seed rand
    fmt.Println("my number: ", rand.Intn(10)); // random from 0-10
}
```



# Math/pi

```go
package main

import (
	"fmt"
    "math"
)

func main() {
    fmt.Println(math.Pi)
}
```

> `P` has to be capital.


## Gin's RealIP Middleware

[Gin](https://github.com/gin-gonic/gin)'s Real IP middleware to set a http.Request's RemoteAddr to the results of parsing either the X-Forwarded-For header or the X-Real-IP header.

## Usage

```go
package main

import (
  "github.com/gin-gonic/gin"
  "github.com/thanhhh/gin-gonic-realip"
)

func main() {
  r := gin.New() // without any middlewares

  router.Use(middleware.RealIP())

  r.Get("/", func() string {
    return "Hello world!"
  })

  r.Run(":8080")
}
```

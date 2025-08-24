# snowflake

high performance Snowflake ID generator, 
built with atomics for speed and efficiency.

built in `sql/driver` and json support

## installation
```bash
go get github.com/nyahchat/snowflake
```

## usage
```go
package main

import (
    "log"
    "github.com/nyahchat/snowflake"
)

func main() {
    nodeId := 1
    epochInMillis := snowflake.TwitterEpoch
    
    generator, _ := snowflake.NewGenerator(nodeId, epochInMillis)

    snowflake := generator.MustGenerate()
    log.Printf("snowflake: %s", snowflake.String())
}
```
# Metaparticle/Sync go library

Metaparticle/Sync for go is a library that implements distributed synchronization for
cloud-native applications using a container sidecar and Kubernetes primitives.


## Quickstart

```go
import (
	"context"
	"time"

	"github.com/metaparticle-io/sync/go/sync"
)

fn main() {
	lock := mpsync.NewLock("some-lock", mpsync.DEFAULT_INTERVAL)
	lock.Lock(context.Background(), func(c context.Context) error {
		fmt.Println("Hello, World!")
		time.Sleep(time.Second * 15)
	})
}
```


# Shows you can set the return variables before the return statement
```
package main

import "errors"

func main() {
	er := x()
	if er != nil {
		println("error")
	}
}

func x() (err error) {
	err = errors.New("this error")
	return
}
```

# For running unit tests with `//go:build unit_test` tag
```
ginkgo -tags=unit_test
```

# To go fmt
```
gofmt -s -w .

// and

gofumpt -l -w .

// and

gci write .
```

# To lint
```
golangci-lint run
```

# oci2aci

oci2aci is a small package that converts [OCI](https://github.com/opencontainers/specs) bundle to
[ACI](https://github.com/appc/spec/blob/master/SPEC.md#app-container-image). It takes OCI bundle as input, and gets ACI image as output.

## Installation
Make sure you have a working Go environment (go 1.1+ is *required*). [See the install instructions](http://golang.org/doc/install.html).

To install it, simply run:
```
$ go get github.com/octools/oci2aci
```

Make sure your `PATH` includes to the `$GOPATH/bin` directory so your commands can be easily used:
```
export PATH=$PATH:$GOPATH/bin
```

## Getting Started
One of the philosophies behind `cli.go` is that an API should be playful and full of discovery. So a `cli.go` app can be as little as one line of code in `main()`. 

``` go
package main

import (
  "github.com/octools/oci2aci"
)

func main() {
  aciImgPath, err := oci2aci.Oci2aciImage(ociPath)
}
```

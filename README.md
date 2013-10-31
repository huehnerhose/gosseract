gosseract-ocr
=============

tesseract-ocr wrapper by Golang

[What is tesseract-ocr?](https://code.google.com/p/tesseract-ocr/) 

Set Up
=============

```sh
apt-get install tesseract-ocr # Basic OCR library by C++
# or yum? brew? Choose the way whichever you can install `tesseract-ocr`
go get github.com/otiai10/gosseract-ocr
go get github.com/r7kamura/gosple # for testing
```

First of All, Run the Tests!!
=============

```sh
cd tests
go test -i
go test
```

Usage
=============

```go
package main

import (
  "github.com/otiai10/gosseract-ocr"
  "fmt"
)

func main() {
  args := gosseract.AnywayArgs{
    SourcePath: "./sample.png",
  }
  text := gosseract.Anyway(args)
  fmt.Printf("Result : %v", text)
}
```
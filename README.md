# EXANTE - Go Client
[EXANTE](https://exante.eu/) Market Data API Client for Go

[![License MIT](https://img.shields.io/badge/License-MIT-blue.svg)](http://opensource.org/licenses/MIT) [![Build Status](https://travis-ci.org/zerodivisi0n/exante-api-go.svg?branch=master)](http://travis-ci.org/zerodivisi0n/exante-api-go)

## Installation
```bash
go get -u github.com/zerodivisi0n/exante-api-go
```

## Basic Usage
```go
package main

import (
	"fmt"
	"github.com/zerodivisi0n/exante-api-go"
)

func main() {
	clientID := os.Getenv("EXANTE_CLIENT_ID")
	applicationID := os.Getenv("EXANTE_APPLICATION_ID")
	sharedKey := os.Getenv("EXANTE_SHARED_KEY")

	client := exante.NewClient(clientID, applicationID, sharedKey)

	exchanges, err := client.Exchanges()
	if err != nil {
		fmt.Println(err)
	} else {
		fmt.Println(exchanges)
	}
}
```

## License

(The MIT License)

Copyright (c) 2012-2016 Apcera Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to
deal in the Software without restriction, including without limitation the
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or
sell copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS
IN THE SOFTWARE.

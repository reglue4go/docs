# Stringable

> Table of Contents

-   [Introduction](#introduction)
-   [Available Methods](#available-methods)
-   [Method listing](#method-listing)

## Introduction

The stringable package provides a fluent chainable object-oriented interface for working with string values.

```go
package main

import "github.com/reglue4go/stringable"

func main() {
	value := stringable.New("GOLANG").Lower().Ucfirst().Value()

	fmt.Printf("%v\n", value) // Golang
}

```

## Available Methods

Each method available on the stringable instance may be chained to fluently manipulate the underlying value.
Almost every method returns a new stringable instance, allowing you to preserve the original copy of the value when necessary:

| Stringable      |                   |                   |
| --------------- | ----------------- | ----------------- |
| [Of](#Of)       | [Substr](#substr) | [Before](#before) |
| [Lower](#Lower) | [After](#After)   | [Upper](#upper)   |
| [Upper](#Upper) |                   |                   |

## Method listing

#### Lower

The lower method converts the given string to lowercase:

```go
value := stringable.New("GOLANG").Lower().Value()

fmt.Printf("%v\n", value) // golang
```

#### Upper

The lower method converts the given string to uppercase:

```go
value := stringable.New("golang").Upper().Value()

fmt.Printf("%v\n", value) // GOLANG
```

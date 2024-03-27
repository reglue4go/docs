# Stringable

[![Reglue Go - Stringable](https://img.shields.io/static/v1?label=coverage&message=100%&color=green&logo=coveralls)](https://github.com/reglue4go/stringable)

> Table of Contents
>
> -   [Introduction](#introduction)
> -   [Available Methods](#available-methods)
> -   [Method Listing](#method-listing)

## Introduction

The stringable package provides an expressive chainable interface for working with string values.

```go
package main

import "github.com/reglue4go/stringable"

func main() {
	instance := stringable.New("GOLANG").Lower().Ucfirst()

	fmt.Printf("%v\n", instance.Value()) // Golang
}

```

## Available Methods

Each method available on the stringable instance may be chained to fluently manipulate the underlying value.
Almost every method returns a new stringable instance, allowing you to preserve the original copy of the value when necessary:

|                 |                     |                           |                   |
| --------------- | ------------------- | ------------------------- | ----------------- |
| [Of](#Of)       | [NewLine](#NewLine) | [BeforeLast](#BeforeLast) | [Append](#Append) |
| [Lower](#Lower) | [After](#After)     | [AfterLast](#AfterLast)   | [Substr](#substr) |
| [Upper](#Upper) | [Before](#before)   |                           |                   |

## Method Listing

#### Lower

The lower method converts the given string to lowercase:

```go
value := stringable.New("GOLANG").Lower().Value() // golang
```

#### Upper

The lower method converts the given string to uppercase:

```go
value := stringable.New("golang").Upper().Value() // GOLANG
```

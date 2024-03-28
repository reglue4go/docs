# Stringable

[![Reglue Go - Stringable](https://img.shields.io/static/v1?label=coverage&message=100%&color=green&logo=coveralls)](https://github.com/reglue4go/stringable)

> Table Of Contents
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

|                     |                     |                               |                         |
| ------------------- | ------------------- | ----------------------------- | ----------------------- |
| [Of](#Of)           | [NewLine](#NewLine) | [BeforeLast](#BeforeLast)     | [Append](#Append)       |
| [Lower](#lower)     | [After](#After)     | [AfterLast](#AfterLast)       | [Substr](#substr)       |
| [Upper](#upper)     | [Before](#before)   | [Between](#Between)           | [Basename](#Basename)   |
| [Ucfirst](#Ucfirst) | [Title](#Title)     | [BetweenFirst](#BetweenFirst) | [Camel](#Camel)         |
| [String](#String)   | [Value](#Value)     | [ToDate](#ToDate)             | [ToBoolean](#ToBoolean) |

## Method Listing

#### [Lower](#available-methods)

The Lower method converts the given string to lowercase:

```go
value := stringable.New("GOLANG").Lower().Value() // golang
```

#### [Upper](#available-methods)

The Upper method converts the given string to uppercase:

```go
value := stringable.New("golang").Upper().Value() // GOLANG
```

[![Go logo](https://reglue4go.github.io/docs/img/go/Go-Logo_Fuchsia.svg 'Go logo')](#top)

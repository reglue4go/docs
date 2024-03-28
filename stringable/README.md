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

|                               |                                     |                                   |                                   |
| ----------------------------- | ----------------------------------- | --------------------------------- | --------------------------------- |
| [After](#after)               | [AfterLast](#afterLast)             | [Append](#append)                 | [Basename](#basename)             |
| [Before](#before)             | [BeforeLast](#beforeLast)           | [Between](#between)               | [BetweenFirst](#betweenFirst)     |
| [Camel](#camel)               | [Contains](#contains)               | [ContainsAll](#containsAll)       | [Dirname](#dirname)               |
| [Dump](#dump)                 | [EndsWith](#endsWith)               | [Exactly](#exactly)               | [Explode](#explode)               |
| [Headline](#headline)         | [IsEmpty](#isEmpty)                 | [IsNotEmpty](#isNotEmpty)         | [Kebab](#Kebab)                   |
| [Lcfirst](#lcfirst)           | [Length](#length)                   | [Limit](#limit)                   | [Lower](#lower)                   |
| [Ltrim](#ltrim)               | [NewLine](#newLine)                 | [Of](#Of)                         | [PadBoth](#padBoth)               |
| [PadLeft](#padLeft)           | [PadRight](#padRight)               | [Pipe](#pipe)                     | [Prepend](#prepend)               |
| [Remove](#remove)             | [Repeat](#repeat)                   | [Replace](#replace)               | [ReplaceArray](#replaceArray)     |
| [ReplaceFirst](#replaceFirst) | [Rtrim](#rtrim)                     | [Slug](#slug)                     | [Snake](#snake)                   |
| [StartsWith](#startsWith)     | [String](#string)                   | [Studly](#studly)                 | [Substr](#substr)                 |
| [Title](#title)               | [ToBoolean](#toBoolean)             | [ToDate](#toDate)                 | [ToFloat](#toFloat)               |
| [ToInteger](#toInteger)       | [ToString](#toString)               | [Trim](#trim)                     | [Ucfirst](#ucfirst)               |
| [Unless](#unless)             | [Upper](#upper)                     | [Value](#value)                   | [When](#when)                     |
| [WhenContains](#whenContains) | [WhenContainsAll](#whenContainsAll) | [WhenEmpty](#whenEmpty)           | [WhenEndsWith](#whenEndsWith)     |
| [WhenExactly](#whenExactly)   | [WhenNotEmpty](#whenNotEmpty)       | [WhenNotExactly](#whenNotExactly) | [WhenStartsWith](#whenStartsWith) |
| [Wrap](#wrap)                 |                                     |                                   |                                   |

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

# Stringable

[![linux](https://img.shields.io/static/v1?label=linux&message=✓&color=green&logo=linux)](#top)
[![macos](https://img.shields.io/static/v1?label=macos&message=✓&color=green&logo=apple)](#top)
[![windows](https://img.shields.io/static/v1?label=windows&message=✓&color=green&logo=windows10)](#top)

[![tests](https://img.shields.io/static/v1?label=coverage&message=100%&color=green&logo=coveralls)](#top)

> Table Of Contents
>
> -   [Introduction](#introduction)
> -   [Available Methods](#available-methods)
> -   [Method Listing](#method-listing)
> -   [Unit Tests Matrix](#unit-tests-matrix)

## Introduction

The stringable package provides an expressive chainable interface for working with string values.

```go
package main

import "github.com/reglue4go/stringable"

func main() {
	title := stringable.New("GO").Append("LanG").Ucfirst().Value()

	fmt.Printf("%v\n", title)
	// Golang
}

```

## Available Methods

Each method available on the stringable instance may be chained to fluently manipulate the underlying value.
Almost every method returns a new stringable instance, allowing you to preserve the original copy of the value when necessary:

| &mldr;                        | &mldr;                              | &mldr;                            | &mldr;                            |
| ----------------------------- | ----------------------------------- | --------------------------------- | --------------------------------- |
| [After](#after)               | [AfterLast](#afterlast)             | [Append](#append)                 | [Basename](#basename)             |
| [Before](#before)             | [BeforeLast](#beforelast)           | [Between](#between)               | [BetweenFirst](#betweenfirst)     |
| [Camel](#camel)               | [Contains](#contains)               | [ContainsAll](#containsall)       | [Dirname](#dirname)               |
| [Dump](#dump)                 | [EndsWith](#endswith)               | [Exactly](#exactly)               | [Explode](#explode)               |
| [Headline](#headline)         | [IsEmpty](#isempty)                 | [IsNotEmpty](#isnotempty)         | [Kebab](#Kebab)                   |
| [Lcfirst](#lcfirst)           | [Length](#length)                   | [Limit](#limit)                   | [Lower](#lower)                   |
| [Ltrim](#ltrim)               | [NewLine](#newline)                 | [Of](#Of)                         | [PadBoth](#padboth)               |
| [PadLeft](#padleft)           | [PadRight](#padright)               | [Pipe](#pipe)                     | [Prepend](#prepend)               |
| [Remove](#remove)             | [Repeat](#repeat)                   | [Replace](#replace)               | [ReplaceArray](#replacearray)     |
| [ReplaceFirst](#replacefirst) | [Rtrim](#rtrim)                     | [Slug](#slug)                     | [Snake](#snake)                   |
| [StartsWith](#startswith)     | [String](#string)                   | [Studly](#studly)                 | [Substr](#substr)                 |
| [Title](#title)               | [ToBoolean](#toboolean)             | [ToDate](#todate)                 | [ToFloat](#tofloat)               |
| [ToInteger](#tointeger)       | [ToString](#tostring)               | [Trim](#trim)                     | [Ucfirst](#ucfirst)               |
| [Unless](#unless)             | [Upper](#upper)                     | [Value](#value)                   | [When](#when)                     |
| [WhenContains](#whencontains) | [WhenContainsAll](#whencontainsall) | [WhenEmpty](#whenempty)           | [WhenEndsWith](#whenendswith)     |
| [WhenExactly](#whenexactly)   | [WhenNotEmpty](#whennotempty)       | [WhenNotExactly](#whennotexactly) | [WhenStartsWith](#whenstartswith) |
| [Wrap](#wrap)                 |                                     |                                   |                                   |

## Method Listing

#### [Dirname](#available-methods)

The Dirname method returns the parent directory portion of the given string:

```go
value := stringable.New("/foo/bar/baz").Dirname().Value()
// "/foo/bar"
```

#### [ContainsAll](#available-methods)

The ContainsAll method determines if the given string contains all of the values in the given array:

```go
value := stringable.New("This is my name").ContainsAll("my", "name")
// true
```

#### [Contains](#available-methods)

The Contains method determines if the given string contains the given value. This method is case sensitive:

```go
value := stringable.New("This is my name").Contains("my")
// true
```

#### [Camel](#available-methods)

The Camel method converts the given string to camelCase:

```go
value := stringable.New("foo_bar").Camel().Value()
// "fooBar"
```

#### [BetweenFirst](#available-methods)

The BetweenFirst method returns the smallest possible portion of a string between two values:

```go
value := stringable.New("[a] bc [d]").BetweenFirst("[", "]").Value()
// "a"
```

#### [Between](#available-methods)

The Between method returns the portion of a string between two values:

```go
value := stringable.New("This is my name").Between("This", "name").Value()
// " is my "
```

#### [BeforeLast](#available-methods)

The BeforeLast method returns everything before the last occurrence of the given value in a string:

```go
value := stringable.New("This is my name").BeforeLast("is").Value()
// "This "
```

#### [Before](#available-methods)

The Before method returns everything before the given value in a string:

```go
value := stringable.New("This is my name").Before("my name").Value()
// "This is "
```

#### [Basename](#available-methods)

The Basename method will return the trailing name component of the given string:

```go
value := stringable.New("/foo/bar/baz").Basename().Value()
// "baz"
```

#### [Append](#available-methods)

The Append method appends the given values to the string:

```go
value := stringable.New("Paula").Append(" ", "White").Value()
// "Paula White"
```

#### [AfterLast](#available-methods)

The AfterLast method method returns everything after the last occurrence of the given value in a string. The entire string will be returned if the value does not exist within the string:

```go
value := stringable.New("App\Http\Controllers\Controller").AfterLast("\\").Value()
// "Controller"
```

#### [After](#available-methods)

The After method method returns everything after the given value in a string. The entire string will be returned if the value does not exist within the string:

```go
value := stringable.New("This is my name").After("This is").Value()
// " my name"
```

#### [Lower](#available-methods)

The Lower method converts the given string to lowercase:

```go
value := stringable.New("GOLANG").Lower().Value()
// golang
```

#### [Upper](#available-methods)

The Upper method converts the given string to uppercase:

```go
value := stringable.New("golang").Upper().Value()
// GOLANG
```

## Unit Tests Matrix

> This package has been successfully tested on the following platform versions.

| golang | ubuntu | macos | windows |
| :----- | :----: | :---: | :-----: |
| 1.18.x |   ✓    |   ✓   |    ✓    |
| 1.20.x |   ✓    |   ✓   |    ✓    |
| 1.22.x |   ✓    |   ✓   |    ✓    |

[![Go logo](https://reglue4go.github.io/docs/img/go/Go-Logo_Blue.svg 'Scroll up')](#top)

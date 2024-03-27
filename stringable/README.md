# Stringable

> Table of Contents

-   [Introduction](#introduction)
-   [Available Methods](#available-methods)
-   [Method listing](#method-listing)

## Introduction

The stringable package provides a fluent chainable object-oriented interface for working with string values.

## Available Methods

Each method available on the stringable instance may be chained to fluently manipulate the underlying value.
Almost every method returns a new stringable instance, allowing you to preserve the original copy of the value when necessary:

| Stringable                 |                              |                              |
| -------------------------- | ---------------------------- | ---------------------------- |
| [Of](#stringable-of)       | [Substr](#stringable-substr) | [Before](#stringable-before) |
| [Lower](#stringable-Lower) | [After](#stringable-After)   | [Upper](#stringable-upper)   |
| [Upper](#stringable-Upper) |                              |                              |

## Method listing

### Stringable Lower

The lower method converts the given string to lowercase:

```go
	value := New("GOLANG").Lower()

    fmt.Printf("%v\n", value)

    // golang
```

### Stringable Upper

The lower method converts the given string to uppercase:

```go
	value := New("GOLANG").Upper()

    fmt.Printf("%v\n", value)

    // golang
```

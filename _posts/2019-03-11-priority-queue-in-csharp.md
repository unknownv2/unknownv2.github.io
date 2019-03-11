---
layout: post
title:  "Priority Queue in C#"
date:   2019-03-11 23:00:00 -0700
categories: programming
---

C# doesn't have a default `PriorityQueue` implementation as part of the .NET Base Class Libaries(BCL), so I started a collection of
some data structure implementations, which include several Priority Queue classes [in this repository](https://github.com/unknownv2/data-structures).

The official tracking issue for adding a `PriorityQueue` implementation to .NET Core can be found [here](https://github.com/dotnet/corefx/issues/574).

## Code Example

In `Java`, the default PriorityQueue orders the values according to their `natural ordering`, which would be ascending order for integers.
[You can find more information about it from the PriorityQueue documentation.](https://docs.oracle.com/javase/8/docs/api/java/util/PriorityQueue.html)

You can create a simple max-heap with a priority queue using:

```Java
PriorityQueue<Integer> queue = new PriorityQueue<>((a,b) -> b - a);
```
The equivalent implementation using one of the classes from the above repository collection in `C#` would be:

```C#
var queue = new Psi.SimplePriorityQueue<int>((a, b) => b - a);
```

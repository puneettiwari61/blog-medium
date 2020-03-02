---
title: "Map and Set in Javascript"
description: "Among others, the following four data structures are new in ECMAScript 6: Map, WeakMap, Set and WeakSet."
date: "2019-12-21T11:27:53.924Z"
categories: []
published: true
canonical_link: https://medium.com/@puneettiwari61/map-and-set-in-javascript-45cc1e183890
redirect_from:
  - /map-and-set-in-javascript-45cc1e183890
---

_Among others, the following four data structures are new in ECMAScript 6:_ `Map`, `WeakMap`, `Set` and `WeakSet`.

![](./asset-1.jpeg)

In this blog, we gonna learn about Map and Set.

Objects and Arrays are already there, then why do we need more data structures like Map and Set.

Working on real projects handling big and complicated data, somewhere Objects and Arrays are not enough. That’s why **Map** and **Set** also exist.

To understand in an easy manner, we can say Map is like an Object and Set is more like an Array.

So, **What’s the difference?**

[**Map**](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) **is a collection of keyed data items, just like an Object. But the main difference is that Map allows keys of any type.**

Yes, unlike an Object where keys are always a string, Map gives us freedom and lets us use arbitrary values as keys and is highly welcome.

Working with single entries.

As above, creating a map is really easy adding single entries to it can be done by `map.set(key, value)` – stores the value by the key.

The important thing we should notice in the above example is that, we are using any data-type as a key, including number, boolean and even we are using **Object** as a key.

**Map can also use objects as keys.**

> _Using objects as keys is one of the most notable and important_ **_Map_** _features. For string keys,_ **_Object_** _can be fine, but not for object keys._

Methods and properties are:

-   `new Map()` – creates the map.
-   `map.set(key, value)` – stores the value by the key.
-   `map.get(key)` – returns the value by the key, `undefined` if `key` doesn’t exist in map.
-   `map.has(key)` – returns `true` if the `key` exists, `false` otherwise.
-   `map.delete(key)` – removes the value by the key.
-   `map.clear()` – removes everything from the map.
-   `map.size` – returns the current element count.

Let’s play with a few map methods.

We can set up a map via an iterable over key-value “pairs” (arrays with 2 elements). One possibility is to use an array (which is iterable)

➡️ **map.size, map.get( ), map.has( )**

Hope, it helped to understand maps.

Let’s understand Set.

### **Sets**

> A Set is a collection of unique elements.

**Unlike an array, we can’t repeat values in Set.**

Managing single elements in Set.

Creating a Set is really easy as above. Let’s see more ways

We can set up a set via an iterable over the elements that make up the set. For example, via an array:

`Set` – is a collection of unique values.

Methods and properties:

-   `new Set([iterable])` – creates the set, with optional `iterable` (e.g. array) of values for initialization.
-   `set.add(value)` – adds a value (does nothing if `value` exists), returns the set itself.
-   `set.delete(value)` – removes the value, returns `true` if `value` existed at the moment of the call, otherwise `false`.
-   `set.has(value)` – returns `true` if the value exists in the set, otherwise `false`.
-   `set.clear()` – removes everything from the set.
-   `set.size` – is the elements count.

### Let’s see how to iterate over **Map** and **Set** elements.

### Iteration over Map

For looping over a `map`, there are 3 methods:

-   `map.keys()` – returns an iterable for keys,
-   `map.values()` – returns an iterable for values,
-   `map.entries()` – returns an iterable for entries `[key, value]`, it’s used by default in `for..of`.

**\*\*\*Both Map and Set has an inbuilt forEach method to loop over their elements.**

### Iteration over Set

The same methods `Map` has for iterators are also supported:

-   `set.keys()` – returns an iterable object for values,
-   `set.values()` – same as `set.keys()`, for compatibility with `Map`,
-   `set.entries()` – returns an iterable object for entries `[value, value]`, exists for compatibility with `Map`.

_Iteration over_ `_Map_` _and_ `_Set_` _is always in the insertion order, so we can’t say that these collections are unordered, but we can’t reorder elements or directly get an element by its number._

Hope, this article has helped you to understand Map and Set better :)

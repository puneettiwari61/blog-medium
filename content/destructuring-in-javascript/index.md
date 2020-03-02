---
title: "Destructuring in JavaScript"
description: "“Destructuring” does not mean “destructive”."
date: "2019-12-18T06:06:54.355Z"
categories: []
published: true
canonical_link: https://medium.com/@puneettiwari61/destructuring-in-javascript-bdf41aa7b600
redirect_from:
  - /destructuring-in-javascript-bdf41aa7b600
---

**_“Destructuring” does not mean “destructive”._**

![](./asset-1.jpeg)

Still remember, the first time when I saw a code something like this..

```
let [color, day] = ['red', 'sunday']
```

I was like how we are declaring an array name itself as an array with square brackets that too by using ‘let’. I know its kinda beginner’s way of approaching it 😅😛.

After understanding how it works, I thought it's just syntax sugar, yeah it's really a syntax sugar but really help us easier to express and saves our few lines of code.

**Let’s see how it works.**

### It allows us to extract properties from an object or items from an array, multiple at a time.

In arrays, if we have to store its values in variables, we generally prefer this way ⬇️

---

So, how destructuring gonna help us, let’s see.

Yes, it was that simple. As it is an array it stores its values with respect to their index. With the help of destructuring it's really easy to store its value in variables without assigning it to one variable at a time.

_It’s called “destructuring assignment,” because it “destructurizes” by copying items into variables. But the array itself is not modified._

**What if we don’t want all values?**

Yes, it's totally fine to leave the one we don't want, just leave space after and before the comma.

**Can we set default values to some variables?**

Why not?

Yeah, its totally fine to give default values to variables, in case there are no corresponding values to them in the array.

If there will be value in the array then the default value will get overwrite.

### Objects

An old way

As we can see above to copy values in variables from an object we generally write like this.

**Let’s see how destructuring helps in Objects.**

Yes, it's that easy, we can do this in one line, without assigning values one by one to variables.

-   \*\* It's important to keep the same name for the variable as the name of the property.

Even in objects, we can use default values similarly like arrays.

_It’s possible to extract data from nested arrays/objects, for that the left side must have the same structure as the right one._

**Hope, it helped to understand destructuring better.**

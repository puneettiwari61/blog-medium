---
title: "Express Middleware — Let’s build one and understand its paradigm."
description: "Express has become the de facto standard for building web apps in Node. To understand Express, it's important to understand Express…"
date: "2020-03-02T05:54:01.421Z"
categories: []
published: false
---

Express has become the de facto standard for building web apps in Node. To understand Express, it's important to understand Express Middleware.

![Express JS](./asset-1.png)

### According to official Expressjs docs — 

**_Middleware_** _functions are functions that have access to the_ [_request object_](https://expressjs.com/en/4x/api.html#req) _(_`_req_`_), the_ [_response object_](https://expressjs.com/en/4x/api.html#res) _(_`_res_`_), and the_ `_next_` _function in the application’s request-response cycle. The_ `_next_` _function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware._

In simpler words, whenever we receive any request from client, middleware facilitates us a way to manipulate the request object or to grab something important from it and even can end the request-response cycle.

**Let’s see a very simple example of a middleware function.**

```
app.use(express.json( ));
```

This is a built-in middleware function in Express. It parses incoming requests with JSON and appends it to the request body.

Similarly for the form we have 

```
app.use(express.urlencoded({ extended: false }));
```

This is a built-in middleware function in Express. It parses incoming requests with urlencoded and appends the data coming from to request body.

**Now let’s see types of middleware functions and their usage.**

Following is a list of possibly used middleware in Express.js app:

-   Application-level middleware
-   Router-level middleware
-   Error-handling middleware
-   Built-in middleware
-   Third-party middleware

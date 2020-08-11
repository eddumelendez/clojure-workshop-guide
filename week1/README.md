# Week 1

Topic:

* Functional Programing Concepts
* Introduction to Clojure

First, REPL is needed. In order to start we need to execute `lein repl` in our terminal.

We will start with a `Hello World`.

* Defining a `String`

```clojure
(def hello-word "Hello World")

(class hello-word)

(print hello-world)
``` 

* Defining a `Number`

```clojure
(def my-number 1)

(class my-number)

(print my-number)
``` 

* Defining a `Ratio`

```clojure
(def my-ratio 2/3)

(class my-ratio)

(print my-ratio)
``` 

* Defining a `Double`

```clojure
(def my-double 2.3)

(class my-double)

(print my-double)
``` 

* Defining a `BigDecimal`

```clojure
(def my-bigdecimal 2.3M)

(class my-bigdecimal)

(print my-bigdecimal)
``` 

* Defining a `Keyword`

```clojure
(def my-keyword :this-is-a-keyword)

(class my-keyword)

(print my-keyword)
``` 

## Namespaces

* Create a namespace

```clojure
(create-ns 'clojure-workshop)
```

* Change namespace

```clojure
(ns user)
```

* Create and change namespace

```clojure
(in-ns 'clojure-workshop)
```

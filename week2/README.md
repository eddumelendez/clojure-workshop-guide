# Week 2

Topics:

* Declaring functions
* Anonymous functions 

In order to write the next functions, we will be creating a project using `lein` and will start the `repl` in order to execute them. Execute the next commands in your terminal:

```
lein new app workshop

cd workshop

lein repl
```

Now, open your IDE and go to `src/workshop/core.clj`

## Functions

### Print Hello World

```clojure
(defn my-function []
  (print "Hello World"))

;; The next expression should be execute it in repl

(my-function)
```

Using anonymous function:

```clojure
(def my-function2 (fn[] (print "Hello World")))

;; The next expression should be execute it in repl

(my-function2)
```

```clojure
(def my-function3 #(print "Hello World"))

;; The next expression should be execute it in repl

(my-function3)
```

### Sum

```clojure
(defn my-function []
  (+ 1 1))

;; The next expression should be execute it in repl

(my-function)
```

Using anonymous function:

```clojure
(def my-function2 (fn[] (+ 1 1)))

;; The next expression should be execute it in repl

(my-function2)
```

```clojure
(def my-function3 #(+ 1 1))

;; The next expression should be execute it in repl

(my-function3)
```

## Functions with arguments

First, create a namespace `src/workshop/week2.clj`. Inside of the new namespace add the following line:

```clojure
(ns workshop.week2)
```

In `repl`, move to other namespace `(ns week2)`

### Print Hello World

```clojure
(defn my-function [name]
  (print (str "Hello " name)))

;; The next expression should be execute it in repl

(my-function)
```

Using anonymous function:

```clojure
(def my-function (fn[name] 
  (print (str "Hello " name))))

;; The next expression should be execute it in repl

(my-function)
```

```clojure
;; if there is more than 1 arg you can use % follow by the arg's number

(def my-function3 #(print (str "Hello " %)))

;; The next expression should be execute it in repl

(my-function)
```

### Sum

```clojure
(defn my-function [operation a b]
  (operation a b))

;; The next expression should be execute it in repl

(my-function)
```

Using anonymous function:

```clojure
(def my-function2 (fn[operation a b] (operation a b)))

;; The next expression should be execute it in repl

(my-function2)
```

```clojure
(def my-function3 #(%1 %2 %3))

;; The next expression should be execute it in repl

(my-function3)
```

NOTE: If there is any update in the namespace after loading the repl use `(use 'workshop.<namespace> :reload)` to reload the content.

# Resources

* [Learn Clojure - Functions](https://clojure.org/guides/learn/functions)
* [Basics of Function](https://clojurebridge.org/community-docs/docs/clojure/function-creation/)

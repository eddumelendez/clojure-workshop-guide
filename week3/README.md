# Week 3

Topics:

* Variadic functions
* Multi-arity functions
* Applying functions
* Partial functions

First, create a namespace `src/workshop/week3.clj`. Inside of the new namespace add the following line:

In `repl`, move to other namespace `(ns week3)`

```clojure
(ns workshop.week3)
```

## Variadic functions

```clojure
(defn variadic-fn [a b & args]
  (println a b args))

(defn variadic-fn [a b c & args]
  (println a b c args))
```

## Multi-arity functions

```clojure
(defn multiarity-fn
  ([a b]
    (println a b))
  ([a b & args]
    (println a b args)))
```

```clojure
(defn multiarity-fn
  ([a b] 
    (multiarity-fn a b 0))
  ([a b & args] 
    (println a b args)))
```

## Applying functions

```clojure
(apply + [1 2 3 4])

(apply + 1 [2 3 4])
```

```clojure
(apply str ["a" "b" "c"])

(apply str "a" ["b" "c"])
```

```clojure
(defn sum
  ([a b]
    (sum a b 0))
  ([a b & args]
    (apply + a b args)))
```

## Partial functions

```clojure
(def my-partial (partial sum 1))
```

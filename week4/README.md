# Week 4

Topics:

* Lists
* Vectors
* Maps
* Set

## Lists

Creating a list

```clojure
(list 1 2 3)

'(1 2 3)

(def my-list '(1 2 3))
```

'Modifying' a list

```clojure
(conj my-list 4)
```

## Vectors

Creating a vector

```clojure
(vector 1 2 3)

[1 2 3]

(def my-vector [1 2 3])
```

'Modifying' a vector

```clojure
(conj my-vector 4)
```

Examine a vector

```clojure
(get my-vector 0)
```

## Maps

Creating a map

```clojure
(def my-map {:a 1 :b 2})

(def my-nested-map {:a {:b 2}})
```

'Modifying' a map

```clojure
(assoc my-map :c 3)

(dissoc my-map :b)

(assoc-in my-nested-map [:a :c] 3)
```

Examine a map

```clojure
(get my-map :a)

(:a my-map)

(get-in my-nested-map [:a :b])
```

## Set

Creating a set

```clojure
(hash-set 1 2 3)

(sorted-set 1 2 3)

#{1 2 3}

(def my-set #{1 2 3})
```

'Modifying' a set

```clojure
(conj my-set 4)

(disj my-set 3)
```

# Resources

* [Collections](https://clojure.org/reference/data_structures#Collections)

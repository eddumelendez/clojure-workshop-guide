# Week 5

Topics:

* Destructuring
* if
    - if-let
    - if-not
* when 
    - when-let
    - when-not
* case
* cond

## Destructuring

Sequential

```clojure
(def my-vector [1 2 3])

(let [[x y z] my-vector]
  (println x y z))
```

Associative

```clojure
(def client {:name "Super Co."
             :location "Philadelphia"
             :description "The worldwide leader in plastic tableware."})

(let [{name :name
       location :location
       description :description} client]
  (println name location "-" description))

(let [{:keys [name location description]} client]
  (println name location "-" description))
```

## if

By default suport only one sentence to execute
```clojure
(if true
    (println "this is true")
    (println "this is false"))
```

The third arg is used for else
```clojure
(if false ;; or nil
    (println "this is true")
    (println "this is false"))
```
if we want to execute more than one sentence we should use "do"

```clojure
(if true
    (do
    (println "this is true")
    (println "this is true, again"))
    (println "this is false"))
```

### if-let

```clojure
(def client {:name "Super Co."
             :location "Philadelphia"
             :description "The worldwide leader in plastic tableware."})

(if-let [name (:name client)]; nil is false
    (println name)
    (println "this is false"))
```


### if-not

```clojure
(def client {:name "Super Co."
             :location "Philadelphia"
             :description "The worldwide leader in plastic tableware."})

(if-not (:name client)
    (println "name doesnt exit")
    (println "this is false"))
```

## When

Use "When" when you only care about the case when condition is truthy
By default suport only many sentence to execute,
when is false return nil
```clojure
(when true
    (println "this is true")
    (println "this is true also"))
```

### when-let

```clojure
(def client {:name "Super Co."
             :location "Philadelphia"
             :description "The worldwide leader in plastic tableware."})

(when-let [name (:name client)]; nil is false
    (println name)
    (println "this is true"))
```


### when-not

```clojure
(def client {:name "Super Co."
             :location "Philadelphia"
             :description "The worldwide leader in plastic tableware."})

(when-not (:name client)
    (println "name doesnt exit")
    (println "this is false"))
```

## case

Case compares the value with each condition with = and evaluates the expression in the matched branch.
```clojure
(defn case-test
    [x]
    (case x
    1 "x is 1"
    2 "x is 2"
    "X is not allowed"))

(case-test 1)
(case-test 2)
(case-test 3)
```

## cond

Similiar to case but want to write your own test case rather than =
user => (defn cond-test
```clojure
(defn cond-test
    [x]
    (cond
    (= x 1) "x is 1"
    (and (>= x 2) (<= x 2)) "x is 2"
    :else "X is not allowed maraca"))

(cond-test 1)
(cond-test 2)
(cond-test 3)
```

```clojure
```
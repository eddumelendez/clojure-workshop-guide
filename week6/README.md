# Week 6

Topics

* Thread macros
    - Thread first
    - Thread Last
    - cond->
* comp

## Thread macros

Threading macros, also known as arrow macros, convert nested function calls into a linear flow of function calls, improving readability.

### Thread First (->)

Insert X as the first parameter in next function

```clojure
(-> "a b c" 
    .toUpperCase 
    (.replace "A" "X")
    first)

;;Result X
```

```clojure

(.replace (.toUpperCase "a b c") "A" "X")

;;Result X
```

### Thread Last (->>)

Insert X as the last parameter in the next function

```clojure
(->> [1 2 3 4] 
     (map #(+ 1 %)) 
     (filter odd?) first)

;Result = 3
```

```clojure
(first (filter odd? (map #(+ 1 %) [1 2 3 4])))

;Result = 3
```

### cond->

Takes a expression and insert X as the first in the next function when cond = true

```clojure
(cond-> 1
        true inc
        false (* 5)
        (= 2 2) (+ 2))
        
;Result = 4
```

### comp

Compose many fucntions in a call

```clojure

((comp #(+ 6 %) #(- 5 %)) 1)

;; (- 5 1) = 4
;; (+ 6 4) = 10

;Result = 10
```

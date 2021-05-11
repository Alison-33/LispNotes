# Lisp Notes

### Expressions
- Expressions are written as lists, using prefix notation, which places operators to the left of their oerands.
- The first element in an expression list is the name of a function and the remainder of the list are the arguments.
- `(- 14 (* 2 3))`


### Arity of functions
- **Arity** is used to describe the number of arguments or operands that a function takes.
- A unary function (arity 1) takes one argument. A binary function takes two arguments.
- An n-ary function takes n arguments
- Variable arity functions can take any number of arguments

### Prohibiting expresion evaluation
- `(/ (* 2 6) 3)` ; Returns 4.
- `'(/ (* 2 6) 3)` ; Returns (/ (* 2 6) 3).


### Boolean operations
- Lisp supports Boolean operators **and**, **or**, and **not**. The 2 former have variable arity, and the last one is unary.
- The values true/false are denoted in Lisp by t/nil respectively.
- The **or** Boolean operator evaluates its subexpressions from left to right and stops immediately if any subexpression evaluates to **true**.
```
\> (let ((x 5))
(or (< x 2) (> x 3))
T
```
- The **and** Boolean operator evaluates its subexpressions from left to right and stops immediately if any subexpression evaluates to **false**


### Constructing lists
- We have 3 built-in functions to create a list which are summarized below:
  1. **cons**: creates a list by adding an element as the head of an existing list
  2. **list**: creates a list comprised of its arguments.
  3. **append**: creates a list by concatenating existing lists.
- A list in Lisp is singly-linked where each node is a pair of 2 pointers, the first one pointing to a data element and the second one pointing to the tail of the list with the last node's second pointer pointing to the empty list.
```
\> (cons 'a '())
(A)

\> (cons 'a (cons 'b '()))
(A B)
```

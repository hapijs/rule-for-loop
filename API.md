
## About

This rule enforces the following:

- Restrict iterator variable names. `for` loop iterator variables should be named `i`. Nested loops should use the variables `j`, `k`, and so on.
- Restrict loop nesting.  You can restrict the maximum nesting of `for` loops. By default, this limit is three.
- Prevent postfix increment and decrement operators. The hapi style guide does not allow postfix increment and decrement operators in `for` loop updates. The prefix version of these operators should be used instead.
- Single variable declaration in initialization section. A single `var i = 0;` is allowed in the initialization section. This only applies to variable declarations, not assignments to existing variables. This means that `for (i = 0, j = 0)` is allowed if `i` and `j` are existing variables. Variable declarations involving destructuring are not allowed.

## Rule options

This rule can be configured by providing a single options object. The object supports the following keys.

### `maxDepth`

A number representing the maximum allowed nesting of `for` loops. Defaults to three.

### `startIterator`

The first variable iterator name to use. This defaults to `'i'`.
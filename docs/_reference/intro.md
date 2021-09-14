---
layout: page
title: Introduction
---
# The Gurklang Language Specification

## The aim of this specification

The Gurklang Language Specification, from here onwards referred to as "the specification", aims
to lay out the ground rules for any implementation of the Gurklang language, from here onwards
referred to as "Gurklang".

1. Any implementation of Gurklang which fails to comply with the criteria outlined in the specification 
will not be considered a valid implementation of Gurklang.

2. It is mandated that all viable implementations of Gurklang shall be open source as to increase
transparency and build a better community.

3. There are no restrictions on the implementation of Gurklang itself. As stated above, if an 
implementation produces expected behaviour, it is valid.

## Notation

The description of lexical analysis and syntax use [BNF Grammar Notation](https://en.wikipedia.org/wiki/Backus%E2%80%93Naur_form)
with slight modifications. Namely the absence of angle brackets: `<` and `>`.

```py
foo ::= bar ( bar | "-" )*
bar ::= "a"..."z"
```

Line 1 states that a `foo` is equivalent to a `bar` followed by 0 or more `bar`s or underscores.
Following on from this, Line 2 states that a `bar` is any letter in the range starting at `a` (ASCII: 97) ending at `z` (ASCII: 122)
present in the [Latin Alphabet](https://en.wikipedia.org/wiki/Latin_alphabet).

A brief summary of BNF Grammar is as follows.

1. A rule begins with a name which is defined in turn by that rule.
2. The name the rules defined is followed by `::=`.
3. A pipe/bar (`|`) is used to separate alternatives. It is the least binding operator in this notation.
4. A star/asterisk (`*`) represents 0 or more repetitions of the preceding item.
5. A plus (`+`) represents 1 or more repetitions of the preceding item.
6. An item enclosed in square brackets (`[...]`) means the item is optional.
7. The `*` and `+` operators bind as tightly as possible.
8. A pair of parentheses (`(...)`) is used for grouping
9. All string literals are enclosed in double quotes (`"..."`)
10. Rules or normally contained on single lines. Rules with many alternatives may be spread over multiple lines
with each line beginning with a pipe/bar (`|`). An example follows.
```py
foo ::= bar ( spam | "_" )*
        | spam ( bar | "_" )*
bar ::= "a"..."z"
spam ::= "@"
```
11. A phrase between a pair of angle brackets (`<` and `>`) will be assumed to provide context and information only;
it does not affect the grammar in any way.
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

The description of lexical analysis and syntax use [EBNF Grammar Notation](https://en.wikipedia.org/wiki/Extended_Backus%E2%80%93Naur_form)
with slight modifications. Namely the absence of angle brackets: `<` and `>`.

```py
foo = bar ( bar | "-" )*
bar = "a"..."z"
```

Line 1 states that a `foo` is equivalent to a `bar` followed by 0 or more `bar`s or underscores.
Following on from this, Line 2 states that a `bar` is any letter in the range starting at `a` (ASCII: 97) ending at `z` (ASCII: 122)
present in the [Unicode](https://home.unicode.org/).

### A table of reference for EBNF grammar

| Usage         | Notation          |
|:--------------|:------------------|
| Definition    | `=`               |
| Concatenation | `,`               |
| Termination   | `;`               |
| Alternation   | `|`               |
| Optional      | `[ ... ]`         |
| Repetition 	| `{ ... }`         |         
| Grouping      | `( ... )`         |
| String        | `" ... "`         |
| String    	| `' ... '`         |
| Comment    	| `(* ... *)`       |
| Special       | `? ... ?`         |
| Exception 	| `-`               |
---
layout: home
---
# Welcome to the Gurklang Language Specification
#### Gurklang is a stack-based, dynamically-typed and functional programming language.

## Stack-based
Every operation carried out in Gurklang makes a series of
changes to the stack. An empty stack is denoted as `()`.
For this example, the function `peek` returns the value of
the top-most item of the stack.

{% highlight bbcbasic %}
>>> peek
()
>>> 1
>>> peek
(1())
>>> 2
>>> peek
(2(1()))
{% endhighlight %}

## Dynamically-typed
Do not mistake a dynamic types with no types.
A dynamically typed programming language simply
defers the process of checking types until runtime;
type errors only occur after compilation, once you
have run the program.

{% highlight bbcbasic %}
>>> "a"
>>> "b"
>>> +
{% endhighlight %}

This program will raise an error complaining two strings can not be added
While this may seem rather disadvantageous, a dynamic type
system allows for more flexibility.

## Functional

Gurklang is influenced by programming languages such as [`Clojure`](https://clojure.org)
and [`Haskell`](https://www.haskell.org/). These languages emphasis a few main features, namely:

1. **Higher-order functions** - functions that operate on functions.
2. **Immutability** - a definition is not a variable, you can't reassign it.
3. **Strong typing** - don't hide errors, bring them out

[View on GitHub](https://github.com/doublevcodes/gurklang-spec){: .btn .btn-green }

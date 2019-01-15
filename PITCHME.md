## Regular expressions

* re
* regex
* regexp

---

## What are they

* mini-language (code)
* each char in regex is an instruction

---

## Transition graph

![](transition_graph.png)

---

## Pseudocode

![](pseudocode.png)

---

## Tricky parts

* syntax is not that tricky
* semantics is

---

## Implementation

* Traditional NFA (non-deterministic finite automaton)
* Used also by Java's [Pattern](https://docs.oracle.com/javase/10/docs/api/java/util/regex/Pattern.html#jcc)

---

## rxrx

```
$ cpanm Regexp::Debugger
```

---

## Greed

quantifiers (`*` `+` `?` `{ }`) match as long a substring as possible

```plain
/".*"/
'He said "hi", she said "hello"'
```

---

## Non-greedy

```plain
/".*?"/
'He said "hi", she said "hello"'
```

---

## Eagerness

leftmost match wins

```plain
/o*/
'good food'

/long|longer|longest/
'longest'
```

---

## Backtracking

the entire regex must match (not just part of it)

```plain
/".*"/
'He said "hi", she said hello'

/"[^"]*"/
'He said "hi", she said hello'
```

---

## More

* https://learning.oreilly.com/videos/understanding-regular-expressions/9781491996300

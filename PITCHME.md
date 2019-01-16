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

## Most common implementation

* Traditional NFA (non-deterministic finite automaton)
* Used also by Java's [Pattern](https://docs.oracle.com/javase/10/docs/api/java/util/regex/Pattern.html#jcc)

---

## Tools

* [Regexp::Debugger](https://metacpan.org/pod/Regexp::Debugger)
* [regex101.com](https://regex101.com)

---

## Greed

quantifiers (`*` `+` `?` `{ }`) match as long a substring as possible

* 'He said "hi", she said "hello"'
* [/".*"/](https://regex101.com/r/fMMSFn/2)
* [/".*?"/](https://regex101.com/r/fMMSFn/3)
* [/"[^"]*"/](https://regex101.com/r/fMMSFn/4)

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

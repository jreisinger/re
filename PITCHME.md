## Intro

* Traditional NFA (non-deterministic finite automaton)
* Used also by Java - https://docs.oracle.com/javase/10/docs/api/java/util/regex/Pattern.html#jcc

* syntax is not that tricky
* semantics is

---

## What are regular expressions

* regexes are actually code (executed on a VM)
* each char in regex is an instruction

---

## Pseudocode

![](pseudocode.png)

---

## Greed

quantifiers (* + ? { }) match as long a substring as possible

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

```
/o*/
'good food'

/long|longer|longest/
'longest'
```

---

## Backtracking

the entire regex must match (not just part of it)

```
/".*"/
'He said "hi", she said hello'

/"[^"]*"/
'He said "hi", she said hello'
```

---

## More

* https://learning.oreilly.com/videos/understanding-regular-expressions/

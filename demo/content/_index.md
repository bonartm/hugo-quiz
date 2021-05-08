---
title: "Demo"
date: 2019-11-19T17:21:20+01:00
page: true
---

# Hugo Quiz

A hugo shortcode for writing quizzes with a markdown-like syntax: https://github.com/bonartm/hugo-quiz.

**Try out the live code editor: https://bonartm.github.io/quizdown-live-editor/**

{{< quizdown >}}

---
primary_color: steelblue
---

# The sound of dog

---
shuffle_answers: false
---

What do dogs sound like?

> Some hint

```python
class Dog(Animal):
    def __init__(self, name):
        self.name = name
```

- [ ] yes
- [ ] no
- [ ] `self.sound = "meow"`
- [x] wuff

# Put the [days](https://en.wikipedia.org/wiki/Day) in order!

> Monday is the *first* day of the week.

1. Monday
2. Tuesday
3. Wednesday
4. Friday
5. Saturday  


# This question has no answer!

- [ ] yes
- [ ] no

{{< /quizdown >}}

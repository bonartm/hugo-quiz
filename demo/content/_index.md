---
title: "Demo"
date: 2019-11-19T17:21:20+01:00
page: true
---

# Hugo Quiz

Here is a simple example of a quiz, written in markdown using hugo shortcodes

{{% quiz test_quiz%}}

## Quiz header

{{< item question="What is Tom's name?" answer=2 choices="tim,tom,carl" >}}
{{< item question="What is the capital of Germany?" answer=2 choices="Cologne,Berlin,Hamburg" >}}

{{% /quiz %}}

Click on the `submit` button to see the result.
